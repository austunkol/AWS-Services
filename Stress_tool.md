# ` Stress Tool`
- Connect to ec2 instance via Terminal

- Get root privileges
```
 sudo su 
 ```
- Then install and run stress application with the following commands and increase CPU usage.
```
 yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
 yum install stress
 stress --cpu 80 --timeout 2000
 ```
- `or`

```
sudo amazon-linux-extras install epel -y
sudo yum install -y stress
stress --cpu 80 --timeout 20000
```
- Stress tool will start to increase the CPU usage of the instance.

- Do the same process for the other running instances if needed. The CPU utilization will gradually increase.
