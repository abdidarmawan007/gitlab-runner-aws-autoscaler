## gitlab runner aws autoscaler with ec2 spot instance

![alt text](https://i.imgur.com/1byPnQS.jpg)

#### EC2 Spot Instance Price as a runner/agent
![alt text](https://i.imgur.com/o6OVzk9.png)


for iam-policy
ec2 gitlat runner manager only can delete EC2 with ec2 profile gitlab-runner-agent
 ```{
            "Action": [
                "ec2:TerminateInstances"
            ],
            "Effect": "Allow",
            "Resource": "arn:aws:ec2:*:(AWS-ID-XXX:instance/*",
            "Condition": {
                "StringEquals": {
                    "ec2:InstanceProfile": "gitlab-runner-agent"
                }
            }
        },
        
