Ideally, this project would be split into several CloudFormation scripts
	- Develop the infrastructure/network
	- Spin the servers into the VPC

However, all the resources are generated in one script as I learned to incorporate
them together.

Attached is the architecture diagram with the following key points:
	- Dedicated VPC for this project
	- 2 public subnets across 2 AZs for high availability
	- 2 private subnets containing the servers that will run Udagram
		- Encompassed in autoscaling group

Usage from folder containing files:

./create.sh NAMEOFDEPLOYMENT udagramCFdeploy.yml udagramParameters.json


Output in AWS Console provides a link with http:// prepended to the public facing load
balancer

http://udagr-Udagr-ILEB9A5Z45WM-697791968.us-west-2.elb.amazonaws.com