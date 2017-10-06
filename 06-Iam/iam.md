# Principle
* Entity interacts with resources
* Needs permissions (policy)
## Types
### Root
* Single sign on
* Has all the rights
* Permanant , cant delete
### IAM user
* Users creates by IAM
* Needs policy to be associated with it for access
### Roles / Temp security token
* Role - Special previliges to principles for set duration of time
* Actors assume a role
  * Temp Token is generated
  * Need to specify time 15 min to 36 hours

