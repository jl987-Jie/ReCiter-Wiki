# Java class
```Java
@Document(collection = "scopusarticle")
public class ScopusArticle {
	
	private long pubmedId;
	private List<Affiliation> affiliations;
	private List<Author> authors;
...
}
```

# JSON example
```javascript
{ 
    "_id" : ObjectId("57b39ad991348621f4e7a6f2"), 
    "_class" : "reciter.xml.parser.scopus.model.ScopusArticle", 
    "pubmedId" : NumberInt(27220207), 
    "affiliations" : [
        {
            "afid" : NumberInt(60008134), 
            "affilname" : "CNRS Centre National de la Recherche Scientifique", 
            "affiliationCity" : "Paris", 
            "affiliationCountry" : "France"
        }, 
        {
            "afid" : NumberInt(60004708), 
            "affilname" : "amp; Hydrology", 
            "affiliationCity" : "Oxfordshire", 
            "affiliationCountry" : "United Kingdom"
        }, 
        {
            "afid" : NumberInt(60020650), 
            "affilname" : "University of Bristol", 
            "affiliationCity" : "Bristol", 
            "affiliationCountry" : "United Kingdom"
        }, 
        {
            "afid" : NumberInt(60001422), 
            "affilname" : "Universite Pierre et Marie Curie", 
            "affiliationCity" : "Paris", 
            "affiliationCountry" : "France"
        }
    ], 
    "authors" : [
        {
            "seq" : NumberInt(4), 
            "authid" : NumberLong(11840208700), 
            "authname" : "Fontaine C.", 
            "surname" : "Fontaine", 
            "givenName" : "Colin", 
            "initials" : "C.", 
            "afids" : [
                NumberInt(60008134)
            ]
        }, 
        {
            "seq" : NumberInt(1), 
            "authid" : NumberLong(55933711500), 
            "authname" : "Sauve A.", 
            "surname" : "Sauve", 
            "givenName" : "Alix M C", 
            "initials" : "A.M.C.", 
            "afids" : [
                NumberInt(60008134), 
                NumberInt(60020650), 
                NumberInt(60001422)
            ]
        }, 
        {
            "seq" : NumberInt(2), 
            "authid" : NumberLong(6507638847), 
            "authname" : "Thébault E.", 
            "surname" : "Thébault", 
            "givenName" : "Elisa", 
            "initials" : "E.", 
            "afids" : [
                NumberInt(60001422)
            ]
        }, 
        {
            "seq" : NumberInt(3), 
            "authid" : NumberLong(56747629500), 
            "authname" : "Pocock M.", 
            "surname" : "Pocock", 
            "givenName" : "Michael J O", 
            "initials" : "M.J.O.", 
            "afids" : [
                NumberInt(60004708)
            ]
        }
    ]
}
```