## \#\# What is ReCiter?

## ReCiter is an algorithm and web service for making highly accurate assertions about author identity in publication metadata. It is designed with institutions in mind so that they can maintain author publication lists accurate and up-to-date for thousands of people. ReCiter is optimized for disambiguating authorship in PubMed and, optionally, Scopus.

## 

## \#\# Would ReCiter be useful at my institution?

## ReCiter rapidly and accurately identifies articles by specific authors, including those at previous affiliations. It does this by leveraging institutionally maintained identity data \(e.g., departments, relationships, email addresses, year of degree, etc.\). As you can read about it in the \[algorithm documentation\]\(Algorithm\), ReCiter is designed to mimic well-informed human judgment. For example:

## \* Dr. Y is more likely to have written this article. It lists his department in the author affiliation field.

## \* Dr. X couldn't have written this article. It was published eight years before she got her Bachelor's degree.

## \* Dr. Z is more likely to have written this article. It lists two authors who are also included as co-investigators on an active grant.

## 

## With the more complete and efficient searches that result from combining these types of data, you can save time and your institution can be more productive. If you run ReCiter daily, you can ensure that the desired users are the first to learn when a new publication has hit PubMed.

## 

## \#\# A use case

## 

## The Department of Pediatrics tells you that the institution is about to hire a new hot-shot faculty member from Harvard, Dr. Andrew Schwartz, and wants to have an updated list of publications right away. 

## 

## \* You reach out to the department, Dr. Schwartz, Office of Faculty Affairs, etc. requesting a CV, but no one gets back to you. You'll have to do this on your own.

## \* The PubMed interface retrieves over 3,500 results when searching for "A Schwartz" as an author.

## \* We can assume that most of these candidate publications are not authored by the "A Schwartz" we are looking for! Even the ones with a Harvard affiliation may be written by another A. Schwartz.

## \* You search for a LinkedIn, Google Scholar, Academia.edu, ORCID or other such profile - any one of these could be incomplete - and find a handful of publications.

## \* You look through the candidate articles for clues. What's the institutional affiliation? What department is listed in the affiliation string? Is a known institutional email listed? Are there any grants indexed on which A. Schwartz was listed as a co-author.

## \* You're feeling especially attentive to detail, so you look at see if certain journals or co-authors names from a known publication \(where Dr. Schwartz's email is indexed\), are shared with other candidate publications. 

## \* This isn't your first rodeo, so you complete this work in about 20 minutes. Good for you!

## 

## Properly populated with identity data, the ReCiter system can handle all this for you in one go, quickly and accurately. Furthermore, if it's set up to work automatically on a daily basis, you can do this every day, for thousands of people. At Weill Cornell Medicine, we use ReCiter for all full-time faculty \(n=1700\) and PhD/MD-PhD students \(n=650\). We are looking to expand its use for PhD alumni, among others.

## 

## \#\# How can my institution use ReCiter?

## We support two methods of working with ReCiter:

## 

## \* \*\*stand-alone\*\*, for users only, and

## \* \*\*with Eclipse IDE\*\* for those who want to help develop ReCiter or read its source code.

## 

## ReCiter is an open source application stack. Currently, institutions wishing to use ReCiter need to install a local copy. Your staff will need to install the application and database, then populate your local database with data about your authors.

## 

## \#\# What technologies are used in ReCiter?

## \* ReCiter stores data about researchers and publications in \*\*MongoDB\*\*.

## \* Its main computation logic is written in \*\*Java\*\*.

## \* It employs the \*\*Spring Framework\*\*, a Java-based application framework designed to manage RESTful web services and server requests.

## 

## \#\# What data sources are used by ReCiter for computation?

## \* \*\*Institution-specific identity data\*\* including emails, names, known relationships, grant IDs, departmental affiliations, etc.

## \* \*\*PubMed\*\* search engine, which primarily accesses the \*\*Medline\*\* database

## \* \*\*Scopus\*\* \(optional\), a bibliographic database used to harvest affiliations. 

## 

## \#\# How important is it to use Scopus?

## 

## Use of Scopus, which depends on a standard license, is optional but helpful. In one experiment, we found that using Scopus data improved algorithm recall by approximately 5% and precision by 0.2%, when compared against using PubMed data alone.

## 

## Using Scopus data tends to be more useful in cases where affiliation data is not present in the PubMed record or the full name of authors isn't indexed. This is more common in older papers. For that reason, Scopus may offer less of an advantage for more recently published papers.

## 

## So long as it's okay with your license, it would be possible to use alternatives to Scopus such as Web of Science. Of course, you would need to figure out how to parse these records, among other things.

## 

## Note that Scopus is only used as a compliment to PubMed. In other words, ReCiter only uses identifiers \(PMID, DOI\) to find additional data \(namely affiliation and full name\) about a candidate article.

