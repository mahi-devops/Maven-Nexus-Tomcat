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
    1.  cd /opt/
    2.  sudo wget https://download.sonatype.com/nexus/3/latest-unix.tar.gz
    3.  sudo tar -xf latest-unix.tar.gz
    4.  sudo mv nexus-3.25.0-03/ nexus3
    5.  sudo chown -R ec2-user: ec2-user nexus3/ sonatype-work
    6.  sudo rm -rf latest-unix.tar.gz
    7. sudo yum list | grep java-1.8
    8. sudo yum install java-1.8.0-openjdk-devel.x86_64 -y
    9. cd nexus3/
   10.  cd bin/
   11. ./nexus start
   12. ./nexus status
```
# To open Nexus in the browser
```
IPv4 Public IP:Default port of nexus
IPv4 Public IP:8081

first sigin to Nexus.
UN: admin
pwd: cat LINK FROM THE SIGNIN PAGE
```
# Configure nexus as a service
```
    vi /opt/nexus3/bin/nexus.rc
    run_as_user="ec2-user"
    sudo ln -s /opt/nexus3/bin/nexus /etc/init.d/nexus
    
    cd /etc/init.d
    sudo chkconfig --add nexus
    sudo chkconfig --levels 345 nexus on
    sudo service nexus start
```
