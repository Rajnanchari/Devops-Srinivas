Topics 

.version control
.Git introduction
.Git Installion

Why need version control system?

   .collaboration
   .storing version
   .figuring out what happended
   .backup


   What is Version Control

     Version control is a system that documents changes mode to file or set of files It allows multiple user to manage multiple revisions of the same unit of information. It is sanpshot of ypur project overtime.

     Local version control
     the practies of having the version DB in the local computer 

     issuse:multiple people parally working on the same project
     solution:centralized version control

 Centralized version control:

 local version control issuse are resloved by centralized version control 
 In cvc, a central respository is maintained where all the versinned file are kept
 now user can checkout and checkin file from their diff computer at any time

 issuse:incase of central server faliure whole system goes down

 solution:Distributed version control

 Distributed version control(DVC)

 .version DB IS stored at every user local system and at the remote server
 .user manipulated the local files and then upload the change to remote server 
 .If any of the server die , a client server can be to sestored.


 What is Git :

    Git is an open source Distributed version control system (DVCS) which is records changes mode to the files laying emphasis on speed , data integrity and distributed non -liner workflow.

 Git workflow:
  The Remote Respository is the server where all the collaborators upload changes made to the file


  image

  .LOcal Repository is user copy  of the version DB
  .the user accesses all the files through local repository and then push the change made to the Remote Repository

  Workspace is user active directory

   .The user modifies existing files and create new file in this space.Git tracks the change.

   Stage is a place where all the modified files marked to be commintted are placed

   clone command commints all the files in the staging area to the local repository.

   .commit command commits all the files in the staging area to the local repository

   .push commandpushes all the changes made in the local repository to the remote repository

   .Fetch command collects the change made in the remote repository  and copies them to the local repository.This  command does not affect our workspace.

   .Pull like Fetch  gets all changes from remote repository and copies them to the local repository 
   .pull merges those changes to the current worrking directory.   


Git Braching Stragy:

Base-main-Major-sanpshot of project

Dev
QA/Test
Releases Branch
Features
hotfix-production-Base

git -- help


collaboratols ==>add team member
personal acess token ==>A/c security purpose used 

.git commit -am ===>it  will working on exiting file
.git commit -m ====> it will working on new file
.git commint --amend ===> we can replace or mofified exiting file  msg 
.git commit --amend -m "taskid:22 this is "
.Before push after commit back the file using revert. once use git revert local data not reflect file.
.Adding a tag to one of the previsous commit 
   syntax :git tag -a <annotation> <commitid > -m <msg>
   commit id can be obtained from git logs

.All these tages can be viewd in git 
    git show <tagname>
 git push --tag ==>To push tag remote repository

 git cherry-pick commit_ID enter

 When you can create local branch push to remote we get got this msg
    git push --set -upstream origin test

 fork is a copy of repository forking a repository allow you to freely experiment with change affecting the original project   


