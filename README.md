# tf-azure-nginx-registry

## Challenge: Create a private module

### The task
Create GitHub repository with Terraform Code in which these Private modules are used

### The result

To fulfill the requirements of this challenge, the following main resources were provisioned:

- **Resource group**
- **Virtual Network (VNet)** - containing public and private subnet
- **Network security group for the web server** - containint inbound and outbound rules which control the traffic based on their priorities 
- **Linux Virtual Machine** - located in private subnet
- **Bastion host** - used as a jump server to connect to the web server
- **Load balancer** - located in public subnet
- **Backend pool** associations - for the connection between the load balancer and the web server

### Private modules

The code uses the following modules from Terraform Cloud Private registry - networking, load-balancer and compute module.

- **Networking** - provisions resources like subnets, public IPs, security groups, network interfaces
- **Compute** - provisions the VM resource
- **Load Balancer** - provisions the load balancer related resources including its public IP, backend pools, probe, rules, etc. 