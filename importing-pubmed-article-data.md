#Java class

To view a full list of the attributes that are represented in a PubMed article object, please refer to src/main/java/reciter/model/pubmed/PubMedArticle.java.

```java
@Document(collection = "pubmedarticle")
public class PubMedArticle {
	
	private MedlineCitation medlineCitation;
	private PubMedData pubMedData;
...
}

public class MedlineCitation {
	
	private enum MedlineCitationOwner {
		NLM,
		NASA,
		PIP,
		KIE,
		HSR,
		HMD,
		SIS,
		NOTNLM
	}
	
	private enum MedlineCitationStatus {
		COMPLETED,
		IN_PROCESS,
		PUBMED_NOT_MEDLINE,
		IN_DATA_REVIEW,
		PUBLISHER,
		MEDLINE,
		OLDMEDLINE
	}
	
	private MedlineCitationPMID medlineCitationPMID;
	private MedlineCitationOwner medlineCitationOwner;
	private MedlineCitationStatus medlineCitationStatus;
	private MedlineCitationVersionDate medlineCitationVersionDate;
	private MedlineCitationVersionID medlineCitationVersionID;
	
	private MedlineCitationDate dateCreated;
	private MedlineCitationDate dateCompleted;
	private MedlineCitationDate dateRevised;
	
	private MedlineCitationArticle article;
	private List<MedlineCitationMeshHeading> meshHeadingList;
	private MedlineCitationKeywordList keywordList;
	private List<MedlineCitationCommentsCorrections> commentsCorrectionsList;
...
}

public class MedlineCitationPMID {

	private final long pmid;
	private String version;
...
}
```

# JSON example
```javascript
{ 
    "_id" : ObjectId("57b3c909febe6a1d38795039"), 
    "_class" : "reciter.model.pubmed.PubMedArticle", 
    "medlineCitation" : {
        "medlineCitationPMID" : {
            "pmid" : NumberLong(18751071)
        }, 
        "article" : {
            "journal" : {
                "journalIssue" : {
                    "pubDate" : {
                        "year" : "1997"
                    }
                }, 
                "title" : "The Western journal of medicine", 
                "isoAbbreviation" : "West. J. Med."
            }, 
            "articleTitle" : "Poem: the disease.", 
            "authorList" : [
                {
                    "lastName" : "Marcus", 
                    "foreName" : "A", 
                    "initials" : "A"
                }
            ]
        }
    }
}
```