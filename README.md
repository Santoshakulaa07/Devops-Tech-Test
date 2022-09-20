Three-tier architecture automation using Terraform
This project is used to automate the process of a three tier architecture in AWS. There are two main files here. A "main.tf" file which configures the AWS resources based on the variables defined in the "variables.tf" file. Before starting with the "main.tf" file make sure you go through the "variables.tf" file to make sure that you have defined all the variables as per your needs. No variables can be left undefined else it would result in an error. After you have defined the variables you can run the "main.tf" file. Before doing so you need to initialise Terraform which needs to be done only once in a folder. Initialise Terraform with the following command:

terraform init
After initialisation has been done, you can proceed to running the "main.tf" file with the following command:

terraform apply
The code does the following:

Creates a VPC with the CIDR block provided in the region you want.
Creates subnets for each layer.
Creates an IGW and NAT gateway.
Creates Route tables.
Creates a RDS instance.
Configures security group for Web layer.
EC2 instances for webservers.
Application load balancer.
Note:
When running the "main.tf" file you might get an error saying that the subnet_group does not exist. In this case just run it again using " terraform apply" and you will be able to get the output.