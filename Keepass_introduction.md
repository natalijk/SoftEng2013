
## Introduction
### What is the project?

+ KeePass Password Safe, release number 1.10. KeePass Password Safe is an OSI Certified Open Source Software distributed under the terms of the GNU General 
Public License Version 2 or under. 


##Overall description of the product (=what is it? can you understand it?)

+The system gives resolution to memorizing passwords problem. Its 
purpose is to keep all of the user’s passwords, data, email accounts, usernames and URLs stored in a very 
secure, encrypted database, protected by a Master Password. The system is very small so it can be easily 
transferred from one computer to another. It provides several functionalities on the already encrypted data 
and the new ones to be inserted. The database produced, is protected by a Master Password only known by 
its inventor with no backup if lost. 

+ KeePass consists of a database which contains data for one or more users. Each user’s data are divided into 
groups and subgroups so that they are organized in a form that serves right the user. Every user has a unique 
Master Key which can be simple or composite and its combination opens uniquely the database. If lost there 
is no recovery. Groups and subgroups contain entries with usernames, passwords URLs etc that can be sent 
or copied to websites, application and accounts. There is also the ability for a onetime key creation to be 
used once in a transaction without the risk of reused by others for any reason. 


##Target audience?
+Developers: in order to be sure they are developing the right project that fulfills requirements provided in 
this document. 
Testers: in order to have an exact list of the features and functions that have to respond according to 
requirements and provided diagrams. 
Users: in order to get familiar with the idea of the project and suggest other features that would make it even 
more functional. 
Documentation writers: to know what features and in what way they have to explain. What security 
technologies are required, how the system will response in each user’s action etc. 
Advanced end users, end users/desktop and system administrators: in order to know exactly what they 
have to expect from the system, right inputs and outputs and response in error situations

##The situation?

Groups and subgroups contain entries with usernames, passwords URLs etc that can be sent
or copied to websites, application and accounts. There is also the ability for a onetime key creation to be
used once in a transaction without the risk of reused by others for any reason.

## Motivation?
+ It was created for the purpose to solve a problem that really bothers many people today when they have to 
choose from memorizing a lot of passwords to be secure or to use every time the same one so they won’t 
forget it but risk be found out by others

##How it works

User has a master key and owns a database;
Master key unlocks database;
Database is divided into groups/subgroups;
Groups/subgroups consist of entries;
Entries send data to webpages/applications;
Database interacts webpages/applications;
Algorithms for encryption encrypts master key;
Algorithms for encryption generates one time password;
One ltime password is used in webpages/applications;


##Structure
1. Introduction
 * Purpose
 * Document Conventions
 * Intended Audience and Reading Suggestions
 * Project Scope
 * References
2. Overall Description
 * Product Perspective 
 * Product Features
 * User Classes and Characteristics
 * Operating Environment
 * Design and Implementation Constraints
 * User Documentation
3. System Features
4. External Interface Requirements
 * User Interfaces
 * Communications Interfaces
5. Other Nonfunctional Requirements
 * Performance Requirements
 * Safety Requirements
 * Software Quality Attributes


## Compare the structure of the document with the template provided for the course group work. 

+ The introduction has more specifications
+ Product features and system features descibed seporatly
+ User cases are defined as the features of the product and user classes and characteristics defined separetly
+ No user case diagrams and scenarios included
+ INcludes an information on operating environment requirements in the overall description
+ User interface described shortly and under External requirements field
+ NO  project management description included

## Use Cases

* What the system (will) do?
    * It provides a very secure, encrypted database where the user can store all his passwords, usernames, 
email accounts, URLs, notes without any risk for others to find them. With one master key the user can
get access to all of this.
   The different use cases can be summarized as the following:
      * Manage password databases (Create, open, save, print and save)
      * Manage groups of passwords among the databases.
      * Manage the password entries.

* Use case diagram?
      * No, they don't use use case diagrams for describing the system.

* How cases are described, how much details?
      * The use cases are specified as "system features", and each scenario is fully documented with a description of
        the use case, the workflow and the functional requirements. This is done by listing the workflow and the 
        requirements, rather than drawing a use case diagram.
      
## General structure of the system

* What chart techniques are used? Why?
      * This document only includes one chart, which is used for showing the main components of the system and the
        relationships between them. It gives a simplified version of the system and makes it easier to understand.

## Functional & non-functional requirements)
* Listed?
   * The functional requirements are presented under its corresponding use case.
     The non-functional requirements are listed at the end of the document.

* Measurable/traceability? (is it possible to check from the upcoming end product if a feature / requirement is implemented or not?)
   * Yes, it is possible. In general, all the features are well-described.

## How does (will) it look?
* UI examples / views?
   * The document doesn't include any screenshots. However the software already exists and these are some screenshots of it: 
   * Entering the master password
   * ![Bilby Stampede](http://keepass.info/screenshots/keepass_2x/getkey_big.png)
   * Main window
   * ![Bilby Stampede](http://keepass.info/screenshots/keepass_2x/main_big.png)
   * Adding a new entry
   * ![Bilby Stampede](http://keepass.info/screenshots/keepass_2x/addentry_big.png)

* Are the pictures mockups or screenshots from existing system?
   * No pictures are included

* Transitions between views
   * No pictures are included



##Process model?
+isn't included to the document

##Keepass point of view

* This document is good, everything is carefully described, well structured. 
* Exist all the use cases and requirements.
* Product requirements are thoroughly listed.
* By the interface description it is easy to imagine it.
* Functional and Non-Functional requirements are not very clear.
