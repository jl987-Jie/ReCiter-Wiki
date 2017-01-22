# Load data about a person into ReCiter

Loading person data into ReCiter is done by the class **Uids** at `src/main/java/reciter/Uids.java`

This class includes a list of UIDs. It goes through these UIDs line by line. It will pull data from LDAP and Oracle and will pull any existing data for these people.

To load data for a person, first ensure that you are connected to the ReCiter database (you may first need to VPN into your institution's network.) Then, add the UID that you want to test into the string array in Uids.java.

Then, open `LdapIdentityController.java`

Start the Spring application (the Tomcat server that will host the ReCiter code) by running `Application.java`

Then point your browser to `http://reciter.med.cornell.edu:8080/reciter/ldap/get/identity/by/uid?uid=nnnnnnn` (Replace nnnnnnn with the desired UID.) This will display the data for the UID formatted as JSON in the browser window. (This is designed for querying.)

If you use the first RequestMapping` URL in `LdapIdentityController.java`, you have to pass the UID as a parameter. This will retrieve data for a single UID.

If you use the second `RequestMapping` URL in `LdapIdentityController.java` it will download the identity information for all the UIDs in that string array. (This is designed for downloading.)

# Query the MongoDB database

To query the ReCiter database
* Open MongoChef.
* Click the "Connect" button and connect to the ReCiter database.
* Click the IntelliShell button.
* In the window that appears, type your query. (A list of queries can be found at ReCiter queries.)
* To execute the query, click the "run query" button (a blue circle with a triangle on it).

# Run ReCiter for an individual

To run ReCiter on your local machine:

1. Launch Eclipse
2. Open a terminal window and navigate to the directory where you installed mongodb. For example:
`cd /Users/myid/large/mongodb-osx-x86_64-3.2.8/bin`
3. Start the database by indicating the path where you have installed the database, using a command like this:
`./mongod --dbpath /Users/myid/databases/mongodb-osx-x86_64-3.2.8/data/db` (replace "/Users/myid/databases/mongodb-osx-x86_64-3.2.8/data/db" with the path to the database on your machine)
4. Change to the mysql directory on your local machine:
`cd /usr/local/mysql/support-files`
5. Start the mysql server:
`./mysql.server start`
5. In Eclipse, launch reciter.controller.application.java as a Java application: `http://localhost:8080/reciter/analysis/by/cwid?cwid=uidhere` (replace "uidhere" with the UID for which you'd like to run analysis).

The RunAnalysis Python file will call the web service that ReCiter is currently servicing on the server. It will run the analysis for all the UIDs in the string array in UIDs.java and will store the data in MongoDB. You can run it by hitting the URL which will imitate what the python script is doing. `http://reciter.med.cornell.edu:8080/reciter/analysis/by/uid?uid=wcb2001`

To see the results run the "get analysis results for a CWID" query in `src/main/resources/mongo_sample_queries/useful_queries.js` in the ReCiter project. There is also the verbose log.

# Add articles to the gold standard for a given UID

This is a query in useful_queries.js. `db.goldstandard.update` to add PMIDs to the gold standard for this UID.

# Remove articles from the gold standard for a given UID

To remove, `db.goldstandard.update` Remove from gold standard for 'cnathan' an erroneous pmid.

# Check performance

The query "find average precision and recall"

# Check how often ReCiter runs

SSH into the server and check the cron tab for the user "reciter" on the server, it will list how often the three jobs are run. One is at 12 a.m., one is at 1 a.m., and the other is at 7 a.m.