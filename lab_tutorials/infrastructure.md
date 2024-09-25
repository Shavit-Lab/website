# ZFS
Useful commands:
- List user quotas: `sudo zfs userspace <filesystem name e.g. tank/root>`
- Set user quota to certain number of gigabytes: `sudo zfs set userquota@<username>=<amount>G tank/root`
- Reset zfs system (only do this if the quota is not working, we have found it necessary only sometimes): `sudo systemctl restart zfs.target`
