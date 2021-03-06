# AWS Elastic compute cloud

## EC2 Basics
* Launching of instance
* Use computer , charge is hourly basis
* software part - AMI , hardware part - instance type

## Intance types
### AMI
* Aws published
* Marketplace
    * Additional charges
* Saved from ec2 instance
* VM/Imported Uploaded
        * Usage
        * Migrate Your Existing Applications and Workloads to Amazon EC2
        * Create a Disaster Recovery Repository for your VM images
        * Copy Your VM Image Catalog to Amazon EC2
## Security of instances
### Addressing of instances
* public DNS name
* public Ip 
    * persists only till ec2 runs
* elastic Ip
    * persists even when ec2 is terminated
### Initial access
* Public key cryptography
* Windows - admin password encrypted using symmetric key encryption
### Virtual firewall
* Security groups
    * accept / deny rules, stateful
## Lifecycle of instances
### Launching
* bootstarpping 
    * install custom software while instance is being launched
    * UserData - script to be executed. un-encrypted - no passwords should be mentioned
    * Uses - install custom s/w , enroll into directory services, OS level patch, chef / puppet
* vm/import export
    *  can import existing vm images to ec2 (and then back)
    *  instances launch within AWS from AMI's cant exported
* instance metadata
    *  http://publicip/latest/meta-data
    *  instance type , id, security group, ami 
### Managing
* Tagging
* Monitoring
### Modifying instance
* Instance type can be changed by stopping, specifying new type and relaunching it 
* Changing security group to allow more protocols 
### Termination protection
* call for termination will be failed till it disables
* still can terminate using - os shutdown command, autoscale, overbidden
## Options
### Pricing
* On-Demand instance
    * price/ hour, no up-front commitment
    * provision computer for unpredictable load
* Reserved 
    *  upfront commit for predictable and steady load 
    * saves 75% of price than on-Demand
    * cost depends on two factors
        * Term commitment
            * One or three years
        * payment Options
            * all upfront
            * partial
            * no upfront
* Spot
    * Workload is not time critical and interruption tollerent
    * Specify price for instance, 
    * so instance runs till
        *  customer terminates orsomeone bids higher
### Tenancy
* Shared
    * One host machine can serve EC2 of more than one customer
* Dedicated instance
    * One host machine serves EC2 instances of only one customers
* Dedicated host
    * One machine serves as only ONE EC2 insatce
    * reqiured for licensing 
### Placement groups
* logical grouping of EC2 instance within single avaiability zones
* applications benefitted from low network latency
* EC2 which supports enahnced networking should be chosen
### Instance stores
* Temporary storage attached to host machine
* no persistancy
* idle for temp storage backup , cahche, db io buffer
* use on EC2 where data processing is more important than data storage
* Multiple types
    1. Ephimeral
    2. Non Volatile Memory -i3 instance
    3. TRIM



