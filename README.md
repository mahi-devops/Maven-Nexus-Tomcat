# Build a sample java project
```
1. download maven - binary zip file and extract
2. downlad java - .exe file
3. setup path for both maven and java.
4. check java version on command prompt - jave -version
5. check maven version on cmd - mvn -v

Run the below command to generate pom.xml file:
mvn archetype:generate  -DgroupId=in.javahome -DartifactId=pets-app -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false

1. In the github create a repository named pets-app
2. open the pom.xml location and do gitbash 
3. follow the steps from readme file of pets-app.
```
# Nexus
```
1. Create a free AWS account.
2. Launch EC2 instance with t2 medium for Nexus.
3. Connect to Nexus(EC2 instance) using putty or mobaexterm.
```
# Creating an EC2 instance for Nexus
```
1. select launch instance 
2. select t2 medium for nexus
3. Add tags - Name: nexus3
4. Create a security group
5. select Review and launch 
```
# Installing nexus on linux machine
```
```
