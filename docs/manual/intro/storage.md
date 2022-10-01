---
sidebar_position: 3
---

# Storage

My go to storage devices are samsung and seagate. I only ever use samsung SSDs(sata & NVME) and seagate Exos drives.
Please checkout my price comparison for HDDs [here](/docs//manual/intro/hardware-recommendations#hdd-drive-comparison-price).

## Pools

You should have a multi-pools setup:

- media pool (HDD's)
- downloading pool (SSD's)
- app pool (SSD)
- transcoding pool (SSD)

## Permissions

Majority of the truecharts catalog has user/groups permissions for 568(apps). So anytime you make a dataset(s) the permissions should be 568 for both owner and groups.
except for some charts that require `www-data`, please be sure to checkout the charts respective istallation documentations for notes on permissions.

ACL's are not supported and can cause issues, so its heavily advised to _never_ use ACL's and use the correct permissions.

## SMB + Pool
