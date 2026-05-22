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

Verify Java is Installed
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
