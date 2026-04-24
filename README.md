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
  
## Architecture
EC2 (Linux) instance with an attached EBS volume mounted to /data


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



## Skills Demonstrated
- AWS EC2 provisioning
- AWS EBS storage management
- Linux disk administration
- Filesystem mounting
- Persistent storage configuration
- Cloud infrastructure fundamentals

## Outcome
Successfully launched an EC2 instance, attached an EBS volume, and mounted it to the Linux filesystem.

## Author
Ivan Garcia  
Aspiring Cloud Engineer (AWS)
