# OpenWrt Third-Party Packages Mirror

This repository syncs selected OpenWrt third-party packages for personal OpenWrt builds.

## Included packages

- luci-theme-argon
- luci-app-autoreboot
- luci-app-arpbind
- luci-app-openvpn-server
- luci-app-vlmcsd
- vlmcsd
- luci-app-ramfree
- luci-app-softethervpn
- fw876/helloworld packages

## Usage

Add this feed to feeds.conf.default:

```bash
src-git mypackages https://github.com/liuxindavid/openwrt-third-party-packages.git;main
```

Then run:

```bash
./scripts/feeds update mypackages
./scripts/feeds install -a -p mypackages
```

Then select packages in make menuconfig.

## Special note

The Makefile of luci-app-autoreboot is automatically overridden for OpenWrt/ImmortalWrt compatibility.

fw876/helloworld is synced into the root of this feed repository, not into a separate helloworld directory.

## Sync source

This repository is automatically synchronized by GitHub Actions.
