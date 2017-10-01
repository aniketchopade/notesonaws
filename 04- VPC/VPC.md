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
* Five IP are reserved 
    * First - network , Second - Router , Third - ?? , Fourth -Reserved , Last- Broadcast

