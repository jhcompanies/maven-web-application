Maven installation
Preriquisites
    AWS Acccount.
    Create Security Group and open Required ports.
        22 ..etc
    Create Redhat EC2 T2.medium Instance with 4GB of RAM.
    Attach Security Group to EC2 Instance.
    Install java openJDK 1.8+

    # install Java JDK 11+ as a pre-requisit for maven to run.

#!/bin/bash
# to install Maven
sudo hostnamectl set-hostname maven
sudo su - ec2-user
cd /opt
sudo yum install wget nano tree unzip git-all -y
sudo yum install java-11-openjdk-devel java-1.8.0-openjdk-devel -y
java -version
git --version
sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.5/binaries/apache-maven-3.9.5-bin.zip
sudo unzip apache-maven-3.9.5-bin.zip
sudo rm -rf apache-maven-3.9.5-bin.zip
sudo mv apache-maven-3.9.5/ maven

