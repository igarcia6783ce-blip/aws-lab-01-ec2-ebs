# > Note: Commands and configuration verified during live AWS lab session using EC2 + EBS.

# AWS EC2 + EBS Basic Volume Setup (Lab 01)

## Overview
This project demonstrates how to launch an EC2 instance, attach an EBS volume, and configure basic storage by formatting and mounting the volume on Linux.

## Next Steps
In the next lab, persistent mounting using fstab will be configured to ensure storage remains available after reboot.


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



### 4. Verification
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
