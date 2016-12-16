Instructions
============
1.) When server is booted run the following commands as root.

sudo su

yum update -y

yum install ruby -y

yum install wget -y

yum install aws-cli -y

cd /home/ec2-user

2.) Here you will setup your AWS access, secret, and region.
aws configure 

wget https://aws-codedeploy-us-west-2.s3.amazonaws.com/latest/install

chmod +x ./install

3.) This is simply a quick hack to get the agent running faster.

sed -i "s/sleep(.*)/sleep(10)/" install 

./install auto


4.) Verify it is running.
service codedeploy-agent status
