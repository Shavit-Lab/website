# ZFS
Useful commands:
- List user quotas: `sudo zfs userspace <filesystem name e.g. tank/root>`
- Set user quota to certain number of gigabytes: `sudo zfs set userquota@<username>=<amount>G tank/root`
- Reset zfs system (might be necessary to activate new quotas): `sudo systemctl zfs.target`