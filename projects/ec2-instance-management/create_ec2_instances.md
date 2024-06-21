# EC2 Instance storage.

## How to Create EBS Volumes and Snapshots


### Creating an EBS Volume

#### Step 1: Create an EBS Volume

1. **Go to the EC2 Dashboard**:
   - Open AWS Management Console.
   - Click on "Volumes" under "Elastic Block Store" on the left.

2. **Create a New Volume**:
   - Click "Create Volume".
   - Set the volume type (e.g., gp2), size, and Availability Zone (same as your instance).
   - Click "Create Volume".

![ebs_01](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ebs_01.png)

3. **Attach the Volume to an Instance**:
   - Select your volume.
   - Click "Actions" > "Attach Volume".
   - Choose your instance and device name.
   - Click "Attach".

![ebs_02](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ebs_02.png)

To create a snapshot of an EBS volume:

1. Go to the EC2 Dashboard in the AWS Management Console.
2. Click on "Volumes" under "Elastic Block Store" in the left-hand menu.
3. Select the volume you want to back up.
4. Click "Actions" > "Create Snapshot".
5. Add a description for the snapshot.
6. Click "Create Snapshot".

### Example: Restoring from a Snapshot

To create a new EBS volume from a snapshot:

1. Go to the "Snapshots" section in the EC2 Dashboard.
2. Select the snapshot you want to use.
3. Click "Actions" > "Create Volume".
4. Choose the volume type, size, and Availability Zone.
5. Click "Create Volume".




## Steps to Create an AMI

### Step 1: Prepare the Instance

1. **Launch an EC2 Instance**: Start with a running EC2 instance configured with the software and settings you need.
2. **Connect to the Instance**: Use SSH (for Linux) or Remote Desktop Protocol (RDP) (for Windows) to connect to your instance.
3. **Configure the Instance**: Install and configure the necessary applications and software on your instance.

[ami_0](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ami_0.png)

### Step 2: Create the AMI

1. **Stop the Instance (optional but recommended)**: Although you can create an AMI from a running instance, it is recommended to stop the instance to ensure data consistency.
    ```bash
    aws ec2 stop-instances --instance-ids i-1234567890abcdef0
    ```
2. **Create the AMI**:
    - Go to the **EC2 Dashboard** in the AWS Management Console.
    - Select **Instances** from the sidebar.
    - Right-click on the instance you want to create an AMI from, select **Image**, then click **Create Image**.
    - Fill in the required details such as **Image Name** and **Image Description**.
    - Choose whether to **No reboot** the instance (stopping it first is recommended for consistency).
    - Click **Create Image**.

[ami_01](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ami_01.png)

### Step 3: Monitor the AMI Creation

1. **View the AMI Status**:
    - Navigate to the **AMIs** section under **Images** in the EC2 Dashboard.
    - You will see your new AMI in the list with a status of **pending**.
    - Once the AMI creation process is complete, the status will change to **available**.
  

[ami_02](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ami_02.png)


### Step 4: Launch an Instance from the AMI

1. **Select the AMI**:
    - Go to the **AMIs** section in the EC2 Dashboard.
    - Select the AMI you created.
2. **Launch Instance**:
    - Click **Launch**.
    - Follow the steps to configure your instance, selecting instance type, configuring instance details, adding storage, and configuring security groups.
    - Review and launch the instance.

[ami_03](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/ami_03.png)



