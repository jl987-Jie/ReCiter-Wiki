# Check how often ReCiter runs

SSH into the server and check the cron tab for the user "reciter" on the server, it will list how often the three jobs are run. 

| Time | Job |
| :--- | :--- |
| 12:00 A.M. | Updates Identity data in MongoDB |
| 1:00 A.M. | Updates PubMed and Scopus articles |
| 7:00 A.M. | Run analysis for all cwids and stores the results of the analysis into MongoDB |





