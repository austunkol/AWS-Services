- `What is VPC?`

- Amazon Virtual Private Cloud is a logically isolated area of the AWS cloud where you can launch AWS resources in a virtual network that you define. 

- `What is Subnet and What are the type of the Subnets?`
- A subnet is a range of IP addresses in your VPC. There are 2 types of subnets;

	- Public Subnet 
	- Private Subnet

- `What is the feature of Public Subnets?`
- When we say Public Subnet, the virtual machines that we place in the subnets can be accessed from the outside world. It has a internet connectivity.

- `What does the Route Table and Router mean?`
- Route Table is a configuration files that explain how to go from destination X to destination Y or to the internet and which way to use.
- Routers are components that manage the Route Tables and they act as “intersections” within the network.

- `How can you define Security Group?`

- Security Groups is used for determining which traffic will access the instance.a In other words, security group is a virtual `Firewall of Instance.`

- `Network ACLs are Stateless. So, what does it mean Stateless?`

- It is a `stateless` means that any changes made in the inbound rule will not reflect the outbound rule

- `What is the Bastion Host?`

- A Bastion Host is a server whose purpose is to provide access to a private network from an external network, such as the Internet. 

- `Why do we need a NAT Gateway & NAT Instance?`

- if you want to connect from  EC2 ınstance in private subnet to the internet, you need to create NAT Gateways or NAT Instance in Public Subnet.Because of the security precaution, our private subnet blocks the connectivity and we don't have Public IP for instance in Private Subnets also. 

- `What is the difference between NAT Gateways and NAT Instance?`

- NAT Gateways or NAT Instance are pretty much similar things and they provide the same functionality, however, a NAT Gateway is an AWS managed NAT service but NAT Instance is specified and managed by us.

- `Are Elastic IPs free?`

- Elastic IPs are totally free `as long as they are being used` by an instance. However, Amazon will charge you $0.01/hr for each EIP that you reserve and do not use. So don't forget to terminate the Elastic IP or associated component such as NAT Gateway if you'll not use anymore in the short term.

- `How can we solve the problem of accessing from Private instance to outside?`

- In such cases, we can use `NAT Gateway or NAT Instance`

- `Why do we prefer NAT Instance instead of NAT Gateway?`

- NAT Gateways are managed by AWS and we don't get involved in anything. But, if your system consists of hundreds of machines and you need some TCP based adjustments, NAT Gateway may not support your needs.

Also, we have one more reason to choose NAT Instances. It's the price.NAT Instances are cheaper than NAT Gateway.