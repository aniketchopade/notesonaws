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
    * First - network , Second - Router , Third - ?? , Fourth -Reserved , Last- Broadcast
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
* Every VPC has default route table (main table)
* YOu can create custom route table
* You can associate custom route table to subnet. When you dont do it , it refers to main
* route table has CIDR block and target. AWS uses most specific route. 
    * 10.2.1.122 --> VGW 
    * 0.0.0.0 --> IGW
    * When traffic is sent to 10.2.1.122 ; specific rule is used (VGW) and not 0.0.0.0