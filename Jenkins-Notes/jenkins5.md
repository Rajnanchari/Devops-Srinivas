### What if jenkins administrator forgot the password
    Go to the jenkins homedirectory c drive             c:\ProgramData\Jenkins.jenkins

    In that path open config.xml file search for true

    Replace True with False false then save it access the jenkins url in browser where you will not see any login details/user details in jenkins GUI & go for the manage jenkins

    First will go to security then under security Realm(where we change config.xml from true to false it will be none).

    First here we need to change security realm from none to 'Jenkins own user database'

    Next go for Authorization(where we change config.xml file from true to false authorization will change to Anyone can do anything)

    Here we need to change from anyone can do anything to either Matrix based/project based strategy.

    Once after changing the strategy under that uncheck the anonymous & click on Add user button & add the admin user & give the roll as administrator then save it.

    We need to go for manage jenkins users go for the admin user change the password then save it. Now restart the jenkins server.

     Note: Better take backup of config.xml

    Once restarted check with admin user whether admin user has all the privileges or not then go back to config.xml file & modify use security tag from false totrue then restart the jenkins server.

### Using Jenkins environment variables
    Jenkins pipeline exposes environment variable via the global variable env, which is available form anywhere within a jenkins file

    https://www.jenkins.io/doc/book/pipeline/jenkinsfile/#using-environment-variables

### Below are the some environment variables

     Build_ID
     The current BUILD ID, identical to BUILD_NUMBER for builds created.

     likewise we have BUILD_NUMBER,BUILD_TAG,BUILD_URL,JENKINS_URL,JOB_NAME,NODE_NAME then WORKSPACE

     For example user jenkins file(declarative pipeline) in that URL you will see basic example code copy that code create new item in jenkins for pipeline job.

     Replace the script with copied code & save it & build it.

     Expected output should be Running 1 on http://localhost:8080/

### How to parameterized the jenkins job
    Parameters
     Parameters/variables allow you to prompt from one or more inputs that will be passed in to a build.

     Create New job in general configuration of that job you can see the option this project is parameterized need to checkbox that & there will use option add pareameter dropdown click on that you will see various parameters those are

     Boolean Parameter

     Choice Parameter

     Credentials Parameter

     File Parameter

     Multi-line string Parameter

     Password Parameter

     Run Parameter

String Parameter

    For example click on choice parameter(Defines a simple string parameter, which can be selected from a list. You can use it during a build) give thw name as ENV & under choice you can give more than one environment name & under description a description that will be shown to user later & click on save.

    When you check the job to be trigger you will see build with parameter options.Click on that select the choices which we configured & go for the build button.

### Another way of creating jenkins user

    Manage jenkins then security checkbox the Allow users.

