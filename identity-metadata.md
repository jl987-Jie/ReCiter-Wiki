# Java class

```java
public class Identity {

	private String cwid; // cwid of the user
	private AuthorName primaryName; // primary name of the user
	private List<AuthorName> alternateNames; // aliases
	private List<String> emails; // list of emails
	private List<KnownRelationship> knownRelationships; // known relationships
	private List<String> departments; // list of department
	private String title; // title of the person
	private List<String> institutions; // institutions
	private Education degreeYear; // degreeYear
	private List<String> personTypes; // types of person: i.e., academic, academic-faculty, etc...
	private String program; // program the person is in.
	private List<String> boardCertifications; // board certifications
	private String citizenship; // citizenship
	private List<String> grants; // grants
	private List<String> keywords; // keywords
	private List<PubMedAlias> pubMedAlias; // name alias from PubMed
	private LocalDateTime dateInitialRun; // the date of the first time that ReCiter perform the retrieval
	private LocalDateTime dateLastRun; // the date of the most recent retrieval
```
# JSON example
```javascript
{ 
    "_id" : "ccole", 
    "_class" : "reciter.database.mongo.model.IdentityMongo", 
    "identity" : {
        "uid" : "ccole", 
        "primaryName" : {
            "firstName" : "Curtis", 
            "firstInitial" : "C", 
            "middleName" : "L", 
            "middleInitial" : "L", 
            "lastName" : "Cole"
        }, 
        "alternateNames" : [
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "L.", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }, 
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "Leland", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }
        ], 
        "emails" : [
            "ccole@med.cornell.edu"
        ], 
        "knownRelationships" : [
            {
                "uid" : "rak2007", 
                "name" : {
                    "firstName" : "Rainu", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Kaushal"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err2004", 
                "name" : {
                    "firstName" : "Elizabeth", 
                    "firstInitial" : "E", 
                    "middleName" : "R", 
                    "middleInitial" : "R", 
                    "lastName" : "Pfoh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sab2028", 
                "name" : {
                    "firstName" : "Samprit", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Banerjee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "huh2009", 
                "name" : {
                    "firstName" : "Richard", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lwetstei", 
                "name" : {
                    "firstName" : "Louis", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Wetstein"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jimperat", 
                "name" : {
                    "firstName" : "Julianne", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Imperato-mcginley"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vit2007", 
                "name" : {
                    "firstName" : "Vicky", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Tiglias"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jtg9003", 
                "name" : {
                    "firstName" : "J. travis", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Gossey"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mey2003", 
                "name" : {
                    "firstName" : "Mary", 
                    "firstInitial" : "M", 
                    "middleName" : "Eleni", 
                    "middleInitial" : "E", 
                    "lastName" : "Yeotsas"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "macallah", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Callahan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err9009", 
                "name" : {
                    "firstName" : "Erika", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Abramson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sam2032", 
                "name" : {
                    "firstName" : "Sameer", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Malhotra"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jruffing", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Ruffing"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jaw2018", 
                "name" : {
                    "firstName" : "Jacob", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Weiser"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "grm2001", 
                "name" : {
                    "firstName" : "Grace", 
                    "firstInitial" : "G", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Migliorisi"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pem2010", 
                "name" : {
                    "firstName" : "Peter", 
                    "firstInitial" : "P", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Michielini"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pas2022", 
                "name" : {
                    "firstName" : "Subroto", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Paul"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sap2026", 
                "name" : {
                    "firstName" : "Samuel", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Prasad"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jyp2001", 
                "name" : {
                    "firstName" : "Jyotishman", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Pathak"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kfischer", 
                "name" : {
                    "firstName" : "Karen", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Fischer"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ame2009", 
                "name" : {
                    "firstName" : "Alison", 
                    "firstInitial" : "A", 
                    "middleName" : "M.", 
                    "middleInitial" : "M", 
                    "lastName" : "Edwards"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lac2021", 
                "name" : {
                    "firstName" : "Lawrence", 
                    "firstInitial" : "L", 
                    "middleName" : "Peter", 
                    "middleInitial" : "P", 
                    "lastName" : "Casalino"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "paa2013", 
                "name" : {
                    "firstName" : "Paul", 
                    "firstInitial" : "P", 
                    "middleName" : "J", 
                    "middleInitial" : "J", 
                    "lastName" : "Albert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "abi2001", 
                "name" : {
                    "firstName" : "Abby", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Isaacs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "adc9001", 
                "name" : {
                    "firstName" : "Adam", 
                    "firstInitial" : "A", 
                    "middleName" : "D", 
                    "middleInitial" : "D", 
                    "lastName" : "Cheriff"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mam2073", 
                "name" : {
                    "firstName" : "Madhu", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mazumdar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nah2005", 
                "name" : {
                    "firstName" : "Nathaniel", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hupert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "joh2020", 
                "name" : {
                    "firstName" : "Josh", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Henninger"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "johnsos", 
                "name" : {
                    "firstName" : "Stephen", 
                    "firstInitial" : "S", 
                    "middleName" : "B.", 
                    "middleInitial" : "B", 
                    "lastName" : "Johnson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mzd2016", 
                "name" : {
                    "firstName" : "Marcos", 
                    "firstInitial" : "M", 
                    "middleName" : "A", 
                    "middleInitial" : "A", 
                    "lastName" : "Davila"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lsb2003", 
                "name" : {
                    "firstName" : "Lidia", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Bernik"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vib9020", 
                "name" : {
                    "firstName" : "Victor", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Brodsky"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kel2011", 
                "name" : {
                    "firstName" : "Kenneth", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Lee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jet2013", 
                "name" : {
                    "firstName" : "Jesse", 
                    "firstInitial" : "J", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Turner"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "aim2001", 
                "name" : {
                    "firstName" : "Alvin", 
                    "firstInitial" : "A", 
                    "middleName" : "I", 
                    "middleInitial" : "I", 
                    "lastName" : "Mushlin"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "all9050", 
                "name" : {
                    "firstName" : "Alex", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Low"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nis2036", 
                "name" : {
                    "firstName" : "Nisha", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Singh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lmk2003", 
                "name" : {
                    "firstName" : "Lisa", 
                    "firstInitial" : "L", 
                    "middleName" : "M", 
                    "middleInitial" : "M", 
                    "lastName" : "Kern"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jam2061", 
                "name" : {
                    "firstName" : "Jayme", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mendelsohn"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jim2012", 
                "name" : {
                    "firstName" : "Jialin", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mao"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "thc2015", 
                "name" : {
                    "firstName" : "Thomas", 
                    "firstInitial" : "T", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Campion"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "maq2004", 
                "name" : {
                    "firstName" : "Maggie", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Qiu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "yob2003", 
                "name" : {
                    "firstName" : "Yolanda", 
                    "firstInitial" : "Y", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Barron-vaya"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "rvd2001", 
                "name" : {
                    "firstName" : "Rina", 
                    "firstInitial" : "R", 
                    "middleName" : "V.", 
                    "middleInitial" : "V", 
                    "lastName" : "Dhopeshwarkar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "weh2009", 
                "name" : {
                    "firstName" : "Wei-chun", 
                    "firstInitial" : "W", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hsu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elb2035", 
                "name" : {
                    "firstName" : "Emma", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Briggs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "meb2001", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Bronnimann"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lur2011", 
                "name" : {
                    "firstName" : "Lucas", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Romero"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jpleonar", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "P", 
                    "middleInitial" : "P", 
                    "lastName" : "Leonard"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "naa2043", 
                "name" : {
                    "firstName" : "Nancy", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Allendorf"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ars2013", 
                "name" : {
                    "firstName" : "Art", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Sedrakyan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elc2013", 
                "name" : {
                    "firstName" : "Eliza", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Chan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "dwd2001", 
                "name" : {
                    "firstName" : "Dan", 
                    "firstInitial" : "D", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Dickinson"
                }, 
                "type" : "co-investigator"
            }
        ], 
        "departments" : [
            "Office of the CIO"
        ], 
        "title" : "Chief Information Officer", 
        "institutions" : [
            "Weill Cornell Medical College, Cornell University", 
            "NewYork-Presbyterian Hospital", 
            "Bowdoin College", 
            "Cornell University Medical College"
        ], 
        "degreeYear" : {
            "bachelorYear" : NumberInt(1986), 
            "doctoralYear" : NumberInt(1994)
        }, 
        "personTypes" : [
            "academic", 
            "academic-faculty", 
            "academic-faculty-weillfulltime", 
            "academic-faculty-associate", 
            "employee-nonacademic", 
            "employee-exempt", 
            "employee", 
            "affiliate", 
            "affiliate-nyp", 
            "affiliate-nyp-weillcampus-credentialed"
        ], 
        "grants" : [
            "FD004494", 
            "HS017029", 
            "RR024996", 
            "RR029822", 
            "TR000457"
        ], 
        "pubMedAlias" : [

        ]
    }
}
```

