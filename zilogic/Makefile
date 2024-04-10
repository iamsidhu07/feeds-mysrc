include $(TOPDIR)/rules.mk

PKG_NAME:=zilogic
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.xz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/iamsidhu07/mysrc.git
PKG_SOURCE_DATE:=2017-08-02
PKG_MIRROR_HASH:=5ff7f8f237425c09d36e5db1421bf25b

include $(INCLUDE_DIR)/package.mk

define Package/zilogic
  SECTION:=tryout
  CATEGORY:=Zilogic
  TITLE:=Hello World Package
endef

define Build/Compile
    $(TARGET_CC) $(TARGET_CFLAGS) -o $(PKG_BUILD_DIR)/hello_world.o -c $(PKG_BUILD_DIR)/hello.c
    $(TARGET_CC) $(TARGET_LDFLAGS) -o $(PKG_BUILD_DIR)/hello_world $(PKG_BUILD_DIR)/hello_world.o
endef

define Package/zilogic/install
    $(INSTALL_DIR) $(1)/usr/bin
    $(INSTALL_BIN) $(PKG_BUILD_DIR)/hello_world $(1)/usr/bin/
endef

$(eval $(call BuildPackage,zilogic))

