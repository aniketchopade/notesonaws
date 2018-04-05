#Cloudwatch
## Cloudwatch for EC2
* CPU ( % utilization and credits)
* Network (packets in/out, bytes)
* Disk ( data read/write in bytes)
* Status check
# Exam
* RAM usage and disk empty space are custom metric
    * Granularity is *minimum* 1 minute 
* Basic monitoring - default interval is 5 minutes ( C5/ M5 it is every 1 minute)
* Other services could be different
# Retention of CW metrics
* 2 weeks
* Older can be retrived by GetMetricStatistics API or Third party tools
* EC2 termination - you have two weeks to collet before they get purged
