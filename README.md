ELECTRIC VEHICLE STATION MANAGEMENT SYSTEM (EVSMS)

This document provides step-by-step instructions to set up and run the Electric Vehicle Station Management System project using Java, Apache Tomcat, MySQL, Eclipse IDE, and MySQL Query Browser.

----------------------------------------------------------------------
PREREQUISITES

Ensure the following tools are installed and configured:

- Java JDK (8 or above)
- Apache Tomcat (9.0+)
- MySQL Server (5.7+)
- Eclipse IDE (Enterprise Java Developers)
- MySQL Query Browser (any version)
- Modern Web Browser (Chrome, Edge, Firefox)

----------------------------------------------------------------------
PROJECT SETUP INSTRUCTIONS

1. INSTALL JAVA JDK
   - Download from: https://www.oracle.com/java/technologies/javase-downloads.html
   - Set environment variables:
     - JAVA_HOME
     - Add 'bin' folder to PATH

2. INSTALL AND CONFIGURE APACHE TOMCAT
   - Download from: https://tomcat.apache.org/
   - Extract the ZIP file
   - Set CATALINA_HOME environment variable
   - Copy the provided EVSMS.war file into:
     [TOMCAT_HOME]/webapps/

3. INSTALL AND CONFIGURE MYSQL
   - Install MySQL Server and create a user (root or custom)
   - Open MySQL Query Browser or MySQL Command Line Client
   - Execute the following command:
     SOURCE path/to/evchargestation.sql;
   - This will create the database and required tables

4. SET UP ECLIPSE IDE
   - Install Eclipse IDE for Enterprise Java Developers
   - Open Eclipse and follow:
     File > Import > Existing Projects into Workspace
   - Import your project (if source code provided), or skip this if using only the WAR file
   - Configure Apache Tomcat:
     - Window > Show View > Servers
     - Right-click > New > Server > Apache > Tomcat v9.0
     - Set the path to the Tomcat installation
     - Add your project to the server

5. DEPLOY THE WAR FILE
   - Copy the provided EVSMS.war file to:
     [TOMCAT_HOME]/webapps/
   - Start the Tomcat server using:
     [TOMCAT_HOME]/bin/startup.bat

6. ACCESS THE APPLICATION
   - Open a web browser
   - Go to: http://localhost:8080/EVSMS/
   - The EV Station Management System homepage should appear

----------------------------------------------------------------------
TROUBLESHOOTING

Issue: Tomcat not starting  
Solution: Check Java installation and JAVA_HOME configuration

Issue: WAR file not deploying  
Solution: Stop Tomcat before copying the WAR file

Issue: Database connection error  
Solution: Verify MySQL username/password and DB config in project

Issue: Port 8080 already in use  
Solution: Change Tomcat port in conf/server.xml

----------------------------------------------------------------------
FILES PROVIDED

- EVSMS.war               → Deployed application archive
- evchargestation.sql     → SQL script to create the database

----------------------------------------------------------------------
STEPS TO RUN THE PROJECT

After completing setup and importing the project into Eclipse:

1. In Eclipse, open the **Project Explorer** or **File Explorer** view  
2. Navigate to the `Home.html` file (or any entry-point page)  
3. Right-click on the file  
4. Choose `Run As > Run on Server`  
5. Select `Tomcat v9.0 Server at localhost`  
6. Click **Finish**  
7. Your project will launch in the browser via Eclipse’s embedded Tomcat serv
