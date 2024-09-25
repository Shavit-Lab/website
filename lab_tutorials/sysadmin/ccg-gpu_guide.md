# Storage Organization
The memory of a physical machine or "disk" is split into "partitions." The layout of these partitions can be shown with the command `lsblk`. A "filesystem" can be added to a partition to give it the ability to store files. The command `df -aTh` shows the available file systems (which can be traced to the partitions that contains it). This command also shows where the file system lies within the overall directory hierarchy, the filesystem format, and how space much is occupied vs. still available.

# Creating User Accounts
## ZFS Quotas
Useful commands:
- List user quotas: `sudo zfs userspace <filesystem name e.g. tank/root>`
- Set user quota to certain number of gigabytes: `sudo zfs set userquota@<username>=<amount>G tank/root`
- Reset zfs system (might be necessary to activate new quotas): `sudo systemctl zfs.target`