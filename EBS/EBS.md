# EBS (Elastic Block Store)

It allows your instances to persist data, even aftr their termination

` EBS volume can only mounted to be one instance at a time`

Think of them as a "Network USB stick"

## EBS Volume


* It's network drive(not a physical drive)

* It's locked to an Availability Zone(AZ)

* EBS volume in us-east-1a cannot be attached to us-east-1b

## EBS Hands On

* Go to EC2
```
- Click to Instance

- Click the Storage
    
- You can see Root device details/type
    
- Scrool down and can see Volume ID
    
- Click the Volume ID/ You can see all EBS Volume ID's
     
- There is a `Create Volume` on the top left

- Choose the `Volume Type`

- Availability zone should be same with EC2 Zone

- Create Volume
```
* After create a volume assign to EC2

```
- Right click to created volume and click the attach volume

- Choose the Instance(EC2) same availability zone

- Hit the attach

- Come back to EC2 instances check the `Volume ID` 
```

[goto: click here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html)


** If you terminate EC2, EBS volume will be available or deleted. When we create EC2 if we chose `Delete on Termination` EBS volume will be deleted. This settings Step 4 in Ec2 creatation.

