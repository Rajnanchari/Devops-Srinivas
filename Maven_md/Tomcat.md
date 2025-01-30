## Apache Tomcat

  .web server is in our host on applicaation

  ### what is Apache Tomcat

    Apache tomcat is an open-source web server and servlect container of java code.

    Prerequisites:
    .java jRE installed and configured 
    .Administrator privilege

   #### How to install apache tomcat on windows
    .via windows service installer


  step2:install tomcat 

  install tomcat via the windows service installer for an automated and wizared epernice.
  .exe is directly download no need to zip here.

  After download zip file, depending on your windows  version ,unzip download file ,Right click the file 
  and select Extract all.

  .Default port number of apache tomcat is 8080.
  .If at all we want change defalut port number goto 
  apache >conf/>then server.xml file we need figure out
  this
       <connect port ="8080" portocal ="HTTP/1.1"
       connectionTimeout ="20000"
       redirectPort ="8443">


## How to start and stop Apache Tomcat
### start
Apache tomcat>Bin>set up(windows Batch file)

### stop 
Apache Tomcat > bin >showdown

### For configuration changes:
    Apache Tomcat ---> Conf

 ### For hosting Of Application (Artificate/Deployble package)
        Apache tomcat --->webapps

   ### For log        
   Apache tomcat --->logs(Apache Tomcat and also application which is running inside Tomcat)

   we can access Apache Tomcat localhost:8080 or 
   127.0.0.1:8080
   


     

