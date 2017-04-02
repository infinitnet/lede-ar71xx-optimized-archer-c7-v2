# TP-Link Archer C7 V2 AC1750 Optimized LEDE Firmware

## Features
- Extended & optimized build for [TP-Link Archer C7 V2](https://lede-project.org/toh/hwdata/tp-link/tp-link_archer_c7_ac1750_v2.0) only based on [latest LEDE trunk source](https://git.lede-project.org/?p=source.git)
- Baked using latest GCC version 6.3 with -O3, 74kc, binutils 2.27 and various patches to maximize performance
- LuCI SSL Web Interface
- VPN ready (OpenVPN, L2TP, IPSec, GRE, IPIP, PPTP)
- TOR ready
- DNSCrypt using OpenNIC for your security, privacy & freedom
- QoS with SQM (cake & more)
- Simple Adblock available in LuCI
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
- vim, nano, tcpdump-mini, htop, rsync, iproute2, ipset, wget, curl, ethtool, dmesg, grep, tar & many more

## FAQ
**Can I block ads with this firmware?**

Yes! Open `/etc/config/dnscrypt-proxy` with `nano` or `vim` and change `option resolver 'fvz-anyone'` to `option resolver 'default.ns1.adguard.com'`. Then restart DNSCrypt with `service dnscrypt-proxy restart`.

**Do you offer any quality assurance?**

Sort of. I push releases manually after testing the builds on my own C7, which prevents major issues with the releases you can find here. The nightly builds are untested!

**My clients are unable to connect to the internet after flashing this firmware!**

Just reboot your router once and it should work. If it still doesn't work, make sure that `dnscrypt-proxy` is enabled and working. SSH to your router and do `service dnscrypt-proxy enable; service dnscrypt-proxy restart`.

## Changelog
- 2017-04-02
  - Upstream updates
  - Added patches and files source code
  - Added nightly builds based on latest release configs to keep up with upstream developments
- 2017-04-01
  - pppossh added
  - openssh-sftp-server added
  - Many netfilter modules removed to increase throughput
  - Kernel settings fine-tuned (sysctl)
  - Many of [gwlim's patches](https://github.com/gwlim/mips74k-ar71xx-lede-patch) cherry picked & ported
  - Many minor changes aimed at improving performance
- 2017-03-19
  - Upstream updates
  - LuCI Material theme added
  - TOR support added
  - rfkill support added
  - ca-certificates added
  - LuCI simple-adblock added
  - Possible performance improvements
  - MIPS16 instructions removed
  - Switched from ath10k-ct to vanilla ath10k
  - Tweaked kernel config
- 2017-03-01
  - Upstream updates
- 2017-02-22
  - Upstream updates
- 2017-02-19
  - Upstream updates
- 2017-02-14
  - Upstream updates
  - Replaced `wpad-mini` with `wpad`
  - Added `hostapd-utils`
- 2017-02-13
  - Upstream updates
  - Minor bug fixes
- 2017-02-09
  - Upstream updates
  - `openssl-util` added
- 2017-02-08
  - Upstream updates
- 2017-02-07
  - Upstream updates
  - More gcc optimizations
  - DNSCrypt added
  - Added config to GitHub repo

- 2017-02-06
  - Upstream updates
  - Added `rsync`
  - BCP38 added (including LuCI app)
  - Compile everything with `-O3` and `-march=74kc`
  - Use GCC 6.3

- 2017-02-05
  - Upstream updates

- 2017-02-04
  - Initial release
