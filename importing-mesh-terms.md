This page describes the list of MeSH terms used for grant recommendations. These may be imported into mysql and then transferred to MongoDB. The details of this strategy is in Issue 131 at https://github.com/wcmc-its/ReCiter/issues/131

# Java class
```Java
@Document(collection = "meshterm")
public class MeshTerm {

	private String mesh;
	private long count;
...
}
```

# JSON example
```javascript
{ 
    "_id" : ObjectId("57c1069cc0a13d0ec03cc1d4"), 
    "_class" : "reciter.database.mongo.model.MeshTerm", 
    "mesh" : "(4-(m-Chlorophenylcarbamoyloxy)-2-butynyl)trimethylammonium Chloride", 
    "count" : NumberLong(257)
}
```