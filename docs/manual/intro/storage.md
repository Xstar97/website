---
sidebar_position: 3
---

# Storage

My go-to storage devices are samsung and seagate. I only ever use samsung SSDs(sata & NVME) and seagate Exos drives.
Please checkout my price comparison for HDDs [here](/docs//manual/intro/hardware-recommendations#hdd-drive-comparison-price).

## Pools

You should have a multi-pools setup:

- media pool (HDD's)
- downloading pool (SSD's)
- app pool (SSD)
- transcoding pool (SSD)

## Permissions

Majority of the truecharts catalog has owner/groups permissions for `apps` or 568.

So anytime you make a dataset(s) the permissions should be set accordingly except for some charts that require `www-data`, please be sure to checkout the charts respective installation documentations for notes on permissions.

ACL's are not supported and can cause issues, so its heavily advised to _never_ use ACL's and use the correct permissions.

## Using samba with Truecharts

This was written by a user `zasx` from the [truechart's discord](https://discord.gg/BaUXFbZu5b). All credits and love should go to him. this is a accepted solution until bluefin is released.

### Setting up a local user

You need a local user with access to the apps group.
Go to Credentials -> Local Users, click on your local user and click Edit.
Add apps to the Auxiliary Groups.

### Setting up a dataset

Go to Storage, click Add dataset where you want it, give it a name and click Save.
Click the 3 dots behind the new dataset, click View Permissions and click the pen.
Change the user to apps and the group to apps. Check Apply User, Apply Group and click Save.

### Setting up a share

Go to Shares, click Add and select the path to your dataset.
Click Advanced options and put the following in the Auxiliary Parameters field:

```
force user=apps
force group=apps
```