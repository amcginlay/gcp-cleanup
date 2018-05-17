# gcp-cleanup

## Steps

- Network services > Cloud DNS - delete all records set entries and containing zones
- Network services > Load Balancers - delete all LBs + attached resources (e.g. backends, etc.)
- Compute Engine > VM instances - stop and delete all
- Compute Engine > Instance groups - delete all
- Compute Engine > Disks - delete all
- Compute Engine > Metadata - delete all
- Compute Engine > Images - delete all user defined images
- Compute Engine > Health Checks - delete all
- Storage > Browser > Buckets - delete all
- VPC Networks > VPC Networks - Delete non-default networks and all sub-components
- VPC Networks > External IP addresses - Release Static Addresses
- VPC Networks > Firewall rules - Delete non-default rules
- IAM & Admin > IAM - delete any accounts the install explicitly created
- IAM & Admin > Service Accounts - delete any accounts the install explicitly created
