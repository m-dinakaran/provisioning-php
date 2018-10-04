# Cloud Formation Template to provision EC2 Instance with HTTPD & PHP: 

1) Use existing Key pair while running Cloud Formation Template. Else, please follow the below steps to create key pair using the Amazon EC2 console/ AWS CLI.  

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html

2) Run the Cloud Formation Template "Provision.yml"

Note: Template will create LAMP stack and updates System Timezone. Enter the Stackname, choose key pair value and proceed with creating stack. 

3) Update the PHP Timezone using the below command

sudo sh -c "echo 'date.timezone = Australia/Adelaide' >> /etc/php.ini"; sudo service httpd restart

4) Verify that "http://<your vm ip>/index.php" shows phpinfo and Timezone set to "Australia/Adelaide" both system wide and in PHP.

http://13.211.109.166/index.php