# Sample Code
### find all identity

```javascript# Java class

```java
public class Identity {

	private String cwid; // cwid of the user
	private AuthorName primaryName; // primary name of the user
	private List<AuthorName> alternateNames; // aliases
	private List<String> emails; // list of emails
	private List<KnownRelationship> knownRelationships; // known relationships
	private List<String> departments; // list of department
	private String title; // title of the person
	private List<String> institutions; // institutions
	private Education degreeYear; // degreeYear
	private List<String> personTypes; // types of person: i.e., academic, academic-faculty, etc...
	private String program; // program the person is in.
	private List<String> boardCertifications; // board certifications
	private String citizenship; // citizenship
	private List<String> grants; // grants
	private List<String> keywords; // keywords
	private List<PubMedAlias> pubMedAlias; // name alias from PubMed
	private LocalDateTime dateInitialRun; // the date of the first time that ReCiter perform the retrieval
	private LocalDateTime dateLastRun; // the date of the most recent retrieval
```
# JSON example
```javascript
{ 
    "_id" : "ccole", 
    "_class" : "reciter.database.mongo.model.IdentityMongo", 
    "identity" : {
        "uid" : "ccole", 
        "primaryName" : {
            "firstName" : "Curtis", 
            "firstInitial" : "C", 
            "middleName" : "L", 
            "middleInitial" : "L", 
            "lastName" : "Cole"
        }, 
        "alternateNames" : [
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "L.", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }, 
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "Leland", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }
        ], 
        "emails" : [
            "ccole@med.cornell.edu"
        ], 
        "knownRelationships" : [
            {
                "uid" : "rak2007", 
                "name" : {
                    "firstName" : "Rainu", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Kaushal"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err2004", 
                "name" : {
                    "firstName" : "Elizabeth", 
                    "firstInitial" : "E", 
                    "middleName" : "R", 
                    "middleInitial" : "R", 
                    "lastName" : "Pfoh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sab2028", 
                "name" : {
                    "firstName" : "Samprit", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Banerjee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "huh2009", 
                "name" : {
                    "firstName" : "Richard", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lwetstei", 
                "name" : {
                    "firstName" : "Louis", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Wetstein"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jimperat", 
                "name" : {
                    "firstName" : "Julianne", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Imperato-mcginley"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vit2007", 
                "name" : {
                    "firstName" : "Vicky", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Tiglias"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jtg9003", 
                "name" : {
                    "firstName" : "J. travis", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Gossey"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mey2003", 
                "name" : {
                    "firstName" : "Mary", 
                    "firstInitial" : "M", 
                    "middleName" : "Eleni", 
                    "middleInitial" : "E", 
                    "lastName" : "Yeotsas"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "macallah", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Callahan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err9009", 
                "name" : {
                    "firstName" : "Erika", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Abramson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sam2032", 
                "name" : {
                    "firstName" : "Sameer", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Malhotra"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jruffing", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Ruffing"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jaw2018", 
                "name" : {
                    "firstName" : "Jacob", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Weiser"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "grm2001", 
                "name" : {
                    "firstName" : "Grace", 
                    "firstInitial" : "G", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Migliorisi"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pem2010", 
                "name" : {
                    "firstName" : "Peter", 
                    "firstInitial" : "P", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Michielini"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pas2022", 
                "name" : {
                    "firstName" : "Subroto", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Paul"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sap2026", 
                "name" : {
                    "firstName" : "Samuel", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Prasad"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jyp2001", 
                "name" : {
                    "firstName" : "Jyotishman", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Pathak"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kfischer", 
                "name" : {
                    "firstName" : "Karen", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Fischer"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ame2009", 
                "name" : {
                    "firstName" : "Alison", 
                    "firstInitial" : "A", 
                    "middleName" : "M.", 
                    "middleInitial" : "M", 
                    "lastName" : "Edwards"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lac2021", 
                "name" : {
                    "firstName" : "Lawrence", 
                    "firstInitial" : "L", 
                    "middleName" : "Peter", 
                    "middleInitial" : "P", 
                    "lastName" : "Casalino"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "paa2013", 
                "name" : {
                    "firstName" : "Paul", 
                    "firstInitial" : "P", 
                    "middleName" : "J", 
                    "middleInitial" : "J", 
                    "lastName" : "Albert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "abi2001", 
                "name" : {
                    "firstName" : "Abby", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Isaacs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "adc9001", 
                "name" : {
                    "firstName" : "Adam", 
                    "firstInitial" : "A", 
                    "middleName" : "D", 
                    "middleInitial" : "D", 
                    "lastName" : "Cheriff"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mam2073", 
                "name" : {
                    "firstName" : "Madhu", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mazumdar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nah2005", 
                "name" : {
                    "firstName" : "Nathaniel", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hupert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "joh2020", 
                "name" : {
                    "firstName" : "Josh", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Henninger"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "johnsos", 
                "name" : {
                    "firstName" : "Stephen", 
                    "firstInitial" : "S", 
                    "middleName" : "B.", 
                    "middleInitial" : "B", 
                    "lastName" : "Johnson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mzd2016", 
                "name" : {
                    "firstName" : "Marcos", 
                    "firstInitial" : "M", 
                    "middleName" : "A", 
                    "middleInitial" : "A", 
                    "lastName" : "Davila"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lsb2003", 
                "name" : {
                    "firstName" : "Lidia", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Bernik"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vib9020", 
                "name" : {
                    "firstName" : "Victor", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Brodsky"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kel2011", 
                "name" : {
                    "firstName" : "Kenneth", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Lee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jet2013", 
                "name" : {
                    "firstName" : "Jesse", 
                    "firstInitial" : "J", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Turner"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "aim2001", 
                "name" : {
                    "firstName" : "Alvin", 
                    "firstInitial" : "A", 
                    "middleName" : "I", 
                    "middleInitial" : "I", 
                    "lastName" : "Mushlin"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "all9050", 
                "name" : {
                    "firstName" : "Alex", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Low"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nis2036", 
                "name" : {
                    "firstName" : "Nisha", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Singh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lmk2003", 
                "name" : {
                    "firstName" : "Lisa", 
                    "firstInitial" : "L", 
                    "middleName" : "M", 
                    "middleInitial" : "M", 
                    "lastName" : "Kern"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jam2061", 
                "name" : {
                    "firstName" : "Jayme", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mendelsohn"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jim2012", 
                "name" : {
                    "firstName" : "Jialin", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mao"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "thc2015", 
                "name" : {
                    "firstName" : "Thomas", 
                    "firstInitial" : "T", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Campion"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "maq2004", 
                "name" : {
                    "firstName" : "Maggie", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Qiu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "yob2003", 
                "name" : {
                    "firstName" : "Yolanda", 
                    "firstInitial" : "Y", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Barron-vaya"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "rvd2001", 
                "name" : {
                    "firstName" : "Rina", 
                    "firstInitial" : "R", 
                    "middleName" : "V.", 
                    "middleInitial" : "V", 
                    "lastName" : "Dhopeshwarkar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "weh2009", 
                "name" : {
                    "firstName" : "Wei-chun", 
                    "firstInitial" : "W", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hsu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elb2035", 
                "name" : {
                    "firstName" : "Emma", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Briggs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "meb2001", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Bronnimann"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lur2011", 
                "name" : {
                    "firstName" : "Lucas", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Romero"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jpleonar", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "P", 
                    "middleInitial" : "P", 
                    "lastName" : "Leonard"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "naa2043", 
                "name" : {
                    "firstName" : "Nancy", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Allendorf"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ars2013", 
                "name" : {
                    "firstName" : "Art", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Sedrakyan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elc2013", 
                "name" : {
                    "firstName" : "Eliza", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Chan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "dwd2001", 
                "name" : {
                    "firstName" : "Dan", 
                    "firstInitial" : "D", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Dickinson"
                }, 
                "type" : "co-investigator"
            }
        ], 
        "departments" : [
            "Office of the CIO"
        ], 
        "title" : "Chief Information Officer", 
        "institutions" : [
            "Weill Cornell Medical College, Cornell University", 
            "NewYork-Presbyterian Hospital", 
            "Bowdoin College", 
            "Cornell University Medical College"
        ], 
        "degreeYear" : {
            "bachelorYear" : NumberInt(1986), 
            "doctoralYear" : NumberInt(1994)
        }, 
        "personTypes" : [
            "academic", 
            "academic-faculty", 
            "academic-faculty-weillfulltime", 
            "academic-faculty-associate", 
            "employee-nonacademic", 
            "employee-exempt", 
            "employee", 
            "affiliate", 
            "affiliate-nyp", 
            "affiliate-nyp-weillcampus-credentialed"
        ], 
        "grants" : [
            "FD004494", 
            "HS017029", 
            "RR024996", 
            "RR029822", 
            "TR000457"
        ], 
        "pubMedAlias" : [

        ]
    }
}
```

# Sample Code
### find all identity

```javascript
db.identity.find();
```

### find a single identity
```javascript
db.identity.find({"cwid": "jil3004"});
```

### insert an identity
```javascript
db.identity.insert({
"cwid": "jil3004", 
"authorName": 
{
	"firstName": "Jie",
	"firstInitial": "J",
	"middleName": "",
  	"middleInitial": "",
  	"lastName": "Lin"
},
"email": [
	"jil3004@med.cornell.edu"
]  	
});
```

### deleting an identity
```javascript
db.identity.deleteOne({"cwid": "jil3004"});
```

### updating an identity
```javascript
db.identity.update(
	{"cwid": "jil3004"}, 
	{
	  $set: {
	    email: ["jie265@gmail.com"]
	  }
	}
);
```# Java class

```java
public class Identity {

	private String cwid; // cwid of the user
	private AuthorName primaryName; // primary name of the user
	private List<AuthorName> alternateNames; // aliases
	private List<String> emails; // list of emails
	private List<KnownRelationship> knownRelationships; // known relationships
	private List<String> departments; // list of department
	private String title; // title of the person
	private List<String> institutions; // institutions
	private Education degreeYear; // degreeYear
	private List<String> personTypes; // types of person: i.e., academic, academic-faculty, etc...
	private String program; // program the person is in.
	private List<String> boardCertifications; // board certifications
	private String citizenship; // citizenship
	private List<String> grants; // grants
	private List<String> keywords; // keywords
	private List<PubMedAlias> pubMedAlias; // name alias from PubMed
	private LocalDateTime dateInitialRun; // the date of the first time that ReCiter perform the retrieval
	private LocalDateTime dateLastRun; // the date of the most recent retrieval
```
# JSON example
```javascript
{ 
    "_id" : "ccole", 
    "_class" : "reciter.database.mongo.model.IdentityMongo", 
    "identity" : {
        "uid" : "ccole", 
        "primaryName" : {
            "firstName" : "Curtis", 
            "firstInitial" : "C", 
            "middleName" : "L", 
            "middleInitial" : "L", 
            "lastName" : "Cole"
        }, 
        "alternateNames" : [
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "L.", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }, 
            {
                "firstName" : "Curtis", 
                "firstInitial" : "C", 
                "middleName" : "Leland", 
                "middleInitial" : "L", 
                "lastName" : "Cole"
            }
        ], 
        "emails" : [
            "ccole@med.cornell.edu"
        ], 
        "knownRelationships" : [
            {
                "uid" : "rak2007", 
                "name" : {
                    "firstName" : "Rainu", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Kaushal"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err2004", 
                "name" : {
                    "firstName" : "Elizabeth", 
                    "firstInitial" : "E", 
                    "middleName" : "R", 
                    "middleInitial" : "R", 
                    "lastName" : "Pfoh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sab2028", 
                "name" : {
                    "firstName" : "Samprit", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Banerjee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "huh2009", 
                "name" : {
                    "firstName" : "Richard", 
                    "firstInitial" : "R", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lwetstei", 
                "name" : {
                    "firstName" : "Louis", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Wetstein"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jimperat", 
                "name" : {
                    "firstName" : "Julianne", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Imperato-mcginley"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vit2007", 
                "name" : {
                    "firstName" : "Vicky", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Tiglias"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jtg9003", 
                "name" : {
                    "firstName" : "J. travis", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Gossey"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mey2003", 
                "name" : {
                    "firstName" : "Mary", 
                    "firstInitial" : "M", 
                    "middleName" : "Eleni", 
                    "middleInitial" : "E", 
                    "lastName" : "Yeotsas"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "macallah", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Callahan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "err9009", 
                "name" : {
                    "firstName" : "Erika", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Abramson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sam2032", 
                "name" : {
                    "firstName" : "Sameer", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Malhotra"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jruffing", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Ruffing"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jaw2018", 
                "name" : {
                    "firstName" : "Jacob", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Weiser"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "grm2001", 
                "name" : {
                    "firstName" : "Grace", 
                    "firstInitial" : "G", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Migliorisi"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pem2010", 
                "name" : {
                    "firstName" : "Peter", 
                    "firstInitial" : "P", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Michielini"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "pas2022", 
                "name" : {
                    "firstName" : "Subroto", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Paul"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "sap2026", 
                "name" : {
                    "firstName" : "Samuel", 
                    "firstInitial" : "S", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Prasad"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jyp2001", 
                "name" : {
                    "firstName" : "Jyotishman", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Pathak"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kfischer", 
                "name" : {
                    "firstName" : "Karen", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Fischer"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ame2009", 
                "name" : {
                    "firstName" : "Alison", 
                    "firstInitial" : "A", 
                    "middleName" : "M.", 
                    "middleInitial" : "M", 
                    "lastName" : "Edwards"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lac2021", 
                "name" : {
                    "firstName" : "Lawrence", 
                    "firstInitial" : "L", 
                    "middleName" : "Peter", 
                    "middleInitial" : "P", 
                    "lastName" : "Casalino"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "paa2013", 
                "name" : {
                    "firstName" : "Paul", 
                    "firstInitial" : "P", 
                    "middleName" : "J", 
                    "middleInitial" : "J", 
                    "lastName" : "Albert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "abi2001", 
                "name" : {
                    "firstName" : "Abby", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Isaacs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "adc9001", 
                "name" : {
                    "firstName" : "Adam", 
                    "firstInitial" : "A", 
                    "middleName" : "D", 
                    "middleInitial" : "D", 
                    "lastName" : "Cheriff"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mam2073", 
                "name" : {
                    "firstName" : "Madhu", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mazumdar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nah2005", 
                "name" : {
                    "firstName" : "Nathaniel", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hupert"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "joh2020", 
                "name" : {
                    "firstName" : "Josh", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Henninger"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "johnsos", 
                "name" : {
                    "firstName" : "Stephen", 
                    "firstInitial" : "S", 
                    "middleName" : "B.", 
                    "middleInitial" : "B", 
                    "lastName" : "Johnson"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "mzd2016", 
                "name" : {
                    "firstName" : "Marcos", 
                    "firstInitial" : "M", 
                    "middleName" : "A", 
                    "middleInitial" : "A", 
                    "lastName" : "Davila"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lsb2003", 
                "name" : {
                    "firstName" : "Lidia", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Bernik"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "vib9020", 
                "name" : {
                    "firstName" : "Victor", 
                    "firstInitial" : "V", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Brodsky"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "kel2011", 
                "name" : {
                    "firstName" : "Kenneth", 
                    "firstInitial" : "K", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Lee"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jet2013", 
                "name" : {
                    "firstName" : "Jesse", 
                    "firstInitial" : "J", 
                    "middleName" : "C", 
                    "middleInitial" : "C", 
                    "lastName" : "Turner"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "aim2001", 
                "name" : {
                    "firstName" : "Alvin", 
                    "firstInitial" : "A", 
                    "middleName" : "I", 
                    "middleInitial" : "I", 
                    "lastName" : "Mushlin"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "all9050", 
                "name" : {
                    "firstName" : "Alex", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Low"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "nis2036", 
                "name" : {
                    "firstName" : "Nisha", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Singh"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lmk2003", 
                "name" : {
                    "firstName" : "Lisa", 
                    "firstInitial" : "L", 
                    "middleName" : "M", 
                    "middleInitial" : "M", 
                    "lastName" : "Kern"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jam2061", 
                "name" : {
                    "firstName" : "Jayme", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mendelsohn"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jim2012", 
                "name" : {
                    "firstName" : "Jialin", 
                    "firstInitial" : "J", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Mao"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "thc2015", 
                "name" : {
                    "firstName" : "Thomas", 
                    "firstInitial" : "T", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Campion"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "maq2004", 
                "name" : {
                    "firstName" : "Maggie", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Qiu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "yob2003", 
                "name" : {
                    "firstName" : "Yolanda", 
                    "firstInitial" : "Y", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Barron-vaya"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "rvd2001", 
                "name" : {
                    "firstName" : "Rina", 
                    "firstInitial" : "R", 
                    "middleName" : "V.", 
                    "middleInitial" : "V", 
                    "lastName" : "Dhopeshwarkar"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "weh2009", 
                "name" : {
                    "firstName" : "Wei-chun", 
                    "firstInitial" : "W", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Hsu"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elb2035", 
                "name" : {
                    "firstName" : "Emma", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Briggs"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "meb2001", 
                "name" : {
                    "firstName" : "Mark", 
                    "firstInitial" : "M", 
                    "middleName" : "", 
                    "middleIniial" : "", 
                    "lastName" : "Bronnimann"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "lur2011", 
                "name" : {
                    "firstName" : "Lucas", 
                    "firstInitial" : "L", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Romero"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "jpleonar", 
                "name" : {
                    "firstName" : "John", 
                    "firstInitial" : "J", 
                    "middleName" : "P", 
                    "middleInitial" : "P", 
                    "lastName" : "Leonard"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "naa2043", 
                "name" : {
                    "firstName" : "Nancy", 
                    "firstInitial" : "N", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Allendorf"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "ars2013", 
                "name" : {
                    "firstName" : "Art", 
                    "firstInitial" : "A", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Sedrakyan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "elc2013", 
                "name" : {
                    "firstName" : "Eliza", 
                    "firstInitial" : "E", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Chan"
                }, 
                "type" : "co-investigator"
            }, 
            {
                "uid" : "dwd2001", 
                "name" : {
                    "firstName" : "Dan", 
                    "firstInitial" : "D", 
                    "middleName" : "", 
                    "middleInitial" : "", 
                    "lastName" : "Dickinson"
                }, 
                "type" : "co-investigator"
            }
        ], 
        "departments" : [
            "Office of the CIO"
        ], 
        "title" : "Chief Information Officer", 
        "institutions" : [
            "Weill Cornell Medical College, Cornell University", 
            "NewYork-Presbyterian Hospital", 
            "Bowdoin College", 
            "Cornell University Medical College"
        ], 
        "degreeYear" : {
            "bachelorYear" : NumberInt(1986), 
            "doctoralYear" : NumberInt(1994)
        }, 
        "personTypes" : [
            "academic", 
            "academic-faculty", 
            "academic-faculty-weillfulltime", 
            "academic-faculty-associate", 
            "employee-nonacademic", 
            "employee-exempt", 
            "employee", 
            "affiliate", 
            "affiliate-nyp", 
            "affiliate-nyp-weillcampus-credentialed"
        ], 
        "grants" : [
            "FD004494", 
            "HS017029", 
            "RR024996", 
            "RR029822", 
            "TR000457"
        ], 
        "pubMedAlias" : [

        ]
    }
}
```

# Sample Code
### find all identity

```javascript
db.identity.find();
```

### find a single identity
```javascript
db.identity.find({"cwid": "jil3004"});
```

### insert an identity
```javascript
db.identity.insert({
"cwid": "jil3004", 
"authorName": 
{
	"firstName": "Jie",
	"firstInitial": "J",
	"middleName": "",
  	"middleInitial": "",
  	"lastName": "Lin"
},
"email": [
	"jil3004@med.cornell.edu"
]  	
});
```

### deleting an identity
```javascript
db.identity.deleteOne({"cwid": "jil3004"});
```

### updating an identity
```javascript
db.identity.update(
	{"cwid": "jil3004"}, 
	{
	  $set: {
	    email: ["jie265@gmail.com"]
	  }
	}
);
```
db.identity.find();
```

### find a single identity
```javascript
db.identity.find({"cwid": "jil3004"});
```

### insert an identity
```javascript
db.identity.insert({
"cwid": "jil3004", 
"authorName": 
{
	"firstName": "Jie",
	"firstInitial": "J",
	"middleName": "",
  	"middleInitial": "",
  	"lastName": "Lin"
},
"email": [
	"jil3004@med.cornell.edu"
]  	
});
```

### deleting an identity
```javascript
db.identity.deleteOne({"cwid": "jil3004"});
```

### updating an identity
```javascript
db.identity.update(
	{"cwid": "jil3004"}, 
	{
	  $set: {
	    email: ["jie265@gmail.com"]
	  }
	}
);
```