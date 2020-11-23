jar

# set the entry point of jar

For example, this command creates app.jar where the Main-Class attribute value in the manifest is set to MyApp:

jar cfe app.jar MyApp MyApp.class
You can directly invoke this application by running the following command:

java -jar app.jar
If the entrypoint class name is in a package it may use a '.' (dot) character as the delimiter. For example, if Main.class is in a package called foo the entry point can be specified in the following ways:

<code> jar cfe Main.jar foo.Main foo/Main.class </code>

# add class path

We want to load classes in MyUtils.jar into the class path for use in MyJar.jar. These two JAR files are in the same directory.

We first create a text file named Manifest.txt with the following contents:

Class-Path: MyUtils.jar
Warning: The text file must end with a new line or carriage return. The last line will not be parsed properly if it does not end with a new line or carriage return.
We then create a JAR file named MyJar.jar by entering the following command:

<code> jar cfm MyJar.jar Manifest.txt MyPackage/*.class </code>
This creates the JAR file with a manifest with the following contents:
Manifest-Version: 1.0
Class-Path: MyUtils.jar
Created-By: 1.7.0_06 (Oracle Corporation)
The classes in MyUtils.jar are now loaded into the class path when you run MyJar.jar.
