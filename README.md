# OpenWrt Third-Party Packages Mirror

This repository syncs selected OpenWrt third-party packages for personal builds.

## Included packages

- luci-theme-argon
- luci-app-autoreboot
- luci-app-arpbind
- luci-app-openvpn-server
- luci-app-vlmcsd
- vlmcsd
- luci-app-ramfree
- luci-app-softethervpn
- luci-app-openclash
- fw876/helloworld packages
- softethervpn (4.44-9807 RTM; OpenWrt 24.10 build tested)

## Usage

Add this feed to feeds.conf.default:

```text
src-git mypackages https://github.com/liuxindavid/openwrt-third-party-packages.git;main
```

Then run:

```bash
./scripts/feeds update mypackages
./scripts/feeds install -a -p mypackages
```

## Notes

- The luci-app-autoreboot Makefile is overridden for compatibility.
- fw876/helloworld packages are synced into the feed root.
- SoftEtherVPN 4.44 uses the OpenWrt 24.10 recipe with an Ubuntu 26.04.1 x86_64 Host build workaround.
- It is NOT automatically selected over the official softethervpn package.
- Verify host and target builds, LuCI start/stop and L2TP/IPsec before deployment.
- The SoftEtherVPN package may need version-specific patches.

Synced automatically by GitHub Actions.
