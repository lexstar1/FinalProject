# Capstone Certification Project
This project is about how to do deploy code to dev/stage/prod etc, just on a click of button.

As soon as the developer pushes the updated code on the GIT master branch, a new test server should be provisioned with all the required software. Post this, the
code should be containerized and deployed on the test server. The deployment should then be tested using a test automation tool, and if the build is successful, it should be pushed to the prod server. All this should happen automatically and should be triggered from a push to the GitHub master branch.

Use the Master VM for Jenkins, Ansible, Puppet, GIT
![Screenshot (109)](https://user-images.githubusercontent.com/59297711/97795314-2d7ebb00-1bdb-11eb-9d1b-68c7586fedd7.png)


Ubuntu VM image for 
Jenkins Slave Node 

![Screenshot (102)](https://user-images.githubusercontent.com/59297711/97795343-6fa7fc80-1bdb-11eb-9aaf-5100aeb09ebe.png)
![Screenshot (103)](https://user-images.githubusercontent.com/59297711/97795350-83ebf980-1bdb-11eb-9537-1e80cd7798fd.png)

Add Build Pipeline Plugin and Post-build task
plugin to Jenkins on the master VM

![Screenshot (105)](https://user-images.githubusercontent.com/59297711/97795359-a1b95e80-1bdb-11eb-89bf-fd07df5790c6.png)


Install python, openssh-server and 
git on the slave node manually

![Screenshot (106)](https://user-images.githubusercontent.com/59297711/97795365-b7c71f00-1bdb-11eb-8f36-742909dae7bc.png)


Set up the necessary tools such as 
git, chromedriver(selenium), chromium browser(selenium)
on the slave node through Ansible

![Screenshot (81)](https://user-images.githubusercontent.com/59297711/97795380-e93fea80-1bdb-11eb-9216-ea2f4a6df2f3.png)
![Screenshot (80)](https://user-images.githubusercontent.com/59297711/97795381-e9d88100-1bdb-11eb-8ccc-b850d671c5f6.png)

Use the docker image and add your PHP website
to it using a Dockerfile and Push the PHP website, 
Dockerfile and Selenium JAR to a git repository

![Screenshot (108)](https://user-images.githubusercontent.com/59297711/97795072-4e91dc80-1bd8-11eb-8330-c8f9ff90231b.png)
![Screenshot (107)](https://user-images.githubusercontent.com/59297711/97795085-649f9d00-1bd8-11eb-8db6-d34af9df60be.png)

Create a Selenium Test for your PHP website. 
It should click on “About” and verify the text
written in it. This will conclude the website 
is deployed and is running fine.

![Screenshot (88)](https://user-images.githubusercontent.com/59297711/97795399-2b692c00-1bdc-11eb-9ef2-1ddd3d66a7b6.png)
![Screenshot (91)](https://user-images.githubusercontent.com/59297711/97795400-2b692c00-1bdc-11eb-9d0e-af95c5933317.png)
![Screenshot (89)](https://user-images.githubusercontent.com/59297711/97795401-2c01c280-1bdc-11eb-9a1f-722e3fd0ba0f.png)


Jenkins Pipeline Tasks:
Install and configure puppet agent 
on the slave node (Job 1)

![Screenshot (110)](https://user-images.githubusercontent.com/59297711/97795435-7a16c600-1bdc-11eb-8ebf-7ea4bd6fbb13.png)

Sign the puppet certificate on 
master using Jenkins (Job 2)

![Screenshot (112)](https://user-images.githubusercontent.com/59297711/97795437-7aaf5c80-1bdc-11eb-97fe-6244830f4501.png)

Trigger the puppet agent on test 
server to install docker (Job 3
)

![Screenshot (111)](https://user-images.githubusercontent.com/59297711/97795466-e5f92e80-1bdc-11eb-8fda-b2c44211d4b4.png)
![Screenshot (114)](https://user-images.githubusercontent.com/59297711/97795467-e691c500-1bdc-11eb-9996-f69335f12a4c.png)

Pull the PHP website, Dockerfile and Selenium JAR from your
git repo and build and deploy your PHP docker container.
After this test the deployment using Selenium JAR file. (Job 4)

![Screenshot (115)](https://user-images.githubusercontent.com/59297711/97795480-25c01600-1bdd-11eb-85be-c686f744c1bc.png)
![Screenshot (117)](https://user-images.githubusercontent.com/59297711/97795481-25c01600-1bdd-11eb-9cae-843f914c43ea.png)

Built image running as container:

![Screenshot (116)](https://user-images.githubusercontent.com/59297711/97795482-2658ac80-1bdd-11eb-895b-7cdbbf66a81b.png)
![image](https://user-images.githubusercontent.com/59297711/97795143-e7285c80-1bd8-11eb-9a25-be87b78202fc.png)



