# AWS EC2 + EBS Basic Volume Setup

## Project Overview
This project demonstrates how to attach an Amazon Elastic Block Store (EBS) volume to an Amazon EC2 Linux instance and mount it as usable storage inside the operating system.

The purpose of this lab was to understand how cloud block storage connects to a virtual server, how Linux identifies attached disks, and how a mounted volume becomes available through a directory such as `/data`.

---

## Objectives
- Launch and access an Amazon EC2 Linux instance
- Attach an additional Amazon EBS volume
- Identify the attached block device using Linux commands
- Create a mount point directory
- Mount the EBS volume to `/data`
- Validate that the volume is available to the operating system

---

## AWS Services Used
- Amazon EC2
- Amazon Elastic Block Store (EBS)
- EC2 Instance Connect
- Linux command line

---

## Architecture
Amazon EC2 Instance  
→ Attached Amazon EBS Volume  
→ Linux block device  
→ Mounted to `/data`

---

## Commands Practiced
lsblk
sudo mkdir /data
sudo mount /dev/xvdf /data
df -h

---

## What I Learned
This lab helped me understand how AWS EBS volumes work as attachable block storage for EC2 instances. I practiced identifying storage devices in Linux, creating a mount directory, mounting a volume, and validating that the operating system could access the additional storage.

---

## Outcome
Successfully attached and mounted an Amazon EBS volume to an EC2 Linux instance, proving that additional cloud storage can be connected and made available inside the server through a Linux mount point.

---

## Next Step

## Persistence Validation

The EBS volume was also configured for persistence by adding it to `/etc/fstab`. After rebooting the EC2 instance, the `/data` mount was tested again.

During validation, the UUID-based entry showed a boot source issue, so the configuration was corrected using the working device path:

```bash
/dev/nvme1n1 /data xfs defaults,nofail 0 2

The configuration was then validated successfully with:

sudo findmnt --verify

After reboot, the /data mount was available again and the test file was readable, confirming that the EBS volume persisted across reboots.



---

## Author
Ivan Garcia 
Cloud Engineering / AWS Hands-On Portfolio Project
