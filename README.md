# TP-Link Archer C7 V2 AC1750 Optimized LEDE Firmware

## Features
- Extended & optimized build for [TP-Link Archer C7 V2](https://lede-project.org/toh/hwdata/tp-link/tp-link_archer_c7_ac1750_v2.0) only based on [latest LEDE trunk source](https://git.lede-project.org/?p=source.git)
- No config files have been added or modified = default settings for services
- LuCI SSL Web Interface
- Improved [ath10k CT](http://www.candelatech.com/ath10k-10.1.php) drivers & firmware
- VPN client ready (OpenVPN, L2TP, IPSec, GRE, IPIP, PPTP)
- QoS with SQM (cake & more)
- Dynamic DNS support
- WiFi Schedule (disable/enable WiFi at specific times)
- HD Idle (spins down connected hard drives when idle)
- Wake On LAN (WOL)
- UPnP support
- Supports common filesystems (btrfs, exfat, f2fs, ext4, msdos, ntfs, nfs, xfs, fuse, reiserfs, squashfs)
- IPv4-over-IPv6
- Supports bonding, relays and bridges
- BCP38 anti spoofing
- Advanced statistics (graphs)
- vim, nano, tcpdump-mini, htop, rsync, ip, wget, curl, ethtool, dmesg, grep, tar & many more

## Changelog
- 2017-02-06
  - Upstream updates
  - Added `rsync`
  - BCP38 added (including LuCI app)
  - Compile everything with `-O3` and `-march=24kc`

- 2017-02-05
  - Upstream updates

- 2017-02-04
  - Initial release