## 

## \#\# What institutional data about authors does ReCiter use? 

## \* name variants \(such as nicknames, name changes, and spelling irregularities\) 

## \* current and former institutional affiliations

## \* departmental affiliation

## \* e-mail addresses \(personal, institutional, etc.\)

## \* years of degree \(bachelor and any terminal degree\)

## \* relationships  \(co-investigatorships, mentor/mentee, people in shared organizational unit\)

## \* common institutional affiliations \(used for everyone\)

## \* individual institutions \(e.g., undergraduate, doctoral, residency, internship, clinical affiliation; used to limit results when someone has an especially common name\)

## 

## \#\# What are the system requirements?

## 

## \#\#\# Running ReCiter on a server&lt;br&gt;

## ReCiter will run on Linux, Mac OS X, and Windows versions 7 and higher. A minimum of 4GB of RAM is required; 16GB of RAM are recommended. An Internet connection is required to download article data from scholarly databases.

## 

## \#\#\# Running ReCiter on a local machine&lt;br&gt;

## ReCiter's API may be run in a browser on any modern machine. The ReCiter server must be accessible to the local machine via a local area network or internet connection. 

## 

## \#\# How do I use ReCiter?

## 

## You'll need to install Java, Maven, and MongoDB on a server; get a copy of the source code; import data into MongoDB; and start the Spring Boot application.

## 

## \#\# How accurate is ReCiter?

## ReCiter's accuracy \(an average of precision and recall as benchmarked against a human-defined gold standard\) has been measured at over 95% for current full-time faculty at Weill Cornell Medicine. The exact accuracy of a given person depends on a variety of factors, especially:

## \* How much identity data you can provide the ReCiter algorithm 

## \* How common a person's name is

## \* How prolific an author has been 

## 

## For example, ReCiter would typically perform far better for a long-time faculty with a unique name and a lot of publications under his belt as opposed to a student with a common name and only a couple publications. Knowing the email a faculty used at a prior affiliation \(your Office of Faculty Affairs has this, at least at Weill Cornell\) is a huge help.

## 

## ReCiter will never be 100% accurate. We are in the process of building an interface to give users an opportunity to provide feedback. This feedback \(accepts and rejects\) will be fed back into ReCiter and used to further tune ReCiter's judgments.

## 

## Data on ReCiter's accuracy at Weill Cornell is available at https://figshare.com/articles/Update\_on\_ReCiter\_Author\_Disambiguation\_Engine/3750003.

## 

## \#\# Who has access to the data?

## \* Data from PubMed about published articles is already publicly available.

## \* Each institution can set its own access rules for personnel information that is used by ReCiter to perform its searches.

## \* ReCiter will only run for authors whose data you have populated into ReCiter.

## 

## \#\# What about ORCID?

## ORCID is a persistent digital identifier designed to distinguish one researcher from every other researcher. Users create an account at orcid.org and manually claim their publications. A handful of publishers now require that submitters include their ORCID ID, and there are efforts by institutions, especially libraries, to increase adoption. 

## 

## Some issues we have noticed with ORCID:

## \* There are a number of duplicate ORCID profiles. 

## \* The False Negative Problem: A new candidate publication appeared three months ago. Is it not in the person's ORCID profile because he didn't get around to adding it, or because he simply didn't author it?... Our administrators like to be "in the know." Ideally, we would tell them of a new authorship the day it was indexed in PubMed, so this poses a problem.

## \* Our users are notoriously overwhelmed. Absent any significant carrot or stick, getting them to maintain a profile in yet another system is an exercise in frustration. It seems trivial, but even getting them to assign the library as delegates would likewise require a lot of persistence.

## \* For reporting purposes, we attempt to track publications authored by users that we can no longer contact and would have trouble encouraging them to clean up their ORCID profile. This includes publications by alumni and inactive faculty. These are individuals who would never give us proxy access to their ORCID profiles.

## 

## For these reasons, ORCID is not quite mature enough for Weill Cornell Medicine to be able to count on it as a reliable source of truth for author identity. If and when that changes, and it starts to become a valuable source of data, ReCiter could be modified to also include ORCID's assertions of authorship.

## 

## \#\# Whom do I contact for help with ReCiter?

## 

## Please email Michael Bales at meb7002@med.cornell.edu or Paul Albert at paa2013@med.cornell.edu.

## 

## \#\# How do I cite ReCiter?

## 

## The original ReCiter algorithm may be cited as follows:&lt;br&gt;

## &lt;br&gt;

## Johnson SB, Bales ME, Dine D, Bakken S, Albert PJ, Weng C. Automatic generation of investigator bibliographies for institutional research networking systems. Journal of Biomedical Informatics 2014;51:8–14. Available from URL: http://dx.doi.org/10.1016/j.jbi.2014.03.013



