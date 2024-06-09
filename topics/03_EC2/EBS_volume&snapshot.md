# EBS Volumes and EBS Snapshots

## What are EBS Volumes?

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

[EBS volume & snapshot]()
  

## Conclusion
EBS Volumes are like cloud hard drives for your EC2 instances, and EBS Snapshots are their backups. They help keep your data safe, scalable, and flexible.


