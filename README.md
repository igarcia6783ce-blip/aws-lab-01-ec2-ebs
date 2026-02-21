# > Note: Commands and configuration verified during live AWS lab session using EC2 + EBS.

## Overview 
This hands-on AWS lab demonstrates
launching an Ec2 instance, attaching and mounting an EBS volume, and configuring persistent  storage on Linux. 

## Objectives
 > Lab performed in AWS console and Linux shell environment.

##Architecture 
EC2 (Linux) attached EBS Volume 
Mounted to /data- Persistent via fstab 
## Steps Performed 
### 1. Launching EC2 Instance 
-Amazon Linux instance  deployed 
-SSH access  configured 
-Key pair authentication used
### 2. Create and attach EBS volume 
-New EBS volume created in same AZ
-Volume attached to EC2 instance 
### 3. Format and Mount Volume 
Commands used:

Isblk sudo mkfs-txfs/dev/xvdf sudo mkdir/data sudo mount /dev/xvdf/data

### 4. Configured Persistent Mount

sudo blkid sudo nano/ect/fstab

UUID entry added to fstab for automatic  mount.

### 5. Verification 
-Instance rebooted 
-Volume automatically Mounted
-Data persisted after reboot

## Skills Demonstrated 
-AWS EC2 provisioning 
-AWS EBS storage management 
-Linux disk administration 
-Filesystem mounting 
-Persistent storage  configuration 
-Cloud infrastructure  fundamentals 

## Outcome 
Successfully configured  persistent block storage on AWS EC2 using EBS and Linux fstab. 

## Author
Ivan Garcia 
Aspiring Cloud Engineer (AWS)

