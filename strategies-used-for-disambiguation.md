Once information retrieval is complete, ReCiter employs a series of strategies to match publications to target authors.

| Phase | Description and strategies |
| :--- | :--- |
| **0. Refine search for common names** | If, during initial retrieval, the count of candidate articles exceeds 2,000, employ a set of strategies to limit the number of results returned.[Limit by department](#limit-by-department)|
| **1. Cluster creation** | Independent of what is know about the target author, group articles in clusters in cases where they share distinctive characteristics. |
| **2. Cluster selection** | Use what is known about a person \(e.g., email address\) to select matching clusters. |
| **3. Individual article selection** | Select articles that were not picked up during cluster selection. |
| **4. Individual article removal** | Remove individual articles that are unlikely matches. |
| **5. Matching MeSH major** | Add articles that share MeSH major terms with selected articles. |

# 0. Refine search for common names

Yi Wang is a radiologist at Weill Cornell. At last count, about 93,795, or 0.3%, of all articles in PubMed were written by a "Y. Wang." Without modification, searching for this name can lead to high computation times and very low precision. In cases where a target author would return more than 2,000 candidate records, ReCiter cancels the initial search \(e.g., Wang Y OR email@med.cornell.edu\). Instead, ReCiter performs the initial search coupled with each of five more targeted searches. Then, it OR's the results of these searches together. This approach ensures that the number of candidate articles is far more manageable.

## Limit by department

The initial search is combined with the name\(s\) of any departments listed for the target author in db.identity. For example: "Wang Y AND Radiology\[affiliation\]."

See [Department Retrieval Srategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/DepartmentRetrievalStrategy.java)

## Limit by common affiliation

To capture publications written while at the current institution, ReCiter will append a canned search for all target authors that limits the results set to the institution's \(as opposed to the individual's\) two dozen or so most common co-authoring institution. For example:

