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
