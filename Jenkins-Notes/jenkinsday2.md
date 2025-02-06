### Pulgins 

They are two ways to install plugins
### Automatically plugin
    once login into jenkins JUI left side you see options manage jenkins click on that in first type system.configuration under you can see plugins go to avaliable plugins search for plugin which is requried and select plugin under list once seleceted the plugin list of plugin.


### Manual Plugin
     under plugin tab go for avaliable plugin search for the plugin click on plugin is required once you click on plugin new tab open then click on Release under releases you see various version of plugins. go for plugin which is required specifice version then yoi see install option click on direct link once link on direct link plugin will download local machine.

     when you download plugin manual way agin we need to deploye jenkins in jenkins jui plugin tag clik on advanced setting where you can choose file upload button to upload it.

###  What is plugin
    plugins are where we can add, remove, disable or enable plugin that can extend the functionality of jenkins or to have extra functionality.    


    When install plugin automatically way plugin extens is JPI(jenkins plugs) 

    when you install manual way HPI(Hudson plugin)


 ### How to uninsatll plugin

      manage jenkins>plugins>Insatlled Plugins 
      -->search plugin name which we wanted to uninstall select the plugin and then uninstall button will be higlighted once clicked on uninatall plugin will uninsatlled.

 ### How to Update Plugin:
      manage jenkins>plugins>updates 
      -->select the plugin and then update button will be highlighted once clicke on update ,plugins will get update.

      In Realtime we should not update plugin directly bcoz the may be challege cncouted it will recommand to update plugins local machine first. in local machine where other team members not effect if anything goes wrong.

 ### How to create user :
     manage jenkins > security >User(create/delete/modify use that can log in to this jenkins ) 
      click on user+ will see   .username
                                .password
                                .confirm password
                                .FullName
                                .Email Adress
                                create user-->click



 ### How to give perminsion to the users.
     manage jenkins>security (secure jenkins how is all to access uses system) click on that is Authorized under Add user button ask user id given id click on ok button.

     user add in exiting list then give required permision to the user by checking the box [the minimum Access is overall read].By defult what where we create user for jenkins user can stored in jenkins own user database.

     This is sutiable for smaller set up where you have no exiting user data base.
     other option LAPD(lightweight Directory Access protol)

### Authorization strategy 
   By defult it see project-based authorization strategy with this we can manages authorization based on the option avaliable under strategy. EX:credential,Agents,Job,etc

### Martix Authorization strategy
    matrix authorization allows configuration the lowest level permission , such as strategy new builds,configuration item or delecting indivually.

### jenkins project(project or job both same)
     It is combinaation of one or more task

     free style project :Classic,genreal-purpose job type that checks out from upto one scm ,executes build steps serially, follwed by post-build steps like archiving artifacts and sending email notification.

     Maven project:Build a maven project. Jenkins takes advantages of your POM files and drastically reduces the congiguration.

     Pipeline:Orchestrates long-running activities that can span multiple build agents.Suitable for building pipelines (formely known as workflow )and/or organizing complex activities that do not easily fit in free-style job type.

     Multi-connguration project:sutible for project that need a large number of different configuration ,such as testing on mutiple enviroments, platform-specific builds,etc.

     Folder:create a container that stores nested items  in it.Useful for grouping things together.unlike view ,which is just a filter ,a folder create a separate namespace,so you can have mutiple things of the same name as a long as they are in different folder.

     Multibranch pipeline:create a set of pipeline project according to detected in one SCM repository.

     Organization folder:create a set of multibranch  project subfloders for repositories.

     Roles Based Access control one of the way secures jenkins 


### How to create Job or Project.

  In jenkins JUI > New item click on new item given the enter an item name Select item type once seleceted any of item then click on ok button highlighted. The job
  job configuration consistance of general(where we can give infromation or distrubution about project)

  The Next source code management where will be passing URL of the respository , Next build-Trigger [In what way we want trigger that job] , build Enviroment ,build steps[where we can add tasks] ,post-build Actions.


### How to get free Style:

   new item > give job name click ok once configurated go to build step congiguration click on add build step dropdown button 
   
   select==>executed window batch file dir in command and save next click build now .now you get out put.


### Blue Ocean

    Blue ocean rethinks the jenkins user experience Desinged from the group up for jenkins pipelines and compatible with freestyle jobs.

