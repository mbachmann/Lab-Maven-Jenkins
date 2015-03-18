SWEN2 Lab - Maven & Jenkins
===========================

## Introduction
This lab is designed to help you become familiar with the Maven build automation tool and the Jenkins Continuous Integration Server that you will be using to manage your projects.

## Objectives
In this excercise you will:
- Setup set up your Maven and Jenkins environment
- Learn to master Maven configuration, lifecycle and goals
- Practice to setup and run integration tasks on a Jenkins Server

## Requirements

**Hardware:** none

**Software:**
- An up to date web browser
- Your preferred text editor
- Basic Maven installation for your platform (see installation section)
- optional: Eclipse to test the Maven Eclipse integration

**Resources:**
- User Account on a SWEN2 lab server with installed Jenkins server
  (Get the server name and account information from your lab assistant)

## Expected results
Complete the tasks given below. Look up the required commands in the available documentation (see [References](#References)). To complete the assignment show your lab assistant the installed task on the Jenkins server.

<!--
## Grading
- none
--> 

## References
Following some references which might help you to complete the tasks:
- [Maven Quick Reference Card][mvnqref]
- [DZone Maven Refcard][mvndzone]
- [Maven Reference Book][mvnref]
- [Maven By Example Book][mvnex]
- [Maven Central Repository][mvncentral]
- [Jenkins Webpage][jenkins-ci]

[mvnqref]:  https://maven.apache.org/guides/MavenQuickReferenceCard.pdf "Maven Quick Reference Card"
[mvndzone]:   http://refcardz.dzone.com/refcardz/apache-maven-2 "DZone Maven Refcard"
[mvnref]:     http://books.sonatype.com/mvnref-book/reference "Maven Reference Book"
[mvnex]:      http://books.sonatype.com/mvnex-book/reference "Maven By Example Book"
[mvncentral]: http://search.maven.org/#browse "Maven Central Repository"
[jenkins-ci]: http://jenkins-ci.org "Jenkins Webpage"

[mvninstall]: http://books.sonatype.com/mvnex-book/reference/installation-sect-maven-install.html
<!--
##Preparation Work before the Lab
- none
-->
## General Notes
???

#### Ask for help
If you are stuck and have a problem you can not solve using the documentation, ask your colleques, the lecturer or lab assistant for help.


## Tasks

This lab consists of three parts:

1. [Setting up Maven](#part1-settingupmaven)
2. [Master Maven](#part2-mastermaven)
3. [Practice Jenkins](#part3-practicejenkins)

### Part 1 - Setting up Maven
#### Installation
Ensure that the command line version of Maven is installed on your computer and that you know how to access it via the command line / terminal interface.

Find some basic info for all Systems in the [install instructions][mvninstall].

The official way to install Maven is to download and unpack the binary ZIP file to a common directory, set the environment variable `M2_HOME` and add the bin directory to your `PATH` environment variable.

##### Windows
Follow process in the [install instructions][mvninstall].

##### Unix (Linux / OS X / Solaris / FreeBSD) manual installation
Download newest apache-maven-x.x.x-bin.zip from http://maven.apache.org/download.cgi.
Open shell:
```
$ sudo unzip ~/apache-maven-x.x.x-bin.zip -d /usr/share/
$ sudo ln -s apache-maven-x.x.x /usr/share/maven
```
Open `~/.profile` (single user) or `/etc/profile` (all users) and add the following lines:
```
export M2_HOME=/usr/share/maven
export PATH=$PATH:$M2_HOME/bin
```

##### Unix (Linux / OS X / Solaris / FreeBSD) installation using package manager
An alternative option to install maven is to use the package manager of the unix system. 
* on DEB based systems (Debian,Ubuntu,...) use: `sudo apt-get install maven`. 
  (this is a quite outdated version 3.0.x)
* on RPM based systems (RedHat,CentOS,Fedora,...) exists no official package
* on OS X you can install Maven using a packet manager for OS X like Homebrew or MacPorts.
  Because the packages are usually compiled during installation you need to install Xcode beforehand. This is recommended especially, if you already have Xcode installed or you would like to install also other common unix packages. 
  Homebrew (<http://brew.sh>): 
  `$ brew install maven`

  MacPorts (<http://www.macports.org/install.php>):
  `$ port install maven2`

##### Verify installation
Open a new shell or cmd.exe session and test if maven is available:
```
$ mvn -version
Apache Maven 3.2.3 (33f8c3e1027c3ddde99d3cdebad2656a31e8fdf4; 2014-08-11T22:58:10+02:00)
Maven home: /usr/local/Cellar/maven/3.2.3/libexec
Java version: 1.8.0_20, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_20.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.10.2", arch: "x86_64", family: "mac"
```

> This concludes part 1 of the lab. You should now have a working Maven installation.



### Part 2 - Master Maven

In this section you will learn how to use Maven to automate an existing project. This is also called 'mavenizing' a project.


#### Fork your copy of the project on GitHub


#### Create a basic POM file
- generate basic POM using `mvn archetype:generate`
- fill in project settings
- add Maven temporary files to .gitignore

#### Add dependencies
- add dependency entries for the required libraries.
- lookup exact artifact id on [Maven-Central][mavencentral]
- List of required libraries
  - x
  - y
  - ...
- Test `mvn compile` goal

#### Add some dependency exclusions


#### Verify the default lifecycle

#### Run tests

- configure surefire Plugin

#### Cleanup your project

#### Use Maven with Eclipse 

- configure Eclipse-Plugin
- add Eclipse files to .gitignore

#### Configure and run Tomcat

- configure Tomcat-Plugin

#### Run Integration tests

- compiler, exec, failsave plugin



> This concludes part 2 of the lab. You should now master the basic Maven workflows.


### Part 3 - Practice Jenkins

#### Login and configure Jenkins

#### Manual build task

#### Nightly build

#### Trigger push on git repository


> This concludes part 3 of the lab. You should now have configured Jenkins to run task periodically and on a git push.

### Closing the Lab


#### If you still have time left. 

- ?

#### Show working Jenkins tasks to your lab assistant



> **Congratulations! You finished the Lab Maven & Jenkins**
