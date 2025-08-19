## Deploying index.hml using Jenkins Pipeline

Steps
1. Install Plugins in jenkins - git server,git push,git parameter, github integration,pipeline SCM API for Blue Ocean
2. Create a github repo push index.html & Jenkinsfile in repo
3. Create pipeline - 
  - Triggers - poll SCM - schedule - *****
  - Pipeline - Pipeline script from SCM 
               SCM - Git
               Repository Url - current repo
               Branch - main
               Script path - Jenkinsfile
4. Save & Build