# CodeDeploy

Automatically deploy applications to on-premise compute platforms, EC2, Amazon ECS or AWS Lambda.


Create a deployment group to define configuration options such as 
    - what type of deployment to perform, In-place vs. Blue/green.
    - whether to deploy directly to instances or auto-scaling groups.
    - how fast you want an application to be deployed.
    - whether you would like a load balancer to manage traffic to and from your instance during deployment.
    
## Requirements

- IAM role for EC2 to access S3 ( I do think this is needed if you revision location is Github - i.e. application is stored in Github )

![](https://github.com/gnetsanet/CodeDeploy/blob/master/images/EC2S3Role.png)

- IAM role for CodeDeploy to access and interact with EC2

![](https://github.com/gnetsanet/nf-CellRanger/blob/master/images/compute_environment2.png)


```
sudo yum update
sudo yum install ruby
sudo yum install wget
cd /home/ec2-user
wget https://aws-codedeploy-eu-central-1.s3.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
```

Make sure AWS CodeDeploy agent is installed and running on the instance you want to deploy you app to.

```
[ec2-user@ip-172-31-25-88 ~]$ sudo service codedeploy-agent status
The AWS CodeDeploy agent is running as PID 12413
```

## Other considerations

- If revision location is S3, the bucket containing the application should be in the same region as the resources/deployment group. 

## Successful Deployment

![](https://github.com/gnetsanet/CodeDeploy/blob/master/images/successful_deployment.png)
