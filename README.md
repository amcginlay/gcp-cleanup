# gcp-cleanup

## Steps to clean up a project after typical use

- Network services
  - Cloud DNS - delete all record set entries and containing zones
  - Load Balancers - delete all LBs plus attached resources as prompted (e.g. frontends, backends, certificates, etc.)

- Compute Engine
  - VM instances - stop and delete all
  - Instance groups - delete all
  - Disks - delete all
  - Images - delete __only__ the images created by your project name
  - Metadata - delete all SSH Keys and Metadata
  - Health Checks - delete all

- Storage
  - Browser > Buckets - delete all

- SQL
  - Delete all

- VPC Networks
  - VPC network peering - Delete all 
  - VPC Networks - Delete __non-default__ networks and all sub-components
  - External IP addresses - Release Static Addresses
  - Firewall rules - Delete __non-default__ rules
  
- IAM & Admin (look for names like terraform, opsman, pks, blobstore but __be careful__ to not remove yourself!)
  - IAM - delete any accounts the install __explicitly__ created
  - Service Accounts - delete any accounts the install __explicitly__ created

- Disable APIs (optional)
  - APIs and Services -> Deshboard - hide used APIs then disable all that remain
