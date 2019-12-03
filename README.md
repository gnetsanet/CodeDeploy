# CodeDeploy

 
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
