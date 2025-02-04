### JBOSS WildFly

  jBoss is a powerfuel open sourece java application server
  developed by RedHat.

  ### how to download 
   go to wildfly.org/downloda 
          current version 35 

### How to shutdown Jboss wildfly in windows(task)?
       bin-->jboss-cli.bat(click on this file and type command shutdown)

#### Port number of wildfly 
     9990======>Admin
     8080======>Application  /Artifacts

  Admin:<URL:9990>
    <URL:8080>/<Application-Name>


 ### Floder Structure of wildfly 

     .domain
     .modules
     .welcome-content
     .Docs
     .bin
    .appclient

     To start JBoss go  to home folder of then bin 
     filename:Standlone(window batch file)

How to create management console create :

     go to home folder of wildfly------>bin filename add-user [windows batch file]

     Here What type of user do you wish to add ?
    a)management user(mgmt-user.prop)
    b)Application User (application-user.pro)

     here select a) here as user name :jBoss
      next password :Enter password 
     
      word your wish and agin ask retype password 

     Admin/management console :<URL:9990>
   userName& password 

  
  Standalone ----->where we have confguration , deployment ,logs

  1)configuration :where we will be having configuration of appication ,user specifies 

  eg:  mgmt-user.properties&
       mgmt-user.properties

  2)log:standalone ----->log of the wildfly


  3)Deployement:A deployment represent anything that   can    be deployed (e.g: an application such as Ejb-Jar,War,EAR any kind of standard achive such as RAR or JBOSS specific deployment )   into server.

you can use drag and drop to add new content or replace existing deployment simply drag one or serval files into the deployement column. if there's alredy a deployment with the same , the deployment will be replaced , other wise the deployment will be added.the deployments added by drag and drop will be enable by default.

     here  lift-side click on you see 
                          .Upload Deployment
                          .unmanaged Deployment
                          .create empty Deployment

               here click upload Deployment 

   ### How to Deploye application or Artifact

   1)copy the war file and paste it deployment floder of wildfly(Home of wildfly ----->standalone------>Deployments)

   2)cp artifact store path Destination of wildfly

   3)JBOSS wildfly GUI------->upload Artifact 

  ### How we can change default port numbers of wildfly (9990 and 8080)task.
     standalone-->configurations-->standalone.xml and standalone-full.xml(change port numbers here)

### How we can configure master/slave architecture in wildfly
    Domain Mode: WildFly must be run in domain mode to enable master/slave functionality. 
    Domain Controller: The master server acts as the domain controller, responsible for distributing configuration and deployments to the slave servers. 
    Configuration File: The domain.xml file defines the domain configuration, including the master and slave servers, and their communication details. 

### confguration :
     Things to keep in mind before changing confguration changes.

     1)where to change
     2)Backup
     3)How to change
     4)Try or Experiment in local Enviroment
     5)Documentation

### Snapshot

   for wildfly -confguration
    Home folder of wildfly-->standalone--->confguration-->standalone-xml-history
    FileName:Standalone.v1
    eg:port number change

Need to rename the original or existed file and then replace the customzed
as per reqirment/change

Different status of the artifacts deployed in wildfly :

  in wildfly ,deployed artifacts can have various status states

      Deployed: The application is successfully deployed and running on the WildFly server.
      Undeployed: The application has been removed from the server and is no longer running.
      Failed: An error occurred during deployment, preventing the application from starting.
      Starting: The application is currently being initialized and is not yet fully available.
      Stopping: The application is in the process of being gracefully shut down.
     Suspended: The application is temporarily paused and not accepting requests.
     Redeploying: An existing deployment is being updated with new code and restarted. 


wildfly management console :
     you can view the status of deployed artifact through the wildfly admin console
     which provides a list of deployments within current state.

 CLI(command line interface)
   using the wildfly command-line interface. you can query the status of deployment with management command.

   indicating whether the application is currently running, being deployed, experiencing issues, or undergoing a state change. 
### Domain & Host controller in wildfly:
      In JBoss wildfly , a "domain controller " is the central management point for a group of server within a domain ,responsible
      for maintaing the  overall configuration and policy.

      while "a host controller" is a separate process running on each server within the domain , communicating 
      with the domain controller to manage the individual server instances on the host machine

      essentially , the domain controller dicatates the overall confguration, and the host controllers execute those
      confguration on their respcetive service.

      key points about domain and controller:

 Domain controller:
 a)Act as the central management point for the entire domain.

 b)Stores the domain-wide confguration in the file called "domain.xml"
     [Home folder>Domain>confguration>domain.xml]

c)Responsible  for distributing confguration changes to all host controlles within the domain


### Host Controller:

  a) manages the appication server instances running on a specific host.

  b)Reds its configuration from a "host.xml" file specific to that host.
    [ Home folder >Domain>confguration>host.xml] 

  c)communicates with the domain controller to receive confguration updates and start/stop server instances.

      DC HC-Domain Control Host Control
      Domain is referring to centralised or master wildfly where we can manage other-(host) wildfly servers. 

