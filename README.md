# end-to-end-cicd-pipelin
__________________________________
Are you looking forward to learn Jenkins right from Zero(installation) to Hero(Build end to end pipelines)? then you are at the right place.

## Install Jenkins.
---
### Pre-Requisites:

* Java (JDK)

### Run the below commands to install Java and Jenkins

#### Install Java
```bash
sudo apt update
sudo apt install openjdk-17-jre
```

#### Verify Java is Installed
```bash
java -version
```
Now, you can proceed with installing Jenkins
```bash
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
Login to Jenkins using the below URL:
http://IP_ADD_of_your_machine:8080
After you login to Jenkins, - Run the command to copy the Jenkins Admin Password
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
Enter the Administrator password

<img width="1717" height="791" alt="jenkins_mainpage" src="https://github.com/user-attachments/assets/a0f52d9b-34e5-4857-a173-80ae1233d68a" />
Click on install suggested plugin
<img width="1733" height="777" alt="jenkins_02" src="https://github.com/user-attachments/assets/3c8e99ea-a1b4-4184-91f6-810d27cfe5b5" />
Wait for the Jenkins to Install suggested plugins
<img width="1717" height="782" alt="jenkins_03" src="https://github.com/user-attachments/assets/33e197df-9776-4c03-acc0-7fa118a18891" />
Create First Admin User or Skip the step [If you want to use this Jenkins instance for future use-cases as well, better to create admin user]
<img width="1267" height="775" alt="jenkins_04" src="https://github.com/user-attachments/assets/c1b7549b-5158-4807-a658-b9f2ac3fb10b" />
Jenkins Installation is Successful. You can now starting using the Jenkins
<img width="1273" height="787" alt="jenkins_05" src="https://github.com/user-attachments/assets/7cbb382f-80d1-40b6-a0ae-7e09605a41d4" />

### Install the Docker Pipeline plugin in Jenkins:
___________________________________________________
* Log in to Jenkins.
* Go to Manage Jenkins > Manage Plugins.
* In the Available tab, search for "Docker Pipeline".
* Select the plugin and click the Install button.
* Restart Jenkins after the plugin is installed.

<img width="1713" height="688" alt="jenkins_06" src="https://github.com/user-attachments/assets/3208dad5-8f25-4a09-b015-38a5b657705c" />
Wait for the Jenkins to be restarted.

### Docker Slave Configuration
____________________________________

Run the below command to Install Docker
```bash
sudo apt update
sudo apt install docker.io
```

### Grant Jenkins user and Ubuntu user permission to docker deamon.
```bash
sudo su - 
usermod -aG docker jenkins
usermod -aG docker ubuntu
systemctl restart docker
```

Once you are done with the above steps, it is better to restart Jenkins.
```bash
http://Ip_add_of_your_machine:8080/restart
```

The docker agent configuration is now successful.
