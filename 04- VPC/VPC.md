# AWS VPC (Virtual Private cloud)
## VPC intro
* VPC is network layer
* Create own network, assign ip address range, set route tables, nw gateways etc.
* To create VPC
    * specify address range
    * CIDR max /16 to min /28
    * no overlap if you are connecting another VPC
* Contains
    1. Subnet
    2. Route tables
    3. Security group
    4. ACLs
    5. DHCP option set
    6. IGW
    7. Elastic ip
    8. ENIs
    9. Nat gateway/ instance
    10. Endpoints
    11. Peering
    12. VGW
## Subnet
* Segment/Subset of VPC's IP address range
* CIDR block is used to select particular Subset
* Minimum /28 
* Five IP are reserved within subnet
    * First - network , Second - Router , Third - DNS server , Fourth -Reserved , Last- Broadcast
### Types
* Public - route table have default route to IGW
* Private - route table don't have route to IGW     
* VPN only - route table have default route to VGW
## Route tables
* Determines Where network traffic of a subnet is directed
* Tool to create public , private or VPN only subnet
* Default root 
    * direct traffic within VPC
    * cant delete or remove
### Important points to remember for exam
* Every VPC has implicit (default)  Router
* Every VPC has default route tavpble (main table)
* YOu can create custom route table
* You can associate custom route table to subnet. When you dont do it , it refers to main
* route table has CIDR block and target. AWS uses most specific route. 
    * 10.2.1.122 --> VGW 
    * 0.0.0.0 --> IGW
    * When traffic is sent to 10.2.1.122 ; specific rule is used (VGW) and not 0.0.0.0
## Internet gateways
* AWS managed (redundant , highly available, scalable)
* Enables traffic between instance & Internet
* performs network address translation for EC2 which has public ip
    * ec2 intance is only aware about private ip
    * IGW translates private ip to its public ip.
    * Keeps mapping between private <--> pulic ip
* EC2 Incoming traffic Enable
    * attach IGW to VPC
    * update subnet route table (0.0.0.0/0 to IGW)
    * set network ACL and securiy group to allow certain traffic
* EC2 Outgoing traffic enable 
    * assign public or elastic ip to your instance
## DHCP option set
## Elastic IP addresses
* AWS has pool of IP address (in a region)
* Elastic IP is static public IP address that can be assigend to EC2/ gateway etc
* Elastic - IP remains same while you can change underlying infrastructure
### Important points to remember for exam
* Allocate EIP before assign
* Cant assign to different region
* One-to-one relationship between EIP <--> Network interface
    * So EC2 can have multiple interfaces, so it can multiple EIP's
* can assign within VPC or different VPC of same region
* keeps tagged to your account even if instance stopped/ terminated
* gets chanrged unless explicitly released  