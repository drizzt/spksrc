COMMIT = 54508df30bc888c4d2359576ceb0cc8f2fa8dbdf

PKG_NAME = taglib
PKG_VERS = 1.11.2
PKG_EXT = tar.gz
PKG_DIST_NAME = $(COMMIT).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/taglib/taglib/archive
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-$(COMMIT)

DEPENDS =

HOMEPAGE = https://taglib.github.io
COMMENT  = A Library for reading and editing the meta-data of several popular audio formats.
LICENSE  = LGPL MPL

PATCHES_LEVEL = 1

CONFIGURE_TARGET = taglib_custom_configure

CMAKE_ARGS = -DCMAKE_INSTALL_PREFIX=$(INSTALL_PREFIX)
CMAKE_ARGS += -DCMAKE_BUILD_TYPE=Release
CMAKE_ARGS += -DCMAKE_INSTALL_LIBDIR=lib
CMAKE_ARGS += -DBUILD_SHARED_LIBS=ON

include ../../mk/spksrc.cross-cc.mk

.PHONY: taglib_custom_configure
taglib_custom_configure:
	$(RUN) cmake $(CMAKE_ARGS)
