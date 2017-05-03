# Creating a Maven project

### You will need somewhere for your project to reside

1. Execute the following Maven goal

```
mvn archetype:generate -DgroupId-com.mycompany.app -DartifactId=my-app DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

### The POM

The pom.xml file is the core of project's configuration in Maven.

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
 
  <groupId>com.mycompany.app</groupId>
  <artifactId>my-app</artifactId>
  <version>1.0-SNAPSHOT</version>
  <packaging>jar</packaging>
 
  <name>Maven Quick Start Archetype</name>
  <url>http://maven.apache.org</url>
 
  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.8.2</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```

### Build the project

You should be in the same folder of the pom.file

```
mvn package
```

# Running Maven Tools

### Maven Phases

- **Validate:** validate the project is correct and all necessary information is available
- **Compile:** compile the source code of the project
- **Test:** test the compiled source code using suitable unit testing framework. These tests should not require the code be packaged or deployed
- **Package:** take the compiled code and package it in its distributable format, such as a JAR.
- **Integration-test:** process and deploy the package if necessary into an enviroment where integration test can be run.
- **Verify:** run any checks to verify the package is valid and meets quality criteria
- **Install:** install the package into the local repository, for use as a dependency in other projects locally
- **Deploy:** done in an integration or release enviroment, copies the final package to the remote repository for sharing with other developers and projects

There are two others Maven lifecycles of note beyond the default list above

- **Clean:** cleans up artifacts created by prior builds.
- **Site:** generates site documentation for this project-


