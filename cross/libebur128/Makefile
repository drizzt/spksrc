PKG_NAME = libebur128
PKG_VERS = 1.2.4
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/jiixyj/libebur128/archive
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = https://github.com/jiixyj/libebur128
COMMENT  = A library that implements the EBU R 128 standard for loudness normalisation.
LICENSE  = MIT

CONFIGURE_TARGET = libebur128_custom_configure

CMAKE_ARGS = -DCMAKE_INSTALL_PREFIX=$(INSTALL_PREFIX)
CMAKE_ARGS += -DCMAKE_BUILD_TYPE=Release
CMAKE_ARGS += -DCMAKE_INSTALL_LIBDIR=lib
CMAKE_ARGS += -DBUILD_STATIC_LIBS=OFF

include ../../mk/spksrc.cross-cc.mk

.PHONY: libebur128_custom_configure
libebur128_custom_configure:
	$(RUN) cmake $(CMAKE_ARGS)
