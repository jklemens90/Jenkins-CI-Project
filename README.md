This was a Continous Integration Pipeline I created using Jenkins, Maven, Github, Checkstyle, SonarQube, Nexus, and Slack.  
- Source code was stored in Github, which was then fetched from Jenkins when a build was initiated.
- Maven was used to run the build process. 
- Checkstyle and SonarQube were used for code analysis, including custom Sonar quality gates I configured. 
- If the build passed the quality gates, Nexus receieved the artifacts and stored them in a software repository. 
- Slack was integrated with Jenkins to receieve notifications when a build succeeded or failed.

For the infrastructure: I ran Jenkins, SonarQube, and Nexus on three different AWS Linux EC2 instances. I configured the security groups accordingly so the servers could communicate with each other during the build process. 

Regarding software installation: I wrote Bash scripts and implemented them in the EC2 user data to automate the installation of Jenkins, Maven, SonarQube, and Nexus. 

I wrote pipeline as a code (PAAC) in DSL for the Jenkins pipeline.  In this code I included the necessary tools, various stages, steps, and post build actions for the pipeline to run correctly. 

During the process, I troubleshot Jenkins builds by referencing the console output/logs.  This allowed me to gain perspective on how to fix any issues with shell scripts, IP addresses, and incorrect versions of dependencies. 

![Stage view](https://user-images.githubusercontent.com/95970840/217977719-91bb576b-c1d5-4d78-a5a7-eb702794b681.png)
![Sonar analysis](https://user-images.githubusercontent.com/95970840/217977739-0db24f44-73ec-452d-9644-c7229f425828.png)
![Nexus Repository](https://user-images.githubusercontent.com/95970840/217977761-25c4f8e7-686d-4371-b4b8-3ff437f395ae.png)

