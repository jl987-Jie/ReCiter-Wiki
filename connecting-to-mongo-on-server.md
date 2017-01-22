In order to connect to the Mongo Server on reciter.med.cornell.edu, please follow the below steps.

1. Install MongoChef http://3t.io/mongochef/
2. VPN into Weill Cornell network.
3. Once it's installed, open MongoChef and go to 'File' -> 'Connect' -> 'New Connection'
4. Edit 'Server' tab as follows:
![](/assets/d93b43a0-8d73-11e6-8dd5-64dc0e4acc03.PNG)
5. Edit 'Authentication' tab as follows:
![](/assets/16deca9c-8d74-11e6-9453-0f7b1f915ba4.PNG)
6. Edit 'SSH Tunnel' tab as follows: (Replace 'SSH User name' with your UNIX username)
![](/assets/4cff2b9e-8d74-11e6-83db-ebf7409cec8c.PNG)
7. Click 'Test Connection' and enter your UNIX password.
8. Connection should be successful.
![](/assets/8b6ef67a-8d74-11e6-8aa8-41bbce482209.PNG)
9. Do a simple query on collection 'testcollection'.
![](/assets/4f7390ee-8d75-11e6-9457-b6826388ce7b.PNG)
