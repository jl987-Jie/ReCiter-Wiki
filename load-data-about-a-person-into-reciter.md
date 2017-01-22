# Load data about a person into ReCiter

Loading person data into ReCiter is done by the class **Uids** at `src/main/java/reciter/Uids.java`

This class includes a list of UIDs. It goes through these UIDs line by line. It will pull data from LDAP and Oracle and will pull any existing data for these people.

To load data for a person, first ensure that you are connected to the ReCiter database (you may first need to VPN into your institution's network.) Then, add the UID that you want to test into the string array in Uids.java.

Then, open `LdapIdentityController.java`

Start the Spring application (the Tomcat server that will host the ReCiter code) by running `Application.java`

Then point your browser to `http://reciter.med.cornell.edu:8080/reciter/ldap/get/identity/by/uid?uid=nnnnnnn` (Replace nnnnnnn with the desired UID.) This will display the data for the UID formatted as JSON in the browser window. (This is designed for querying.)

If you use the first RequestMapping` URL in `LdapIdentityController.java`, you have to pass the UID as a parameter. This will retrieve data for a single UID.

If you use the second `RequestMapping` URL in `LdapIdentityController.java` it will download the identity information for all the UIDs in that string array. (This is designed for downloading.)