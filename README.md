# AWS Cloudformation Scripts

 Udacity Project 2 - Launch Configuration for your application servers in order to deploy four servers, two located in each of your private subnets. The launch configuration will be used by an auto-scaling group.
 
 In this project, I have to deploy web servers for a highly available web app using CloudFormation.  I wrote the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up.

To test project:
- Goto file server-parameters.json and update S3Bucket with your bucket name.
- Upload udacity.zip to your bucket.
- First create network 
```sh
./create.sh <network-stack-name> network.yml network_parameters.json
```
Then create server stack - 
```sh
./create.sh <server-stack-name> servers.yml servers-parameters.json
```

Head to CloudFormation on AWS Console and in udagram-servers output you will have Project URL.

If you make changes in Script after creating stack, use 
- To update network stack 
```sh
./create.sh <network-stack-name> network.yml network_parameters.json
```
- To update server stack 
```sh
./create.sh <server-stack-name> servers.yml servers-parameters.json
```



