# gcp-cleanup

## Steps

- Network services
  - Cloud DNS - delete all records set entries and containing zones
  - Load Balancers - delete all LBs + attached resources (e.g. backends, etc.)

- Compute Engine
  - VM instances - stop and delete all
  - Instance groups - delete all
  - Disks - delete all
  - Metadata - delete all
  - Images - delete all user defined images
  - Health Checks - delete all

- Storage
  - Browser > Buckets - delete all

- VPC Networks
  - VPC Networks - Delete non-default networks and all sub-components
  - External IP addresses - Release Static Addresses
  - Firewall rules - Delete non-default rules

- IAM & Admin
  - IAM - delete any accounts the install explicitly created
  - Service Accounts - delete any accounts the install explicitly created
