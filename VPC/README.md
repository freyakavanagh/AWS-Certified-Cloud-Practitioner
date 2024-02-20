# VPC (Virtual Private Cloud)

- A private network to deploy your(regional) resources within.

- Subnets: allow you to partition your network inside your VPC and is within/associated with an availibility zone.
  -  Can be public (accessable from the internet) or private (not accessible)
  -  Can put instances, load balancers and databases in them
-  Route Tables: To define access to the internet and between subnets.
-  Internet Gateway: helps the VPC instances within public subnets to connect to the internet.
   -  Public subnets have a riute to the internet gateway
- NAT Gateways: allow your instances in private subnets access to the internet but not access from it. (remain private)
  - Built inside a public subnet and a route is built from the private subnet to the NAT, and from the NAT to the Internet Gateway
  - NAT Gateway(AWS Managed), NAT Instances (self-managed).
- NACL (Network ACL): A firewall which controls traffic from and to the subnet with ALLLOW and DENY rules for IP's
  - Return traffic must be explicitly allowed by rules (stateless)
- Security Groups: A firewall that controlls traffic to and from an ENI/ an EC2 Instance with ALLOW rules for IP's and other security groups
  - Return traffic is automatically allowed (stateful)

# IP Adresses

## IPv4

- Public IPv4 can be used on the internet
- Private IPv4 can be used within your own network
- An EC2 instance gets a new public IP address every time you stoop and start it, the private IP is fixed.

- Elastic IP: Allows you to attached a fixed public IPv4 address to an EC2 instance

## IPv6

- Only public addresses.



