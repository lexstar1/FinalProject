# Capstone Certification Project
This project is about how to do deploy code to dev/stage/prod etc, just on a click of button.

As soon as the developer pushes the updated code on the GIT master branch, a new test server should be provisioned with all the required software. Post this, the code should be containerized and deployed on the test server. The deployment should then be tested using a test automation tool, and if the build is successful, it should be pushed to the prod server. All this should happen automatically and should be triggered from a push to the GitHub master branch.

Use the Master VM for Jenkins, Ansible, Puppet, GIT
![image](https://user-images.githubusercontent.com/59297711/97794948-b0514700-1bd6-11eb-8062-1470300e095e.png)

Ubuntu VM image for Jenkins Slave Node 
![image](https://user-images.githubusercontent.com/59297711/97795006-543af280-1bd7-11eb-8b69-3df89f4e21f6.png)
![image](https://user-images.githubusercontent.com/59297711/97795012-66b52c00-1bd7-11eb-8374-a4a93f559df9.png)

Add Build Pipeline Plugin and Post-build task plugin to Jenkins on the master VM
![image](https://user-images.githubusercontent.com/59297711/97795019-80ef0a00-1bd7-11eb-813e-db07db560b77.png)
![image](https://user-images.githubusercontent.com/59297711/97795023-9f550580-1bd7-11eb-96f8-66e0b8ede87b.png)

Install python, openssh-server and git on the slave node manually
![image](https://user-images.githubusercontent.com/59297711/97795025-b09e1200-1bd7-11eb-8588-24ae12ba8bcf.png)

Set up the necessary tools such as git, chromedriver(selenium), chromium browser(selenium) on the slave node through Ansible
![image](https://user-images.githubusercontent.com/59297711/97795027-bb58a700-1bd7-11eb-9405-817caae2bef7.png)
![image](https://user-images.githubusercontent.com/59297711/97795036-d3c8c180-1bd7-11eb-96f5-1231b16494e1.png)

Use the docker image and add your PHP website to it using a Dockerfile and Push the PHP website, Dockerfile and Selenium JAR to a git repository
![Screenshot (108)](https://user-images.githubusercontent.com/59297711/97795072-4e91dc80-1bd8-11eb-8330-c8f9ff90231b.png)
![Screenshot (107)](https://user-images.githubusercontent.com/59297711/97795085-649f9d00-1bd8-11eb-8db6-d34af9df60be.png)

Create a Selenium Test for your PHP website. It should click on “About” and verify the text written in it. This will conclude the website is deployed and is running fine.
![image](https://user-images.githubusercontent.com/59297711/97795102-839e2f00-1bd8-11eb-976f-04056620db54.png)

Jenkins Pipeline Tasks:
Install and configure puppet agent on the slave node (Job 1)
![image](https://user-images.githubusercontent.com/59297711/97795114-987ac280-1bd8-11eb-9c23-b0aa219e8c05.png)

Sign the puppet certificate on master using Jenkins (Job 2)
![image](https://user-images.githubusercontent.com/59297711/97795124-ac262900-1bd8-11eb-89e4-5ab87d1698bf.png)

Trigger the puppet agent on test server to install docker (Job 3)
![image](https://user-images.githubusercontent.com/59297711/97795128-c233e980-1bd8-11eb-88d4-682f6b89f37d.png)

Pull the PHP website, Dockerfile and Selenium JAR from your git repo and build and deploy your PHP docker container. After this test the deployment using Selenium JAR file. (Job 4)
![image](https://user-images.githubusercontent.com/59297711/97795131-ccee7e80-1bd8-11eb-8180-953c51dda2f3.png)

Built image running as container:
![image](https://user-images.githubusercontent.com/59297711/97795139-daa40400-1bd8-11eb-96f3-3496c9c1be57.png)
![image](https://user-images.githubusercontent.com/59297711/97795143-e7285c80-1bd8-11eb-9a25-be87b78202fc.png)



