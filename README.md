## **What is ReCiter?**

ReCiter is an algorithm and web service for making highly accurate assertions about author identity in publication metadata. It may be used to keep author publication lists accurate and up-to-date.

## **Why should my institution use ReCiter?**

ReCiter rapidly and accurately identifies articles by specific authors. It does this by combining publication data from PubMed \(and, optionally, Scopus\) with data you provide about your institution's own authors.

With the more complete and efficient searches that result from combining these types of data, you can save time and your institution can be more productive.

ReCiter's accuracy has been measured at over 95% for current full-time faculty at Weill Cornell Medicine.

## A use case:

**You wish to search for articles by Andrew Schwartz \(not his real name!\) who currently works at Harvard, but used to work at Union County Community College.**

* The PubMed interface will retrieve over 3,500 results when searching for "A Schwartz" as an author.
* **Most of these are not authored by the A. Schwartz we are looking for!**
  * It will show results for all people who are named "A. Schwartz".  
  * You _could_ filter the search by Harvard University, but then would have to search again for papers written when A. Schwartz was at other institutions.  
  * You would also _have to research A. Schwartz_ \(e.g., using LinkedIn and Google Scholar\) to identify those past affiliations.

The ReCiter system can handle that search for you in one go, quickly and accurately.

## **How can my institution use ReCiter?**

We support two methods of working with ReCiter:

* **stand-alone**, for users only, and
* **with Eclipse IDE** for those who want to help develop ReCiter or read its source code.

ReCiter is an open source application stack. Currently, institutions wishing to use ReCiter need to install a local copy. Your staff will need to install the application and database, then populate your local database with data about your authors.

## **What technologies are used in ReCiter?**

* ReCiter stores data about researchers and publications in **MongoDB**.
* Its main computation logic is written in **Java**.
* It employs the **Spring Framework**, a Java-based application framework designed to manage RESTful web services and server requests.

## **What data sources are used by ReCiter for computation?**

* **PubMed** search engine, which primarily accesses the **Medline** database
* **Scopus** \(optional\), a bibliographic database used to harvest affiliations. Using Scopus data is especially useful in cases where affiliation data is not present in the PubMed record.
* Institution-specific data.

## What data about authors does ReCiter use?

* name variants \(such as nicknames, name changes, and spelling irregularities\) 
* current and former institutional affiliations and departments
* e-mail addresses
* years of graduation
* collaborators
* journal publication patterns

## **What are the system requirements?**

## **How do I use ReCiter?**

You'll need to install Java, Maven, and MongoDB on a server; get a copy of the source code; import data into MongoDB; and start the Spring Boot application.

## **How accurate is ReCiter?**

Accuracy depends on the amount of data available to ReCiter. Certain types of data have greater disambiguation power than others. Data on ReCiter's accuracy at Weill Cornell is available at [https://figshare.com/articles/Update\_on\_ReCiter\_Author\_Disambiguation\_Engine/3750003](https://figshare.com/articles/Update_on_ReCiter_Author_Disambiguation_Engine/3750003).

## Who has access to the data?

* Data from PubMed about published articles is already publicly available.
* Each institution can set its own access rules for personnel information that is used by ReCiter to perform its searches.
* ReCiter will only run for authors whose data you have populated into ReCiter.

## **Who do I contact for help with ReCiter?**

## **How do I cite ReCiter?**



