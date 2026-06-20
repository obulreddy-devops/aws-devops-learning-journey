## AWS Hands on practice ##
# What i did today #
Today I performed real AWS hands-on tasks using EC2 IAM and S3 services.
----
## IAM (Identity access management) 🔐 ##
--created IAM Role.
--Attached permissions to EC2 Instances
--Fixed AWS CLI permission issues
👉 IAM Role helped to EC2 to securely access AWS services like s3 without using access keys.
----

----
## EC2 (Elastic compute cloud) ##
--Launched EC2 instance(t3.micro)
--connected using SSH from local machine
--used EC2 as a linux server in Aws cloud
👉 EC2 act as a linux server in AWS cloud
----

----
## S3 (simple storage service) ##
--crated s3 bucket
--upload files from ec2 to s3 unsing aws cli
--verified uploaded files in s3 bucket
👉 S3 used as cloud storage for files.
----

----
## AWS CLI Operations (Real practice)
From EC2 server, I performed:
-created a text file
'''bash
echo "Hello AWS Devops" >test.txt
----

## Commands used inside ec2 linux server ##
--create s3 bucket--
aws s3 mb s3://s3-bucket-name(unique)

--list s3 bucket--
aws s3 ls

--create a file --
echo "Hello AWS Devops" >test.txt

--check a file --
cat test.txt

--upload file to s3 --
aws s3 cp test.txt s3://s3 bucket name

--Download a file --
aws s3 cp s3://s3 bucket name

--sync folder with s3 --
aws s3 sync . s3:// s3 bucket name

-- verify s3 content --
aws s3 ls:// s3 bucket name

--check iam role very important --
bash
aws sts get-caller-identity

### END TO END FLOW ### 
EC2 Server → create file (linux commands) →AWS CLI (IAM Role authentication) →S3 Bucket (Upload /Download/ Sync)

### Key learning ###
EC2 = Cloud linux server
IAM Role = Secure AWS permissions
S3 = Storage system
 AWS CLI = Automated tool
Real Devops = EC2 + IAM + S3 integration

##Interview##
I performed AWS CLI-Based automation using EC2, IAM Role, and s3 integration with real file transfer
