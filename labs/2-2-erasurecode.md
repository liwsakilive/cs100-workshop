### Get erasure code profile
- ceph osd erasure-code-profile ls
- ceph osd erasure-code-profile get default

### Create erasurecode rule
- ceph osd crush rule create-erasure {name} {profile-name}

### Create new profile
- ceph osd erasure-code-profile set {profile-name} crush-failure-domain=rack,k=2,m=1 (--force)

### Create erasurecode pool 
- ceph osd pool create {pool-name} {pg} erasure {profile}