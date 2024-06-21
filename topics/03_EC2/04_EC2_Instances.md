# EC2 INSTANCE STORAGE


## Types of EC2 Storage

- **Amazon Elastic Block Store (EBS)**
- **Instance Store**
- **Amazon Elastic File System (EFS)**



## EBS Volumes and EBS Snapshots

### What are EBS Volumes?

- EBS (Elastic Block Store) volumes are storage you can attach to your EC2 instances. Think of them like hard drives for your cloud servers.

- They bound to specific availabilty zone

- It can be detached from an EC2 instance and attach to another instance quickly

- To move volume accross , you need to snapshot it first


### Types of EBS Volumes:

1. **General Purpose SSD (gp2/gp3)**: Good for general use.
2. **Provisioned IOPS SSD (io1/io2)**: High performance for heavy use.
3. **Throughput Optimized HDD (st1)**: Good for big data and large logs.
4. **Cold HDD (sc1)**: Cheapest option for rarely accessed data.

### Benefits:
- **Persistent Storage**: Keeps data even if the server stops.
- **Scalable**: Easy to resize.
- **Flexible**: Can attach/detach from servers as needed.
- **Secure**: Data can be encrypted.

## What are EBS Snapshots?

EBS Snapshots are backups of your EBS volumes. They are stored in S3 (Simple Storage Service).

### Benefits:
- **Data Protection**: Helps to back up your data.
- **Scalability**: Quickly restore and launch instances from snapshots.
- **Cost-Effective**: Only changed data is saved after the first snapshot.

### How Snapshots Work:
- **First Snapshot**: Full copy of the volume.
- **Next Snapshots**: Only the changes since the last snapshot are saved.

## Common Uses:
- **Backups**: Regularly back up your volumes.
- **Disaster Recovery**: Quickly recover data if something goes wrong.
- **Migration**: Move data between regions or instances.

## EBS snapshot features

### EBS snapshot archieve

- Move snapshot to an "archieve tier" that is 75 % cheaper
- takes with 24 - 72hrs for restoring the archieve

### Recycle bin for EBS snapshots

- setup rules to retain deleted snapshots so you can recover them after an accidental deletion

### steps to create a EBS volume and snapshot


  

## Conclusion
EBS Volumes are like cloud hard drives for your EC2 instances, and EBS Snapshots are their backups. They help keep your data safe, scalable, and flexible.


## AMI - Amazon Machine Image 


An Amazon Machine Image (AMI) is a template that contains the software configuration required to launch an EC2 instance.  


## Types of AMIs

- **Public AMIs**: AMIs provided by AWS or the community that are available for use by all AWS users.
- **Private AMIs**: AMIs that you create and are available only to your AWS account.
- **AWS Marketplace AMIs**: AMIs available for purchase through the AWS Marketplace, often bundled with software and configurations provided by third parties.

## Components of an AMI

- **Root Volume**: Contains the image used to boot the instance.
- **Block Device Mapping**: Defines the volumes attached to the instance when it's launched.
- **Permissions**: Determines who can access the AMI.



## EC2 Instance Store

### Introduction

Amazon EC2 instance store provides temporary block-level storage for your instances. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content.

### Characteristics of Instance Store

- **Ephemeral Storage**: Data stored in instance store volumes is ephemeral and can be lost if the instance is stopped, terminated, or fails.
- **High I/O Performance**: Instance store provides high I/O performance and is suitable for applications that require temporary storage with high throughput.
- **Local Storage**: Instance store volumes are physically attached to the host computer, providing lower latency compared to network storage options like EBS.

### Use Cases

- **Buffers and Caches**: Temporary storage for applications that use large amounts of data for a short period.
- **Scratch Data**: Storage for temporary data generated during data processing or computations.
- **Session Data**: Storing session data for applications where session persistence is not required.


[EBS volume & snapshot](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/create_ec2_instances.md)