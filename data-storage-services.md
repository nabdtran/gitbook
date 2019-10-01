# Data Storage Services

### Storage and Database Decision Chart

![](.gitbook/assets/image%20%283%29.png)

BigQuery for data warehousing.

### Cloud Storage

|  | Regional | Multi-Regional | Nearline | Coldline |
| :--- | :--- | :--- | :--- | :--- |
| Design Patterns | Data that is used in one region or needs to remain in one region | Data that is used globally and has no regional restrictions | Backups - data that is access no more than once a month | Archival or Disaster Recovery data that is accessed no more than once a year |
| Feature | Regional \(Replication\) | Geo-redundant | Backup | Archived or DR |
| Availability | 99.9% | 99.95% | 99.0% | 99.0% |
| Durability | 9 9's | 9 9's | 9 9's | 9 9's |
| Duration | Hot Data | Hot Data | 30 day minimum | 90 day minimum |
| Retrieval Cost | None | None | $ | $$ |

### Cloud Storage Overview

Buckets cannot be nested

Objects inherits class of bucket \(Coldline\)

No minimum size

### Changing Default Storage Classes

Multi-Regional buckets cannot be changed to Regional or vice versa.

### Access Control

Bucket policies in IAM controls the bucket level. ACLs are used for the file level.

Signed URL can allow you to share an object to others with some scope. Can be a timed URL.



