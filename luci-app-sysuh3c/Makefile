include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-sysuh3c
PKG_VERSION=1.0
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk

define Package/luci-app-sysuh3c
	SECTION:=luci
	CATEGORY:=LuCI
	SUBMENU:=3. Applications
	TITLE:=SYSU H3C 802.1X Client for LuCI
	PKGARCH:=all
	DEPENDS:=+sysuh3c
endef

define Package/luci-app-sysuh3c/description
	This package contains LuCI configuration pages for SYSU H3C.
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/luci-app-sysuh3c/install
	$(INSTALL_DIR) $(1)/etc/config
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/model/cbi
	$(INSTALL_DIR) $(1)/usr/lib/lua/luci/controller
	
	$(INSTALL_CONF) ./files/root/etc/config/sysuh3c $(1)/etc/config/sysuh3c
	$(INSTALL_BIN) ./files/root/etc/init.d/sysuh3c $(1)/etc/init.d/sysuh3c
	$(INSTALL_DATA) ./files/root/usr/lib/lua/luci/model/cbi/sysuh3c.lua $(1)/usr/lib/lua/luci/model/cbi/sysuh3c.lua
	$(INSTALL_DATA) ./files/root/usr/lib/lua/luci/controller/sysuh3c.lua $(1)/usr/lib/lua/luci/controller/sysuh3c.lua
endef

$(eval $(call BuildPackage,luci-app-sysuh3c))
