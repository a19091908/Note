<h1>WebSphere</h1>

###How to run WebSphere

1. cd to the bin folder in the server path like: 
    C:\Program Files\IBM\WebSphere\AppServer\profiles\AppSrv01\bin

2. use command to run startSerser.bat or .sh
    Windows: start startServer.bat server1


###How to find all the port numbers relevant to WebSphere

1. cd to the path like: 
    C:\Program Files\IBM\WebSphere\AppServer\profiles\AppSrv01\logs

2. read AboutThisProfile.txt

3. you can see the port numbers in this file.
    such as: manage console port, HTTP, and HTTPS

###How to enter manage page of WebSphere

1. https://[IP]:[manage console port]/ibm/console/logon.jsp
    such as: https://localhost:9043/ibm/console/logon.jsp

###How to deploy 

1. In the left panel of the management interface, click "build a new application"

2. upload the war file that you want to deploy

3. set up some configurations
    For example, you can define the root directory of the application

4. click application -> application type -> websphere enterprise application

5. start the application you want to start

###set up JDBC

* set up JDBC provider
    1. click create a new JDBC provider

    2. choose DB type, provider type, and implement type

    3. put the JDBC driver to the class path (Note that please put the right version of driver suitable for your application )

* set up data source
    1. click create a new data source

    2. type JNDI name such as jdbc/Taroko_SIT

    3. choose JDBC provider you just created

    4. type the name of the database and server and the port number

    5. After finishing this, we need to set up userid and password

    6. click the data source you just created

    7. click the JAAS-J2c on the right of pannel

    8. create DB login information including the name of the information, a userid, and a password

    9. come back to the detail page of the data source you just created

    10. choose the name of DB login information, and choose "DefaultPrincipalMapping" as mapping-setting alais

    11. after finishing all the steps mentioned above, click test connection 
