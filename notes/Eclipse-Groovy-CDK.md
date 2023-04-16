---
layout: page
title: Eclipse, Groovy, CDK
---

# Setting up the environment
Recently I have gone through the process of setting up the environment that allow for running simple Groovy scripts with the [Chemistry Development Kit](https://cdk.github.io/). The latter one contains a set of open source Java libraries for Cheminformatics. The simplest way of integrating the CDK library is through [Maven](https://maven.apache.org/). Let's go. 
## Eclipse
* Just download and install the Eclipse IDE for Java developers, the best from an official website of Eclipse, i.e. from [here](https://www.eclipse.org/downloads/packages/). I used the version 4.27.0.

## Java SDK
* I used the Java SDK from [OpenJDK] (https://www.openlogic.com/openjdk-downloads), the version 17.0.6+ 10 for Windows. After the installation needs to be configured in Eclipse (like [here](https://stackoverflow.com/questions/13635563/setting-jdk-in-eclipse)). 

## Maven in Eclipse
* In Eclipse click *Help / Install New Software*, the "Work with" field enter: https://download.eclipse.org/releases/latest. Choose General Purpose Tools / m2e - Maven Integration for Eclipse (see screen blow).
![Maven in Eclipse](images/Eclipse-CDK-Maven_in_Eclipse.PNG)
* In principle it should be possible now to create new Maven project.

## Groovy in Eclipse
* Again we need to choose *Help / Install New Software*, this time we need to provide the link to the appropriate Groovy-Eclipse plug-in release. To find it the best is to go the [Github of Groovy Development Tools](https://github.com/groovy/groovy-eclipse), and go to its [Wiki page](https://github.com/groovy/groovy-eclipse/wiki). In the bottom there is a table with the plug-in releases compatible with Eclipse versions. Take the appropriate link and paste is into the "Work with" field in Eclipse (see below).
![Installing Eclipse Groovy Development Tools](images\CDK-Eclipse-Groovy.png)

# Creating the Groovy project and adding CDK dependencies
To create the Groovy project with integrated CDK libraries we need to follow some steps.
## Creating the Groovy project
* Open Eclipse and create the Groovy project: *File / New / Other / Groovy / Groovy Project*, click Next. 
* Type in Project Name and optionally set up the JDK / JRE environment.
* Click Finish.

## Turning into Maven project.
To incorporate the CDK library via Maven it is convenient to turn the default Groovy project into the Maven Project. To do so, just right-hand-click on the Groovy project, then *Configure / Convert To Maven Project* (see below)
![Converting the Groovy project into Maven project](images\CDK-Convert-To-Maven.PNG)
This will create the pom.xml file and other artifacts related to the Maven project. 
## Adding CDK dependency
The last thing is adding the Maven dependency containing the CDK into this file. We need to add this piece of xml into pom.xml:
```xml
  <dependencies>
   <dependency>
    <artifactId>cdk-bundle</artifactId>
    <groupId>org.openscience.cdk</groupId>
    <version>2.8</version>
  </dependency>
 </dependencies>
```
Saving the pom.xml file should trigger the download of newly incorporated dependencies. 

That's it. Now you are ready to go with Groovy scripts utilizing the CDK capabilities.