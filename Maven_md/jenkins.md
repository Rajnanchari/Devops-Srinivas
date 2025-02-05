continuous integration and its importance

     importance of continuous integration
     1)improve Quality : improves to quality by running multiple unit test and analysing various static code.
     2)Increase productivity:Automating build of code saves a lot of time there by increasing productivity.
     3)Reduce Risk:Eliminates the risk of potential human error.


 ###  Introduced to jenkins:
    features of jenkkins
      .easy installation process
      .provides advance security
      .optimized performance 
      .upgrade are easily availble 
      .disstibuted team management
###  What is continuous integration 
          it is the process of automating the building and testing of code ,each time one of the team member commits changes to version control.

      CI/CD(continuous Integration /continuous deliver or continuous deploymement delivery also knows as Release)

### Popular continuous integration Tools
   .Gitlab cl
   .codeship
   .Bamboo
   .jenkins
   .Teamcity
   .Travisci

   from Aws cloud if we want to perform CI/CD there are various servers like code commint ,code deploye , code guru,
   code pipeline, code build 

   In Azure cloud we want azure devops azure boards, azure repos,azure pipline , azure test plan, azure Artifact.


### What is jenkins

   A Continuous integration server which manages and control processes such as plan ,code ,test ,deploy,operated, and 
   monitor in devops Enviromemt.

### Why Jenkins is so popular

    .open sourec
    .Good Plugin support 
    .Good communication support 
    .Fast and Reliable
    .Good Os Support 
    .Scripted Builds

### Topics

   .Jenkins Arechitecture
   .plugin management in jenkins
   .jenkind security management 
   .Notification master slave arechitecure
   .Jenkins Delivery pipline
   .jenkins Delartive pipline

### Jenkins Architecture Source control management

### plugin management in jenkis

     .To have extra functions we will going for plugin.
     .update:show updates to plugins alredy installed
     .Avaliable:show plugins that are available  for instlltion.
     .Installed:displays plugins installed that have no updates
     .advanced: lists configuration of http proxy, allows manual upload of plugin and url of plugin site



In real time we cannot install plugins as simple as that reason being there might be challenges with proxy settings as well as vpn(virtual private network) inorder to 
avoid this we should configure http proxy in Jenkins plugin of advanced tab.


###  How to install Jenkins on windows:

      Different ways of installation:
      a)using docker
      b)using Kubernetes
      c)using Linux
      d)using war file
      e)offline installations
      f)macos

### prerequisites:

     minimum hardware requirements
     256 mb of RAM
     1GB of drivespace(although 10gb is a recommended minimum if running Jenkins as a docker container)
     recommended hardware configuration for small team
     4gb+ of RAM
    50gb+ of drivespace

### Jenkins tool is developed on java code

        prerequisites:
        A system running windows 10 
        the latest copy of JDK OR JRE installed
         Access to an account with administrator privileges

         Jenkins.io/download/(LTS)

      steps:
          1)Browse to the downloads page of Jenkins under the downloading Jenkins section is a list of installers for the long-term support version of Jenkins
          click the windows link to begin the download download Jenkins 2.479.3
          once you click on windows text under download Jenkins

         a)once after downloading need to go to downloaded folder double click on Jenkins which is of type windows install package.
         b)The setup wizard starts click next to proceed
         c)select the install destination folder and click next to continue
         d)under the run service as a local or domain user option, enter the domain username and password for the user account you want to run Jenkins with. click test credentials to verify
         the login data, then click next to proceed
         Logon type 
         first option:run service as local system (not recommended)

         e) enter the port number you want Jenkins to run on. click test port to check if the slected port is available, then click next to continue
          default port no of Jenkins 8080
        f)select the directory where java is installed on your system and click next to proceed
        g)select the features you want to install with Jenkins and click next to  continue
        h)click install to start the installation process

### how to configure Jenkins:

                .After completing installation process you have to unblock Jenkins before you can customize and start using it.
                .In your web browser, navigate to the default port number you select during the installation using the following address http://localhost:8080
                .navigate to the location on your system specified by the unblock Jenkins page 
                please copy the password from location
                c:/ProgramData/Jenkins/.jenkins/secrets/initialAdminPassword
                where initial Admin password is a file inorder to read the data of that file use cat command
                cat c:/ProgramData/Jenkins/.jenkins/secrets/initialAdminPassword
                copy the password from the inital Admin Password file
                paste the password in the administrator password field on the unblock Jenkins page and click continue to proceed
                once you unlock Jenkins customize and prepare the Jenkins environment
                click the install suggested plugins button to have Jenkins automatically install the most frequently used plugins
                after Jenkins finishes installing the plugins anter the required information on the create first admin user page. click save and continue to proceed

### How to stop the jenkin server on windows:
                   In windows search option search for services and select search for J(left side stop)option

### how to restart the Jenkins
     safe restart go to url of Jenkins
     http://localhost:8080/safeRestart
     Jenkins will try to pause jobs and restart once all running jobs are either finished or paused
     Jenkins is restarting banner
     this will be displayed on most Jenkins pages, you can use it to let users know what is happening a default message will be added if you dont supply one.








