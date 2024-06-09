# Security Group Setup in AWS

## Objective
Learn how to create and manage a security group in AWS to control inbound and outbound traffic to your EC2 instances.

## Steps
1. Create a security group.
2. Define inbound and outbound rules.
3. Attach the security group to an EC2 instance.

## AWS Services Used
- EC2
- VPC (Virtual Private Cloud)

## Security Group Setup Instructions

### Step 1: Create a Security Group

1. **Navigate to the Security Groups Section**:
   - Open the AWS Management Console.
   - Go to the EC2 Dashboard.
   - In the left-hand navigation pane, click on "Security Groups" under "Network & Security".

![sg_01](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/sg_01.png)


2. **Create a New Security Group**:
   - Click the "Create security group" button.
   - Enter a name and description for your security group (e.g., `web-server-sg`).
   - Select the VPC where this security group will be used.

### Step 2: Define Inbound and Outbound Rules
1. **Add Inbound Rules**:
   - Click on the "Inbound rules" tab.
   - Click "Edit inbound rules".
   - Add rules to allow necessary traffic (e.g., HTTP, SSH):
     - Type: HTTP
     - Protocol: TCP
     - Port Range: 80
     - Source: 0.0.0.0/0 (for public access) or specific IP ranges
     - Type: SSH
     - Protocol: TCP
     - Port Range: 22
     - Source: Your IP (for secure SSH access)
   - Click "Save rules".

2. **Add Outbound Rules**:
   - Click on the "Outbound rules" tab.
   - Click "Edit outbound rules".
   - By default, all outbound traffic is allowed. You can modify this as per your requirements.
   - Click "Save rules".

[sg_02](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/sg_02.png)



### Step 3: Attach the Security Group to an EC2 Instance
1. **Attach During Instance Launch**:
   - When launching a new EC2 instance, you can select the created security group in the "Configure Security Group" step.
2. **Attach to an Existing Instance**:
   - Go to the "Instances" section in the EC2 Dashboard.
   - Select the instance you want to modify.
   - Click "Actions" > "Networking" > "Change security groups".
   - Select the security group and click "Assign security groups".

[sg_03](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/docs/sg_03.png)
