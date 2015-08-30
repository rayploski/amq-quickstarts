Red Hat JBoss A-MQ Quickstarts
====================
Summary: The quickstarts demonstrate messaging using Red Hat JBoss A-MQ. They provide small, specific, working examples that can be used as a reference for your own project.

Introduction
------------

These quickstarts run on Red Hat JBoss A-MQ 6.1 or later. We recommend using the JBoss A-MQ ZIP file. This version uses the correct dependencies and ensures you test and compile against your runtime environment. 

Be sure to read this entire document before you attempt to work with the quickstarts. It contains the following information:

* [Available Quickstarts](#available-quickstarts): List of the available quickstarts and details about each one.

* [Suggested Approach to the Quickstarts](#suggested-approach-to-the-quickstarts): A suggested approach on how to work with the quickstarts.

* [System Requirements](#system-requirements): List of software required to run the quickstarts.

* [Configure Maven](https://github.com/jboss-developer/jboss-developer-shared-resources/blob/master/guides/CONFIGURE_MAVEN.md#configure-maven-to-build-and-deploy-the-quickstarts): How to configure the Maven repository for use by the quickstarts.

* [Run the Quickstarts](#run-the-quickstarts): General instructions for building, deploying, and running the quickstarts.

* [Optional Components](#optional-components): How to install and configure optional components required by some of the quickstarts.

Use of AMQ_HOME Variable
---------------------------------

The quickstart README files use the *replaceable* value `AMQ_HOME` to denote the path to the JBoss A-MQ installation. When you encounter this value in a README file, be sure to replace it with the actual path to your JBoss A-MQ 6 installation. 

* If you installed JBoss A-MQ using the ZIP, the install directory is the path you specified when you ran the command.

Available Quickstarts
---------------------

The list of all currently available quickstarts include:

* amq-helloworld-jms:  This is the default quickstart and is recommended as a first step for becoming acquainted with A-MQ.

* amq-helloworld-net:  This quickstart provides an example of using a C# client to send and retrieve messages.  This quickstart currently only runs on a Windows system.

* amq-helloworld-python:  This quickstart provides an example of using a python client to send and retrieve messages from A-MQ.

* amq-helloworld-intravm:  This quickstart provides an example of accessing and using the A-MQ broker from within the same Java Virtual Machine.  

* amq-helloworld-stomp:  This quickstart provides an example of how to access the A-MQ broker via the STOMP protocol.


Some quickstarts are designed to enhance or extend other quickstarts. These are noted in the **Prerequisites** column. If a quickstart lists prerequisites, those must be installed or deployed before working with the quickstart.

[TOC-quickstart]


Suggested Approach to the Quickstarts
-------------------------------------

We suggest you approach the quickstarts as follows:

* Regardless of your level of expertise, we suggest you start with the **helloworld** quickstart. It is the simplest example and is an easy way to prove your server is configured and started correctly.
* If you are a beginner or new to Red Hat Developers, start with the quickstarts labeled **Beginner**, then try those marked as **Intermediate**. When you are comfortable with those, move on to the **Advanced** quickstarts.
* Some quickstarts are based upon other quickstarts but have expanded capabilities and functionality. If a prerequisite quickstart is listed, be sure to deploy and test it before looking at the expanded version.


System Requirements
-------------------

The applications these projects produce are designed to be run on Red Hat JBoss A-MQ 6.1 or later. 

To run these quickstarts with the provided build scripts, you need the following:

1. Java 1.6 or above, to run JBoss A-MQ and Maven. You can choose from the following:
    * OpenJDK
    * Oracle Java SE
    * Oracle JRockit

2. Maven 3.0.0 or newer, to build and deploy the examples
    * If you have not yet installed Maven, see the [Maven Getting Started Guide](http://maven.apache.org/guides/getting-started/index.html) for details.
    * If you have installed Maven, you can check the version by typing the following in a command prompt:

            mvn --version 

3. The JBoss A-MQ distribution ZIP.
    * For information on how to install and run JBoss, see the [JBoss A-MQ Documentation](https://access.redhat.com/documentation/en-US/Red_Hat_JBoss_A-MQ/) _Getting Started Guide_ located on the Customer Portal.

4. You can also use [JBoss Developer Studio or Eclipse](#use-jboss-developer-studio-or-eclipse-to-run-the-quickstarts) to run the quickstarts. 


Run the Quickstarts
-------------------

The root folder of each individual quickstart contains a README file with specific details on how to build and run the example. In most cases you do the following:

* [Start the JBoss A-MQ Broker](https://github.com/jboss-developer/jboss-developer-shared-resources/blob/master/guides/START_JBOSS_EAP.md#start-the-jboss-eap-server)
* [Build and run the quickstarts](#build-and-run-the-quickstarts)

           
### Build and Run the Quickstarts

See the README file in each individual quickstart folder for specific details and information on how to run and access the example. 

_Note:_ If you do not configure the Maven settings as described here, [Configure Maven](https://github.com/jboss-developer/jboss-developer-shared-resources/blob/master/guides/CONFIGURE_MAVEN.md#configure-maven-to-build-and-deploy-the-quickstarts), you must pass the configuration setting on every Maven command as follows: ` -s QUICKSTART_HOME/settings.xml`


#### Build the Quickstart Archive

In most cases, you can use the following steps to build the application to test for compile errors or to view the contents of the archive. See the specific quickstart README file for complete details.

1. Open a command prompt and navigate to the root directory of the quickstart you want to build.
2. Use this command if you only want to build the archive, but not deploy it:
   * If you have configured the Maven settings :

            mvn clean install
   * If you have NOT configured settings Maven settings:

            mvn clean install -s QUICKSTART_HOME/settings.xml

#### Build and Run the Quickstart Archive

In most cases, you can use the following steps to build and run the application. See the specific quickstart README file for complete details.

1. Make sure you start the JBoss A-MQ server as described in the quickstart README file.
2. Open a command prompt and navigate to the root directory of the quickstart you want to run.
3. Use this command to build and deploy the archive:

   * If you have configured the Maven settings :

            mvn clean install exec:java
   * If you have NOT configured the Maven settings :

            mvn clean install exec:java -s QUICKSTART_HOME/settings.xml


Use JBoss Developer Studio or Eclipse to Run the Quickstarts
------------------------------------------------------------

You can also deploy the quickstarts from Eclipse using JBoss tools. For more information on how to set up Maven and the JBoss tools, see the [JBoss Enterprise Application Platform Documentation](https://access.redhat.com/documentation/en-US/JBoss_Enterprise_Application_Platform/) _Getting Started Guide_ and _Development Guide_ or [Get Started with JBoss Developer Studio](http://developers.redhat.com/products/devstudio/get-started/ "Get Started with JBoss Developer Studio").
