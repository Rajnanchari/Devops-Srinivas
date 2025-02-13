### Tool Configuration in Jenkins
    If at all you wanted to configured tool's like Apache maven , docker etc.
    We need go to 
    manage jenkins>system configuration then tools[configure tools,there locations and automatic installer]
    Eg:To configure apache maven specifice version(3.6.6) under that to configure apache maven  in tool like we should install plugin apache maven then only we can able to see maven installation in tool.
    click on add maven then you can go for specifice requirement.To install automatically you should check the box automaticallu option.

 ### How to Trigger job Remonetly

   To configure this kind of req to makes use tigger -trigger build remontely using authatication token below the 
   create freestyle job with name build remontely.

   checkbox the trigger build remonetly options and configuture any build step with authatication 
   Token(aja-123) save it and check this job user below url
    syntax Remote URL: JENKINS-URL/job/buildremonetly/build?Token=TOKEN-NAME
     Where jenkins-url is jenkins is listening or Accesible
     build remonetly is a JobName
     TOKEN-NAME is Authatication token which we configure 
     Eg:localhost:8999/job/buildremonetly/build?Token=aja123

   Another way of Trigger job remontely 

     In order to trigger (example job2 we can go for below command )
     curl -u admin:<API-TOKEN> -X POST locallhost:8999/job/job2/build

     where -u is user(admin)

     API token which as to be generated with the user admin post is a method to cal the url      