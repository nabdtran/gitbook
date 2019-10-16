# Virtual Machines

### Snapshots

Transfer disk type

Persistent disk snapshots

* Not available for local SSD
* Creates an incremental backup not visible in buckets
* Snapshots can be restored to a new persistent disk on the same project
* Snapshots do not backup VM metadata, tags

Resize persistent disk

* Increase storage capacity to increase IOPS

### Compute Engine

Infrastructure as a Service

Predefined or custom machine types:

* vCPUs and Memory
* Persistent HDD
* Networking
* Linux or Windows

Features

* Machine rightsizing
* Stackdriver statistics
* Instance metadata
* Startup scripts
* Availability policies
* Per second billing
* Sustained use discounts
* Committed use discounts
* Preemptive 80% discount
* Global load balancing

### Storage

Persistent disks.

* Standard, SSD or local SSD
* Standard and SSD persistent disks scale in performance for each GB of space allocated
* Local SSD great for batch jobs
* Resize disks, migrate instances with no downtime

### Networking

* Inbound/Outbound firewall rules
  * IP based
  * Instance/group labels
* Regional HTTPS load balancing
* Network load balancing
  * Does not require pre-warming



