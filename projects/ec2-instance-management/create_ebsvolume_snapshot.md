# How to Create EBS Volumes and Snapshots

## Creating an EBS Volume

### Step 1: Create an EBS Volume

1. **Go to the EC2 Dashboard**:
   - Open AWS Management Console.
   - Click on "Volumes" under "Elastic Block Store" on the left.

2. **Create a New Volume**:
   - Click "Create Volume".
   - Set the volume type (e.g., gp2), size, and Availability Zone (same as your instance).
   - Click "Create Volume".

[ebs_01]()

3. **Attach the Volume to an Instance**:
   - Select your volume.
   - Click "Actions" > "Attach Volume".
   - Choose your instance and device name.
   - Click "Attach".

[ebs_02]()

To create a snapshot of an EBS volume:

1. Go to the EC2 Dashboard in the AWS Management Console.
2. Click on "Volumes" under "Elastic Block Store" in the left-hand menu.
3. Select the volume you want to back up.
4. Click "Actions" > "Create Snapshot".
5. Add a description for the snapshot.
6. Click "Create Snapshot".

## Example: Restoring from a Snapshot

To create a new EBS volume from a snapshot:

1. Go to the "Snapshots" section in the EC2 Dashboard.
2. Select the snapshot you want to use.
3. Click "Actions" > "Create Volume".
4. Choose the volume type, size, and Availability Zone.
5. Click "Create Volume".




