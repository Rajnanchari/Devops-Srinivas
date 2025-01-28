introduction to MAVEN
=================================
         Maven is a tool that is used to compile ,validate codes ,and analyze the test-cases in the code .


--> manages the building ,reporting and documentation from source code management(SCM)
--> maven projects are configured through project object model(POM)
--> POM.XML file contains documentation for all of the objects ,properties ,methods and events  


## what is the capable of maven
========================================

--> information of the project is centralized through maven 
--> our software project is modeled by it
--> Build process is managed 
--> data about the software project is gathered than build itself 
--> document the software ,and our project 
--> Deployable artifacts can be generated from source code 

### Maven Build Life-Cycle
===================================

--> in Maven , the build is run using a predefined and ordered set of steps to call the build life cycle 
--> The Build task that will be performed during the each phase are determined by the configuration in the selected packaging 
--> Maven relies on build life-cycle to define the process of building and distributing artifacts (eg:Jar files, war files)
--> these are 3 builts in build life cycles 
         
         .   Default:-- handles project building & Deployment
            .clean  :-- handles the project clean 
            . site   :--handles project site generation 



## Maven Artifacts 
=========================

--> An artifact is an file resulting from packaging a project 
--> can be a jar, war, ear ,xml file  these are some examples 
--> artifacts are deployed in repositories ,so they can be used ,as dependencies ,by other projects 
--> Artifacts are identified by 3 components 
   
      @ group id : an unique identifier for a group of related artifacts . usually named like java packages (ex:Jpereira.mobile)
      @ Artifact id : an unique identifier within the context of group id ,that identifies the Artifacts projects (eg: Puzzle )
      @ Version: also called Artifacts coordinates 


## project object model (POM)
================================

--> POM for short 
--> XML file located at root of the project(pom.xml)
--> it includes configuration for your projects including :

       . information about the project 
       . configuration details to build the project 
       . contains default values for most of the projects .ex: source dir,target dir 
       . dependencies of the project 
        configuration about plugins & goals 
       . used repositories 


## Maven repository flow
==============================

   step 1: when developer executes mvn it will go and check in local repository .
           if found the dependencies or plugins in the local repository developer 
           will see the output 
   step 1: if not found in local repository from developer machines it will go and 
              search in remote repository 
   step 3: from remote repository required dependencies or plugins will get in local repository 
   step 4: from local repository developer will get output 










  