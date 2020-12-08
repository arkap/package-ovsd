include $(TOPDIR)/rules.mk

PKG_NAME:=ovsd
PKG_VERSION:=2020-12-08
PKG_RELEASE:=$(PKG_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/arkap/ovsd.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=3a03476e2fececed3752ba4e68c92e71160c7db1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_MAINTAINER:=Arne Kappen <arne.kappen@hhi.fraunhofer.de>

PKG_BUILD_PARALLEL:=1

PKG_LICENSE:=GPL-2.0

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk


define Package/ovsd
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+openvswitch +libubox +libubus +netifd +libuci
  TITLE:=Open vSwtich device handler for netifd
  MAINTAINER:=Arne Kappen <arne.kappen@hhi.fraunhofer.de>
endef

define Package/ovsd/description
  External device handler adding Open vSwitch support to netifd.
endef

define Package/ovsd/install
	$(INSTALL_DIR) $(1)/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ovsd $(1)/sbin/
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,ovsd))
