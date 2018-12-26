# ZaMvnRepo
Za Maven Repository Demo

## Local(Lan) Maven Repository
Nexus Repository:
    http://10.203.3.63:8081 
    
    docker run -d -p 8081:8081 \
        --name qj-nexus sonatype/nexus3:3.0.0  
        -v /home/latti/bin/nexus-data:/nexus-data

   Setup Maven Repo you can refer to:
        [using-nexus-3-as-your-repository](https://blog.sonatype.com/using-nexus-3-as-your-repository-part-1-maven-artifacts)


## jlib

A demo java lib project.

You can focus on "distributionManagement" in its pom.xml file.

 `> deploy -e -X`
 
 But you must setup user info in maven's settings.xml in ${MVN_HOME}/conf folder
 
  ```
     <server>
       <id>jlib-snapshot</id>
       <username>your-repo-user</username>
       <password>your-repo-password</password>
     </server>
  ```
  
 ## jmain
 
 A normal java application used to test the jlib in your own maven repo.
 
 You can mention `repositories` in its pom file.
 
 