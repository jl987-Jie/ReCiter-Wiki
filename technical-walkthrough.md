![](/assets/ReCiter Architecture.png)
Please note that use of Scopus is optional. In one experiment, we found that using Scopus data improved algorithm recall by approximately 5% and precision by 0.2%, when compared against using PubMed data alone.

1. Scopus, PubMed articles and person specific data are retrieved and stored into MongoDB on a recurrent basis.
2. Web interface interacts with REST api exposed by ReCiter.
3. ReCiter outputs analysis do MongoDB on a recurrent basis.

## Components of ReCiter
The code for ReCiter consists of four main parts: database storage utilities, PubMed retriever and parser, Scopus retriever and parser, and ReCiter algorithm.

## Pseudocode
Target individuals are extracted from institutional databases. For each target from a given list, publications are retrieved from a given publication source, sorted and partitioned into groups with different purported authorship. The publications ultimately assigned to each target individual are contained in the attribution group that best matches the characteristics of the target.

1. Append publication data from scholarly databases (Scopus and Medline) to local institutional database
2. Select target individuals from local database with accompanying descriptive information. 
3. Identify articles for each target individual:
  1. Retrieve a publication set for a given target from the local database.
  2. Sort the publication set according to completeness of target name and citation content. 
  3. Partition the publication set into attribution groups (identities), such that each group is likely to share the same author, as follows: For each publication in the publication set:
    1. Choose candidate groups out of all the attribution groups already formed.
    2. Select the attribution group that best matches the given publication (if any).
    3. Add the publication to the attribution group (or start a new group).
    4. Select the attribution group that is the best match for the given target.