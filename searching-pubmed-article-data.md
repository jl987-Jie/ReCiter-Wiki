#Java class

```Java
@Document(collection = "esearchresult")
public class ESearchResult {

	private String cwid;
	private ESearchPmid eSearchPmid;
...
}

public class ESearchPmid {

	private List<Long> pmids;
	private String retrievalStrategyName;
	private LocalDateTime retrievalDate;
...
}
```
# JSON example

```javascript
{ 
    "_id" : ObjectId("57b3956091348618f43c95c6"), 
    "_class" : "reciter.database.mongo.model.ESearchResult", 
    "cwid" : "aas2004", 
    "eSearchPmid" : {
        "pmids" : [
            NumberLong(27374990), 
            NumberLong(27220207), 
            NumberLong(26914314), 
            NumberLong(26574704), 
            NumberLong(3745091)
        ], 
        "retrievalStrategyName" : "FirstNameInitialRetrievalStrategy", 
        "retrievalDate" : ISODate("2016-08-16T22:36:16.778+0000")
    }
}
```