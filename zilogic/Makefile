include $(TOPDIR)/rules.mk

PKG_NAME:=zilogic
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/iamsidhu07/mysrc.git 
PKG_SOURCE_VERSION:= ddfa83769a6b3b7b0f4b308136cf8eb028788d0b
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_SOURCE_VERSION)
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.xz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)

include $(INCLUDE_DIR)/package.mk

define Package/zilogic
	SECTION:=tryout
	CATEGORY:=Zilogic
	TITLE:=Hello World Package
endef

define Build/Compile
	$(MAKE) CC = $(TARGET_CC) -C $(PKG_BUILD_DIR)/ 
endef

define Package/zilogic/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/hello_world $(1)/usr/bin/
endef

$(eval $(call BuildPackage,zilogic))

