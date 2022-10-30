### CMPE 272 - HW-5 Jenkins
Team Name: Spartan Devs <br/>
Team Members: <br/>
Bhavya Hegde - 016656029 <br/>
Darshini Venkatesha Murthy Nag - 016668951 <br/>
Sirisha Polisetty - 016012477 <br/>

*Setup and run jenkins on a ec2 instance on aws
Launch an ec2 instance

![Ec2](https://user-images.githubusercontent.com/103618216/198853089-2cd9604b-2699-485c-9c9a-1d4c8a1f95e1.png)


### Download dependencies and install Jenkins on Ec2
* [ec2-user ~]$ sudo yum update –y
* [ec2-user ~]$ sudo wget -O /etc/yum.repos.d/jenkins.repohttps://pkg.jenkins.io/redhat-stable/jenkins.repo
* [ec2-user ~]$ sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
* [ec2-user ~]$ sudo yum upgrade
* [ec2-user ~]$ sudo amazon-linux-extras install java-openjdk11 -y
* [ec2-user ~]$ sudo yum install jenkins -y
* [ec2-user ~]$ sudo systemctl enable jenkins
* [ec2-user ~]$ sudo systemctl start jenkins
* [ec2-user ~]$ sudo systemctl status jenkins

### Login to Jenkins and Install Plugins

![login](https://user-images.githubusercontent.com/103618216/198853491-8da321da-174a-4f5e-ab96-e8f703d88727.png)

### Create a personal token in github then add this token details in jenkins.

![ps](https://user-images.githubusercontent.com/103618216/198853564-dc5d6822-0a87-4e30-a86e-9d19407c11fb.png)

### Added the personal token to jenkins configure system under github Servers

![addps](https://user-images.githubusercontent.com/103618216/198853582-59f1ad9b-8cb9-4c6b-82ac-7ec0890ca1c9.png)


### Create a Repo in github and add jenkins webhook to send events to jenkins

![repo](https://user-images.githubusercontent.com/103618216/198853595-a59fd753-8df7-4c6e-9489-e67093a27638.png)

### Created a  jenkins job for the repo which we are sending events through jenkins webhook

![repo1](https://user-images.githubusercontent.com/103618216/198853613-367f36bc-878c-4373-bb10-f3ffb8ca4e31.png)

### Build Trigger : Github hook trigger for GITScm Polling
![build](https://user-images.githubusercontent.com/103618216/198853635-a24d4ca5-205e-4740-8bd8-3aa091d85ecf.png)

### Webhook triggers

![web](https://user-images.githubusercontent.com/103618216/198853652-195b7e44-9f92-49b9-8bc4-07094fc0ad86.png)

### Jenkins Job Configuration Setup
![jen](https://user-images.githubusercontent.com/103618216/198853669-fb5cf58c-6b05-464d-b117-3b6bf297127a.png)
![jen1](https://user-images.githubusercontent.com/103618216/198853707-b4c70f64-0026-4d9e-a05d-f7615ae8455c.png)

![jen2](https://user-images.githubusercontent.com/103618216/198853711-744d90df-235e-4ea0-ba35-d9e9d6d30711.png)

### Jenkins Status are showing up on github commits
![commit](https://user-images.githubusercontent.com/103618216/198853746-f58883cb-d1c8-43c2-ac83-259a3e862d18.png)

### Github check is set up as mandatory on branch protection rules for to be merged to main.
![branch](https://user-images.githubusercontent.com/103618216/198853770-0bfb7586-07a7-4e3a-aee7-a360fcc2b832.png)


### 
