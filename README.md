# git-strawberry

# Plain Dosa
git add .;git commit -m"plain dosa started ,dosa batter added";git push origin plain-strawberry
git log --one-line
git cat-file -p <commit>
ex: git cat-file -p a32def

* Merge Commit is a special commit which has 2 parents
* Other commits has only 1 parent

* Merge vs Rebase ?
a) merge creates extra commit called merge commit, Rebase does not create extra commit
b) merge preserves the history , rebase does not preserve the history
c) Rebase rewrites the history, it will change commit id.
d) Rebase has linear history, merge has circular history

when to use Merge vs Rebase ?
* if a branch is shared among multiple members, if you want to preserve the history, go for merge. Long releases, waterfall model
* if it is vigirous agile or microservices development, usually a branch is owned by single person , then go for rebase..



#karam Dosa
* Dosa batter
* Errakaram

- Merge Conflicts
* git checkout main; git pull
* git checkout egg-dosa-ramesh
* git merge main
* sit & resole conflicts
* git commit <resolved conflicts>

### Branching Strategy
1. What are the branches
2. How you bring changes from Dev to PROD
3. other branches to main/master branch

* git flow -> master develop release feature and hotfix --> suitable for waterflow model
* feature branch  -> main merge --> suitable for agile , devops, microservices
* trunk based 


* what are long lived branches?
In git flow --> master develop

* what are short lived branches?
In git flow -> feature release and hotfix

main/master --> always points to PROD

develop -> long lived branches -> always points to active development which is going on
-------
source -> main/master
destination -> main/master

short-lived branches:
--------------------

feature-1 branch -- lifetime until merge to develop branch
source is develop
destination is develop

clone --> build --> unit test cases --> scans --> create image --> push image

If success -> successfully merge into master branch

feature-2 branch:-- lifetime until merge to develop branch
-----------------
1. pull the changes from develop
2. merge/rebase 
3. raise PR & merge to develop branch

Release = New features + Bug fixes + improvements

Release branch -> short lived branch --> example: release-1.3
-------------
1. Source is development
2. Destination is master/develop
3. lifetime is until release completes & sent to PROD. You get the changes to master/main

then deploy into env Dev/QA/UAT & test the application
deploy to PROD. If successfully deployed, then you merge these changes into master or main

once deployment is successfull, then merge release branch into master/main & develop & successfully delete release branch


For new release --> create release branch

git flow is suitable for waterfall model

product based has to support multiple versions at a time --> 20,19,18,17
git checkout release-18

Hot Fix: (Emergency Defect)
---------------------------
SLA --> Service Level Agreement 
priority - 1 --> max 4 hours --> Address immediately (Business shut-down)

source: main
destination: develop and /main

new branch name: hotfix-emergency-ticket-price --> direct approval from Chairman/CEO
test it in develop once & deploy it to PROD. 

After hotfix Success, get the changes both into main & develop


********************************************************************

feature branching strategy:
----------------------------
only 2 branches master/main & feature branch

* web apps will not have any versions (facebook,whatsapp)


From master, create feature branch, then
clone --> build --> unit test cases --> scans --> create image --> push image

merge to main --> QA, UAT,SIT,PROD

For hotfix:
From main create hotfix branch & then deploy to DEV -> merge the changes to main -> deploy to PROD

Trunk based:
-----------
main branch -> only 1 branch -> implemented in startups



* git reset
* git revert
* git squash
* git stash
* git cherry-pick

