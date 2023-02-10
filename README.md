This was a Continous Integration Pipeline I created using Jenkins, Github, SonarQube, Nexus, and Slack.  
- I utilized Jenkins and Maven to run the build process. 
- Github was used to store source code which was then fetched from Jenkins when a build was ran. 
- SonarQube was used for code analysis, including quality gates I configured. 
- Nexus was used to act as a software repository for the artifacts after the build was successful.  
- Slack was integrated with Jenkins to receieve notifcations when a build succeeded or failed.

For the infrastructure: I ran Jenkins, SonarQube, and Nexus on three different AWS EC2 instances. I configured the security groups accordingly so the servers could communicate with each other during the build process. 

Regarding software installation: I wrote Bash scripts and implemented them in the EC2 user data to automate the installation of Jenkins, Maven, SonarQube, and Nexus. 

I wrote pipeline as a code (PAAC) in DSL for the Jenkins pipeline.  In this code I included the necessary tools, various stages, steps, and post build actions for the pipeline to run correctly. 

During the process, I troubleshot Jenkins builds by referencing the console output/logs.  This allowed me to gain perspective on how to fix any issues with shell scripts, IP address configuration, and incorrect versions of dependencies. 

(https://user-images.githubusercontent.com/95970840/217977559-e47fe3a4-b2e9-4c31-97f5-939297ada647.png)
