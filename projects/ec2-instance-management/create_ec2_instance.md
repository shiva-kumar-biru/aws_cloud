# Create EC2 Instance

Step 1. 

Go to your AWS account and log in, then search for EC2 Instances in the search bar. Or you can click on the services button that is on the top left corner of your dashboard, from there also you can search for the same.


**Home-->EC2-->Launch Instance**

![EC2instance](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_01.png)

Step 2.

Give a name of your choice, select Amazon Linux as a machine image, select your key-pair or create one if not have any. Leave the instance type t2.micro ie free tier as the same. Select **select existing security group** in network settings and select dropdown as "launch-wizard" and click on lauch instance on the bottom right

![EC2_instance_steps](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_02.png)

The instance is running as shown in the below image

![running_instance](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_03.png)


Step 3.

To know the details of the instance Id , click on the instance id . the following details such as private and public ip and the dns address and so on .. can be find here . 

the below shows the private and public ip addr of the Instance 

![info_about_instance](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_04.png)


Step 4. 

To run the instance on the laptop/local computer

- click on connect button
- Go to SSH client
- Go to terminal 
- navigate to the folder where the key is downloaded and do chmod 400 "abc.pem"
- ssh -i "abc.pem" ec2-user@ec2-publicipaddr.compute-1.amazonaws.com

![Run](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_05.png)


Step 5.

Instance is connected 

![Connected](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ec2_06.png)




# To create an EC2 instance with the EC2 user data to have a Website 

Before launching the instance, in the additional details, there is a user data section


```bash
#!/bin/bash



# Install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd

# Create a simple web page
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html

```

Verify the Web Server:

Open a web browser and navigate to the public IP of your EC2 instance. You should see the "Hello World" message:

http://your-ec2-public-ip

- First , you wont be able to see the "Hello World" on the browser
  
- To get the output, You have to change the security group settings , and allow port 80 for http 


![sg](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/hello_browser.png)

The output is 

[output](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/output.png)
