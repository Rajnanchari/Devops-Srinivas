introduction to MAVEN

 Maven is a tool that is used to compile ,validate codes ,and analyze the test-cases in the code .

--> manages the building ,reporting and documentation from source code management(SCM)
--> maven projects are configured through project object model(POM)
--> POM.XML file contains documentation for all of the objects ,properties ,methods and events  


## what is the capable of maven

   . information of the project is centralized through maven 
   . our software project is modeled by it
   . Build process is managed 
   . data about the software project is gathered than build itself 
   . document the software ,and our project 
    . Deployable artifacts can be generated from source code 

### Maven Build Life-Cycle

--> in Maven , the build is run using a predefined and ordered set of steps to call the build life cycle 
--> The Build task that will be performed during the each phase are determined by the configuration in the selected packaging 
--> Maven relies on build life-cycle to define the process of building and distributing artifacts (eg:Jar files, war files)
--> these are 3 builts in build life cycles 
         
         .   Default:-- handles project building & Deployment
            .clean  :-- handles the project clean 
            . site   :--handles project site generation 



## Maven Artifacts 

--> An artifact is an file resulting from packaging a project 
--> can be a jar, war, ear ,xml file  these are some examples 
--> artifacts are deployed in repositories ,so they can be used ,as dependencies ,by other projects 
--> Artifacts are identified by 3 components 
   
      @ group id : an unique identifier for a group of related artifacts . usually named like java packages (ex:Jpereira.mobile)
      @ Artifact id : an unique identifier within the context of group id ,that identifies the Artifacts projects (eg: Puzzle )
      @ Version: also called Artifacts coordinates 


## project object model (POM)

--> POM for short 
--> XML file located at root of the project(pom.xml)
--> it includes configuration for your projects including 

       . information about the project 
       . configuration details to build the project 
       . contains default values for most of the projects .ex: source dir,target dir 
       . dependencies of the project 
        configuration about plugins & goals 
       . used repositories 

### Maven repository flow:

 Step1: when developer executes mvn command it will go and checkin local repository.If found the dependencies or plugins in the local repository developers will see the output.

  Step2: If not found in the local repository from developer machines it will go and search in remote repository

  Step3: From remote repository required dependencies or plugins will get stored in local repository

Step4: from the local repository developer will get the output.

### project object model:
     pom for short

     xml file located at the root of the project(pom.xml)

    it includes configuration for your project including:
    information about the project
    configuration details to build the project
    contains default values for most of the projects.Ex sourcedir,targetdir
    Dependencies of the project
    configuration about plugins and goals
    
    used repositories

### Declaring Dependencies

     while declaring the dependencies, coordinates of the artifacts must be provided
     groupid: a unique identifier for the group of related artifact

     artifactid: an artifact is a file which is made after
     packaging a project and artifact is a unique identifier 
     with in the context of groupid and it identifies the 
     artifacts

     version: it is an identifier for the release or 
     build number of project

### maven installation:

      A system running windows
      A working internet connection
      Access to an account with administrator priviliges
      access to the command prompt
      A copy of java installed and ready to use, with the 
      JAVA_HOME environment variable setup

     step1: download maven zip file and extract 
     step2: add maven_home system variable(Enviroment variable)
     step3:add maven_home directory in path variable(New)

### Install java on windows
      prerequisites:
      system running windows
      internet connection
      administrator priviliges  
      How to install java 

        Step 1: Add Java to System Variables
                 Step 2: Add JAVA_HOME Variable


       First go to the browser and search Download java 
	• Select windows and select 64 Installer click on the link 
	• so after clicking on the link the java jdk will be download it into your local machine 
          it will download into a c drive in local machine 
          open the c drive go to program file then go to java and then click on jdk and select and copy the path 
          After selecting the path go to edit the system environment variables then click on ev select new gave variable name as JAVA_HOME and that path which you have copied from the jdk
          Select Path in variable path then click on edit then click on new paste the jdk path here also 
          ckeck on command prompt search java -version then it will show you what version you have download 
               
         
              



  