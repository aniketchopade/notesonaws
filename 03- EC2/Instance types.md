# AWS EC2 Instances
## Instance types
### General Purpose - Balences all resouces - Compute, Memomry and Network
* T2
    * Burstable
    * Accures credits when CPU is idle
    * Credits are used when traffic is active
    * Lowest cost , general Purpose
        * Use cases - Websites and web applications, development environments, 
        * build servers, code repositories, micro services, test and staging environments, 
        * and line of business applications. 
* M4
    * EBS Optimized at no additional cost
    * Supports enhanced Network features - cluster networking
        * Use cases - Small and mid-size databases, data processing tasks that require additional memory, caching fleets, 
        and for running backend servers for SAP, Microsoft SharePoint, cluster computing
M3
* SSD based instance storage
    * Use cases - Same use cases as above
### Compute Optimized - Have high performing processors
* C4 (compute)
    * EBS Optimized, enhanced networking & clustering
    * High performance front-end fleets, web-servers, 
    * Batch processing, distributed analytics, 
        * Use cases - high performance science and engineering applications, ad serving, MMO gaming, and 
        video-encoding.
C3 (Compute)
    * SSD backed instance
    * Supports enahcned networking
### Memomry Optimized
* X1 
    * For Large scale, enterprise class in-memory applications
    * EBS Optimized
        * Use cases - in-memory databases like SAP HANA, 
        big data processing engines like Apache Spark or Presto, 
        and high performance computing (HPC) applications. 
* R4 (RAM)
    * memory intensive applications
       * Use cases - High performance databases, data mining & analysis, in-memory databases, distributed web scale in-memory caches, 
        applications performing real-time processing of unstructured big data, Hadoop/Spark clusters
* R3 (RAM)
        * Use cases -high performance databases, distributed memory caches, in-memory analytics, 
        genome assembly and analysis, Microsoft SharePoint
### Accelerated Computing - 
* P2 (Powerfull)
    * General purpose GPU computing
        Use cases - Machine learning, high performance databases, computational fluid dynamics, computational finance, seismic analysis, 
                    molecular modeling, genomics, rendering, and other server-side GPU compute workloads.
* G3 (Grphics)
    * Optimized for Grpahics intensive applications
        Use cases - 3D visualizations, graphics-intensive remote workstation, 
        3D rendering, application streaming, video encoding, and other server-side graphics workloads.
* F1 (FGPA)
    Field programming gate arrays
        Genomics research, financial analytics, real-time video processing, big data search and analysis, and security.

### Storage Optimized
* I3 (iops)
    * NVMe SSD Storage
        * Use cases - NoSQL databases like Cassandra, MongoDB, Redis, in-memory databases such as Aerospike, 
                    scale out transactional databases, data warehousing, Elasticsearch, analytics workloa
* D2 (Dense)
    * Dense storage  (48 tb)
        Use cases - Massively Parallel Processing (MPP) data warehousing, 
                    MapReduce and Hadoop distributed computing, 
                    distributed file systems, network file systems, log or data-processing applications
