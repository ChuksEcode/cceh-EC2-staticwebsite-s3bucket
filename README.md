# Hosting an HTML Site on AWS EC2 Instance
This repository will walk you through the process of hosting an HTML site on an AWS EC2 instance. We'll cover setting up the instance, 
configuring security groups, and deploying your HTML files.The task entails uploading the web files to an S3 bucket, Creating a script 
that downloads the web files from the S3 bucket and hosts the HTML website on an EC2 instance. Then add the script to the EC2 user data
at launch to host the HTML website.


## Prerequisites
Before getting started, make sure you have the following:
1. An AWS account with necessary permissions to create and manage EC2 instances. Sign up for an AWS account at https://aws.amazon.com if you don't have one already.
2. AWS Command Line Interface (CLI) installed on your local machine.
3. A domain name (optional) to associate with your site.

## Step 1: Create an S3 Bucket
1. Log in to the AWS Management Console.
2. Navigate to the S3 service.
3. Click on the "Create bucket" button.
4. Provide a unique bucket name and select a region for your bucket.
5. Click on "Create" to create the S3 bucket.
6. Upload the Web Files
7. Select your bucket in the AWS Management Console.
8. Click on the "Permissions" tab.
9. Click on "Bucket Policy" or "Access Control List" depending on your requirements.
10. Configure the necessary permissions to allow public access. trol.

## Step 2: Launch an EC2 Instance
1. Log in to your AWS Management Console.
2. Choosing an AWS Region
3. Navigate to the EC2 service. I will be using the default region Northern Virginia
4. Click on the "Launch Instance" button.
5. Choose an Amazon Machine Image (AMI) that suits your requirements (e.g., Amazon Linux 2).
6. Select an instance type based on your needs and click "Next".
7. Configure the instance details such as the number of instances, network settings, and storage.
8. Configure security groups to allow inbound traffic on port 80 (HTTP) and 22 (SSH).
9. Review the instance details and click "Launch".
10. Select or create a key pair for SSH access and click "Launch Instances".

## Step 3: Connect to the EC2 Instance
1. Once the instance is launched, note down the public IP or public DNS of the instance from the EC2 dashboard.
2. Open a terminal or command prompt on your local machine.
3. Use the SSH command to connect to your instance: ssh -i <path_to_key_pair> ec2-user@<public_ip_or_dns>.
4. If prompted, confirm the connection by typing "yes".

## Step 4: Script Development
This script should have the functionality to download the web files from the S3 bucket 
and host your HTML website on an EC2 instance. Keep in mind that ensuring the script's 
accuracy is crucial for the successful execution of the operation.




