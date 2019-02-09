![banner](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/banner.png)

# Challenge:

Create one environment on AWS using ECS (ec2 launch type) and deploy KONG API Gateway (community edition) onto it and expose the service and management ports to the internet.
Optional: Configure a demo application to run on the same cluster and expose the service via Kong.

### Technology Used:

- Terraform v0.11.11 + provider.aws v1.58.0
- 

### System Requirements:

I am working from a windows machine with 10.0.17763 N/A Build 17763. I also have the linux subsystem installed and running with terraform added to the path for use with both bash and powershell. 
For the purposes of this demo, I will use SSH (putty) to administer an EC2 instance where terraform will be installed - no need to rely on local hardware. 

Terraform download: 

 - https://www.terraform.io/downloads.html

### EC2 Creation and setup:

 - Login to the AWS console with the appropriate user account (not the root account):

![login_aws](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/aws_login.PNG)

 - Select EC2 from the management console:

![select_ec2](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/select_ec2.PNG)

 - Launch a new instance:

 ![launch_instance](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/launch_instance.PNG)

 - Select an appropriate AMI:

 ![select_ami](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/select_ami.PNG)

 - Choose and instance type: 

 ![choose_instance](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/choose_instance_type.PNG)

 - Review setup and launch the instance:

 ![review_launch](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/review_launch.PNG)

 - Create, or re-use and already created key pair (do not store in a public visible repo or location!):

 ![key_pair](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/key_pair.PNG)

 - Select acknowledge, and launch the instance:

 ![acknowledge_launch](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/acknowledge_launch.PNG)

 - Review launch status until the instance is ready:

 ![review_launch](https://s3-ap-southeast-2.amazonaws.com/terraform-kong-09022019/review_launch.PNG)
 
 