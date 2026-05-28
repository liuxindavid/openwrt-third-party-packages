# SPDX-License-Identifier: Apache-2.0
#
# Copyright (c) 2025 ImmortalWrt.org

include $(TOPDIR)/rules.mk

LUCI_TITLE:=LuCI support for Scheduled Reboot
LUCI_DEPENDS:=

define Package/luci-app-autoreboot/conffiles
/etc/config/autoreboot
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
