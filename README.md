# Automating-Loadbalancer-Configuration-With-Shellscripting
Deployment of Nginx as a Load balancer using shell script


## Deploying and configuring the webservers

we need to codify the process we need to deploy in the shell scripting.

__Follow the steps below to run the script :__

__step 1:__ provision an Ec2 instance running on ubuntu 20.04.

Result:

![](./images/1.png)

__step2:__ open port 8000 to allow traffic from anywhere using the security group.

Result:

![](./images/2.png)


__step 3:__ connect to the webserver via the terminal using SSH client.

Result:

![](./images/3.png)

__step 4:__ open a file

Results:

![](./images/4.png)

![](./images/7.png)


__step 5:__ Run the shell script using this command: `./install.sh 54.177.88.13 (your public_ip address)`

Results:

![](./images/8.png)


![](./images/9.png)


__Deploying and configuring Nginx load balancer__

we need to provision an Ec2 instance `Nginx-loadbalancer` running ubuntu 22.04 and then open port 80 using the security group.

Results:

![](./images/10.png)

![](./images/11.png)




__step1:__ connect to your web browser using SSH client 

![](./images/12.png)



__step2:__ On your terminal, open a file `nginx.sh` and change the permission on the file to make it executable.

![](./images/13.png)

__step3:__ Run this command `sudo vi nginx.sh` and paste your file then close the file by typing `Esc shift + :wq!`.

First digits is the public IP address of the EC2 instance where Nginx is installed.


Second digits is the URL and port number of the first webserver to which the load balancer will distribute traffic.

Third digits is the URL and port number of the second webserver to which the load balancer will distribute traffic.


Results:

![](./images/24.png)

![](./images/25.png)


Result for webserver 1:

![](./images/26.png)



Result for webserver2:

![](./images/27.png)



Result for loadbalancer:




![](./images/22.png)


![](./images/23.png)














































































