# AWS EC2 Provisioning using Manual Setup & Terraform
Author : Rishi Ranjan

# Objective 
1. Understand AWS core concepts
2. Launch an EC2 instance manually using AWS Console
3. Provision an EC2 instance using Terraform\

# AWS Core Concepts Overview
1. AWS : AWS is a cloud platform that provides on-demand computing resources like servers, storage, networking, and databases.
2. EC2 (Elastic Compute Cloud) : EC2 provides scalable virtual servers (instances) in the cloud.
3. IAM : IAM is used to manage users, roles, and permissions securely.
4. VPC : A logically isolated network in AWS where resources are launched.
5. Subnet : A logical, segmented partition of an IP network designed to break large networks into smaller, more manageable, and efficient sub-networks.

# Part 1: Launch EC2 Instance Manually (AWS Console)
## Steps
1. Login to AWS Management Console.
2. Navigate to EC2 → Instances → Launch Instance.
3. Name the Instance. <img width="1620" height="266" alt="Image" src="https://github.com/user-attachments/assets/2bcfb447-21bf-4362-b742-0394120a923d" />
4. Choose Ubuntu(free tier).  <img width="1242" height="260" alt="Image" src="https://github.com/user-attachments/assets/d1c9d47f-ef29-4aeb-b495-9bc51e2e57e8" />
5. Select instance type: t3.micro (Free Tier).   <img width="1304" height="245" alt="Image" src="https://github.com/user-attachments/assets/29ecabc9-5f24-4537-91d8-4adcb7fc02f3" />
6. Create Key Pair named : vms. <img width="1615" height="170" alt="Image" src="https://github.com/user-attachments/assets/448699c9-de51-4636-9645-57b3abe8d957" />
7. Configure Security Group.
8. Launch the instance.
9. INSTANCE is Created   <img width="1883" height="370" alt="Image" src="https://github.com/user-attachments/assets/e260af6f-bee7-4525-aa3a-286aaf2862c2" />

# Terraform Core Commands
- terraform init :  It performs essential setup tasks to prepare the directory for subsequent commands.
- terraform plan : Core component of the Terraform workflow used to create an execution plan that previews the changes Terraform will make to your infrastructure without actually applying them.
- terraform apply : Core component of the Terraform workflow used to execute the actions proposed in a plan to create, update, or destroy infrastructure resources in the real world.
- terraform destroy : Used to permanently deprovision all the infrastructure and associated resources 

# Part 2: Provision EC2 Using Terraform
## Steps
1. First Install Terraform in your local machine from develepors.hashicorp.com/terraform.
2. After Installing we have to make .tf file to connect the local machine to the aws cloud.
3. That .tf file will be made as provider.tf file and the code would be copy and pasted from the documentation found in registry.terraform.io.  <img width="731" height="619" alt="Image" src="https://github.com/user-attachments/assets/de0a3bb4-f41a-40c3-8670-eb40192e7cad" />
4. In this file we will add the access key and security key(for practice purpose only and it is not recommended) and all the details about the instance like ami image, name, tag, etc.
5. After saving this file, we will use command :-
 - terraform init
- terraform plan
- terraform apply
6. After these commands our instance will be created and start running. <img width="1566" height="223" alt="Image" src="https://github.com/user-attachments/assets/57206ab9-f7af-4c43-abc2-a0a01dbc8198" />

# Conclusion
- In this task we learned about AWS Instances and how to setup it manually and as in Infrastrusture as Code with the help of Terraform.
- We learned that doing with the help of Terraform makes it easier and faster while manually it takes time.
