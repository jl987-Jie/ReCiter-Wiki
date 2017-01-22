# What is required for me to use ReCiter?

The steps required for installing ReCiter vary depending on how you wish to use the system. If you just want to use ReCiter for author name disambiguation you might wish to run it as a standalone tool. If you want to contribute to ReCiter or if you are using it for research, you may choose to install and run it within Eclipse, an integrated development environment (IDE). ReCiter can run as a server on any modern laptop or desktop computer (or on a more powerful server) (see [system requirements] for more details.)<br>

The table below is a summary of the requirements for four different ways of using ReCiter.

## Java

If you wish to run ReCiter on your local machine, you must first install Java (if it is not already installed). Alternately, you may use a browser to run an instance of ReCiter installed on a different machine accessible through your local area network or via the internet. In this case, Java is not required on your local machine. Here are instructions for installing Java, which is freely available. You will need version 8 or higher: [Java Platform, Standard Edition Development Kit (JDK)] (http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html).

## Git

Git is the distributed version control system being used to host the code for ReCiter. If you wish to run ReCiter on your local machine, you must first install Git (if not already installed). Here are instructions for installing [Git] (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), which is freely available.

## Apache Maven

Apache Maven is a build automation tool that ensures that additional dependencies (required code libraries) are installed automatically along with ReCiter. If you wish to run ReCiter on your local machine, you must first install Maven (if not already installed). Maven is freely available: [Apache Maven] (http://maven.apache.org/install.html).

# Installing ReCiter as a server

## Installation prerequisites

To install ReCiter as a server you will first need to install Java, Git, and Apache Maven, as described above. These tools are freely available.

## Install ReCiter as a server without Eclipse
1. Open a terminal window or command prompt as follows:<br>
* If you are using a Mac (OS X), click the magnifying glass in your menu bar to open Spotlight. Enter "Terminal" in the search box and double-click the application. You can also use Finder to navigate to your Applications folder, open the Utilities folder, and then open the Terminal application.
* If you are using Windows, instructions for opening a command prompt for Windows 7, 8, and 10 are available [here] (https://www.lifewire.com/how-to-open-command-prompt-2618089).
2. Use the change directory command (`cd`) to navigate to the directory where you would like to install ReCiter. For example:<br>
`cd /Users/myaccount/reciter`
3. Enter the following command to use git to clone ReCiter to your local machine:<br>
`git clone https://github.com/wcmc-its/ReCiter.git`
4. Enter the following command to star ReCiter by using the Spring Boot framework:<br>
`mvn spring-boot:run`
5. Open your web browser, where you may access the API commands used to run ReCiter. For example, to run ReCiter for all UIDs, enter the following:
`localhost:8080/reciter/all/analysis/`

## Install ReCiter as a server with Eclipse
1. Download the latest version of Eclipse from http://www.eclipse.org
2. Install Eclipse using the install method appropriate for your operating system
3. Run Eclipse
4. From the Eclipse welcome screen, click on "Checkout projects from Git". (If you do not see the Eclipse welcome screen it may be accessed by selecting "Help", then "Welcome".)
5. Click "Clone URI"
6. Click Next
7. In the "URI" box, type https://github.com/wcmc-its/ReCiter.git
8. In the Authentication panel, enter your login username and password for the GitHub repository
9. Once the ReCiter project has finished compiling, right-click on the parent directory for the ReCiter project in the Package Explorer in Eclipse and select "Team, Pull"
10. In the Package Explorer, right-click on src/main/java/reciter/Application.java and select "Run As, Java Application"

## Run ReCiter on the server
After installing ReCiter with either of the two methods above (i.e., with or without Eclipse), open your web browser. You may then run ReCiter by entering the API commands used to run ReCiter. For example, if the ReCiter server is on your local machine, to run ReCiter for all UIDs, enter the following:
`localhost:8080/reciter/all/analysis/`

# Database installation

## Installing MongoDB

Followed the steps in the [MongoDB installation page] (https://docs.mongodb.com/manual/installation/?jmp=footer) to install it onto your operating system.