# AWS Cloudwatch
## Cloudwatch
* Define metric, create a alarm and send notification
* Enabled for number of AWS services
* Basic monitoring 
    * Data points are sent every 5 minutes
* Detailed monitoring
    * Data points are sent every minute
    * Supports aggregation at extra cost
    * Aggreation is allowed only within region
* Custom metric
    * Os visible metric can be PUT using AWS Cloudwatch API
    * Then alarm and notification is triggered as if it is AWS defined metric
## Cloudwatch logs
* Log files
* Cloudwatch agent needs to be installed on EC2
* Retained only for 2 weeks.
* 5000 alarms limit per account 