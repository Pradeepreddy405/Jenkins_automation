# Learn Jenkins automation
Jenkins A to Z
What is Jenkins ?

Installation of Jenkins an AMAZON LINUX
1.	Check for system updates on Amazon Linux by using the below command 
sudo yum update -y

2.	Adding the Jenkins repo to Amazon linux
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo

3.	We need to import the key from Jenkins repo manually
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

4.	Upgrade 
sudo yum upgrade -y

5.	Jenkins is a Java-based open-source server that runs on any server. Jenkins runs on Java, you need either latest version of Java Development Kit (JDK) or Java Runtime Environment (JRE).
Note : Before going to install java . Just check weather Jenkins compatible with java 11 or java 17 .
sudo dnf install java-17-amazon-corretto -y

6.	After java installation. check the java version by using the below command.
Java –version

7.	Installing Jenkins
sudo yum install jenkins -y
 
8.	systemctl : The systemctl command is a Linux utility that manages and interacts with the systemd system and service manager.

systemd is used to manage system settings and services. i.e to operate the particular services by using the instructions like start , stop , restart , reload , enable and disable 
     Some common systemctl commands are :  start, stop, restart,  reload, enable, and disable

9. To enable the jenkins service
    sudo systemctl enable jenkins
   
10.To start the jenkins servece
    sudo systemctl start jenkins
    
11. We need to expose the jenkins port on the instance/server where the jenkins is running on.
12. In Amazon cloud >Ec2 instance > security groups > inbound rules > Add rule : tcp 8080 > Save changes
13. Restart the jenkins service by using the below command
    sudo systemctl restart jenkins
   
