# > Note: Commands and configuration verified during live AWS lab session using EC2 + EBS.

# AWS EC2 + EBS Persistent Storage Lab

## Overview
This hands-on AWS lab demonstrates launching an EC2 instance, attaching and mounting an EBS volume, and configuring persistent storage on Linux.

## Objectives
- Launch EC2 instance in AWS
- Create and attach EBS volume
- Format and mount EBS volume
- Configure persistent mounting using fstab
- Verify persistent storage after reboot

## Architecture
EC2 (Linux) with attached EBS volume mounted to /data and persisted via fstab.

## Steps Performed

### 1. Launching EC2 Instance
- Amazon Linux instance deployed
- SSH access configured
- Key pair authentication used

### 2. Create and Attach EBS Volume
- New EBS volume created in same Availability Zone
- Volume attached to EC2 instance

### 3. Format and Mount Volume
Commands used:

```bash
lsblk
sudo mkfs -t xfs /dev/nvme1n1
sudo mkdir /data
sudo mount /dev/nvme1n1 /data
```

### 4. Configure Persistent Mount
Commands used:

```bash
sudo blkid
sudo nano /etc/fstab
sudo mount -a
```

UUID entry added to /etc/fstab for automatic mount.

### 5. Verification
- Instance rebooted
- Volume automatically mounted
- Data persisted after reboot

## Skills Demonstrated
- AWS EC2 provisioning
- AWS EBS storage management
- Linux disk administration
- Filesystem mounting
- Persistent storage configuration
- Cloud infrastructure fundamentals

## Outcome
Successfully configured persistent block storage on AWS EC2 using EBS and Linux fstab.

## Author
Ivan Garcia  
Aspiring Cloud Engineer (AWS)