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
* Again we need to choose *Help / Install New Software*, this time we need to provide the link to the appropriate Groovy-Eclipse plug-in release. To find it the best is to go the [Github of Groovy Development Tools](https://github.com/groovy/groovy-eclipse), and go to its [Wiki page](https://github.com/groovy/groovy-eclipse/wiki). In the bottom there is a table with the plug-in releases compatible with Eclipse versions. Take the appropriate link and paste is into the "Work with" field in Eclipse (see blow).
![Installing Eclipse Groovy Development Tools](images\CDK-Eclipse-Groovy.png)