> Wang Y AND \(\(new york\) OR 10065 OR 10021 OR weill OR cornell OR \(newyork AND presbyterian\) OR \(new york AND presbyterian\) OR HSS OR \(hospital special surgery\) OR \(North Shore hospital\) OR \(Long Island Jewish\) OR \(memorial sloan\) OR \(sloan kettering\) OR sloan-kettering OR hamad OR \(mount sinai\) OR \(methodist houston\) OR \(National Institute of Mental Health\) OR \(beth israel\) OR \(University of Pennsylvania Medicine\) OR \(Merck Research\) OR \(New York Medical College\) OR \(Medicine Dentistry New Jersey\) OR Montefiore OR \(Lenox Hill\) OR \(Cold Spring Harbor\) OR \(St. Luke's-Roosevelt\) OR \(New York University Medicine\) OR Langone OR \(SUNY Downstate\) OR \(Albert Einstein Medicine\) OR Yeshiva OR UMDNJ OR Icahn Medicine OR \(Mount Sinai\) OR \(columbia medical\) OR \(columbia physicians\)\)

See [Affiliation Retrieval Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/AffiliationRetrievalStrategy.java)

## Limit by institutional affiliation

The initial search is combined with all the institutional affiliations listed for the target author in db.identity. This is the only instance in the code where these institutional affiliations are used.

For example: "Wang Y AND \(Fudan University OR  University of Wisconsin Madison\)"

See [Affiliation in DB Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/AffiliationInDbRetrievalStrategy.java)

## Limit by grant ID

The initial search is combined with the grant IDs listed for the target author in db.identity. For example: "Wang Y AND EB01344\[Grant number\]."

See [Grant Retrieval Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/GrantRetrievalStrategy.java)

## Limit by first full name

The initial search is combined with the first full name of the target author. For example: "Wang Y AND Wang Yi."

See [First Name Initial Retrieval Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/FirstNameInitialRetrievalStrategy.java)

# 1. Cluster creation

## Seed with known articles

Db.GoldStandard contains known publications by a target author. If available, even a couple of such publications can dramatically improve the accuracy of the algorithm. Known pulications are used to seed the initial cluster.

See [Gold Standard Retrieval Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/xml/retriever/pubmed/GoldStandardRetrievalStrategy.java)

## Article completeness

Every article is sorted by completeness. This score is based on the presence of:

* Complete first name
* Three or more MeSH major terms
* Scopus affiliation ID of target author
* E-mail of target author
* Affiliations for all authors
* Three or more co-authors

If there is no known publications, the most complete article forms the first cluster. The next most complete article is compared against the most complete article.

If there is a known publication, those articles form the first cluster. The next most complete article is compared against the cluster originator.

They are added to the same cluster if one of the following cases occurs...

## Coauthor clustering

If two articles share the same co-authors \(excluding the name of the target author\), the pair of articles are clustered together.

## Journal clustering

If two articles share the same journal, the pair of articles are clustered together.

See [Name Matching Clustering Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/cluster/clusteringstrategy/article/NameMatchingClusteringStrategy.java)

# 2. Cluster selection

## Email

For each author in the article under consideration, ReCiter checks the affiliation field \(as indexed in both PubMed and Scopus\). If the field contains the target author's actual email, then the cluster is selected. Note that at Weill Cornell, there are several different email domains, so ReCiter also looks at other variants of the email \(i.e., uid + one of "@med.cornell.edu", "@mail.med.cornell.edu", "@weill.cornell.edu", or "@nyp.org"\).

See [Email String Match Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/email/strategy/EmailStringMatchStrategy.java)

## Department

Affiliations in papers often include "Department of...." Especially for smaller departments like Dermatology, this is a strong signal.

For each author in the article that it currently is examining, ReCiter extracts the department string using regex `Department of (.+?)[\\.,]` and checks if the extracted department matches one of the departments that the target author is in. If the department strings match and the first name initials match, then it selects that entire cluster.

See [Department String Match Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/department/strategy/DepartmentStringMatchStrategy.java)

## Known relationship

Institutions tend to have a lot of information on how people are connected. Person A and Person B are on the same grant. They're in the same HR unit or sub-unit \(e.g. a research lab\). They have an advisor/advisee relationship....

Here, ReCiter looks to see if there any co-authors in the candidate cluster that have a last name and first initial which matches a known relationship. ReCiter selects such clusters.

See [Known Coinvestigator Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/knownrelationship/strategy/KnownRelationshipStrategy.java)

## Common affiliation

In cases where an author's affiliation is not listed, the presence of a co-author from a home or frequently collaborating institution significantly increases the likelihood that the article was written by the target author. In the case of Weill Cornell, for example, we have learned that approximately 12 percent of articles for which one or more author affiliations is the Hospital for Special Surgery, also includes at least one author from Weill Cornell. You may want to experiment with different institutions to identify the effect on performance.

If one of these institutions appears in the affiliation string, ReCiter selects the entire cluster.

See \[Common Affiliation Strategy\] \([https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/affiliation/strategy/CommonAffiliationStrategy.java](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/affiliation/strategy/CommonAffiliationStrategy.java)\)

# 3. Individual article selection

At this point, ReCiter goes back and looks for cases where it can justify selecting additional individual articles.

## Common coauthor

ReCiter compares the current article under consideration against all the articles in an already selected cluster. ReCiter checks if there are any matching mutual coauthors by checking first, middle, and last name. Such a match must be 100% \(Junie B. Jones ≠ Junie Jones\). If the number of mutual coauthors is at least one, then the article is also selected.

See [Coauthor Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/article/coauthor/strategy/CoauthorStrategy.java)

## Common journal

This strategy works by comparing the current article that we are considering with articles in an already selected cluster. It checks if the journal of the two articles match, then it checks if the two articles' target author share the same first name. If both journal and first name match, then we add this article to that cluster.

See [Journal Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/article/journal/strategy/JournalStrategy.java)

## Cites, cited by, and co-citation

PubMed Central contains a subset of all the occasions when one article cites another article. There are three cases that ReCiter uses:

* cites - Article A cites Article B
* cited by - Article B cites Article A
* co-citation - Article C cites Article A and Article B

When any one of these cases occurs and any one of these is already in the selected cluster, the likelihood that both are authored by the target author increases. Articles A, B, and C are all added to the selected cluster.

ReCiter does not use cited by metadata from Scopus.

See [Citation Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/article/citation/strategy/CitationStrategy.java)

## Article size

Some people have relatively unique names. Using number of candidate records as an indication, we can be more aggressive in assuming such people wrote an article.

If a target author has &lt; 200 candidate publications, assume that such a person wrote it in these circumstances:

1. Matching full first name \(Richard Granstein, e.g., 6605225\), or
2. Matching first initial and middle initial \(RD Granstein, e.g., 8288913\), or

If a target author has &lt; 500 candidate publications, assume that such a person wrote it in these circumstances:

1. Full first, middle initial, and last name match, and
2. Matching institutional affiliation

Example: Richard D. Granstein, e.g., 6231484, or Carl F. Nathan, e.g., 3989315\)

See \[Article Size Strategy\] \([https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/articlesize/strategy/ArticleSizeStrategy.java](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/articlesize/strategy/ArticleSizeStrategy.java)\)

# 4. Individual article removal

## Degree year discrepancy

### Bachelors

Check the difference between journal publication year of the article and the target author's year of bachelor's degree.  If the candidate article is published any more than one year prior to their bachelor's degree, remove the article from the selected cluster.

### Doctoral

Check the difference between journal publication year of the article and the target author's year of terminal or doctoral degree.

* If the doctoral year is &lt; 1998 and if the difference is &lt; -6, then this article is removed.
* Else if the doctoral year is &gt;= 1998 and if the difference is &lt; -13, then this article is removed.

This variability was included because starting around 1998, doctoral students became much more likely to author articles with their names indexed as co-authors.

See [Year Discrepancy Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/degree/strategy/YearDiscrepancyStrategy.java)

## Remove by name

The variable use of spaces, dashes, periods, co-mingling first and middle names, etc. poses a lot of challenges. Collecting every institutional instance of different aliases of users gets some of the way there. But some author names can, at best, only be predicted.

After cycling through any known names as indexed in some institutional source, this strategy attempts to anticipate names that aren't explicitly defined in db.identity. The following is a set of examples for how this strategy works.

| Name in db.identity | Name as indexed in article | Decision | Notes / additional condition to fulfill |
| --- | --- | --- | --- |
| Juan Miguel | Juan-Miguel | Keep |  |
| Juan Miguel | J-M | Keep |  |
| Bi-sen | Bisen | Keep |  |
| Bi-sen | B-S | Keep |  |
| Mary J. Roman | MJ Roman | Keep |  |
| Nasser Altorki | Nassar Altorki | Keep | Levenstein distance &lt; 2; common affiliation must also be positive |
| Massimiliano Szulc | Massimo Szulc | Keep | first three characters match; common affiliation is also positive |
| Joan \(first name\) H.F.\(middle name\) Drosopoulos \(last name\) | Joan HF \(first name\) Drosopoulos \(last name\) | Keep |  |
| W. Clay Bracken | C. Bracken | Keep |  |
| J. David Warren | DK Warren | Remove |  |
| Anna Bender | Anna M. Bender | Remove | middle initial indexed in article but is null in db.identity |
| Aaron J. Marcus | AO Marcus | Remove |  |
| W. Clay Bracken | WC Bracken | Keep |  |

See [Remove By Name Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/targetauthor/name/RemoveByNameStrategyContext.java)

# 5. Matching MeSH major

National Library of Medicine indexes articles with the MeSH vocabulary. In cases where a MeSH term is judged to be especially relevant to an article, the major designation is also added.

We have noticed that a given author tends to be recurrently indexed with the same MeSH major terms. As an example, Ronald G. Crystal has published 123 papers in which "adenoviridae" is an indexed MeSH major term. Only 19,097 articles have been so indexed. Dr. Crystal personally accounts for over 0.6% of all papers. That is a lot!

The MeSH major strategy works as follows:

* Identify papers in the non-selected group that share MeSH major terms with those in the selected group.
* Count up how often that term is used in the selected pile. Suppose, in all the other selected articles, a MeSH major is used 12 times.
* Look up how common that MeSH major terms is used in PubMed. Suppose there are 2,000 papers in all of PubMed that also have that term.
* Multiply 12 by 10,000 \(a constant\) and then divide by 2,000 \(the raw count in all of PubMed for that term\). If the resulting number exceeds some threshold \(currently 0.4\), then move the article into the selected pile.

See [MeSH Major Strategy](https://github.com/wcmc-its/ReCiter/blob/master/src/main/java/reciter/algorithm/evidence/article/mesh/strategy/MeshMajorStrategy.java)

