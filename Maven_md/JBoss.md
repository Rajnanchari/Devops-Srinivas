### JBOSS WildFly

  jBoss is a powerfuel open sourece java application server
  developed by RedHat.

  ### how to download 
   go to wildfly.org/downloda 
          current version 35 

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

   How we can change defult port number of wildfly 

      -->mgmt console and application port number

    How we configure master.

       -->slave configuration in wildfly


   
                        