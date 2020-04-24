PKG_NAME = loudgain
PKG_VERS = 0.6.8
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/Moonbase59/loudgain/archive
PKG_DIST_FILE = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/taglib cross/libebur128 cross/ffmpeg

HOMEPAGE = https://github.com/Moonbase59/loudgain
COMMENT  = A loudness normalizer that scans music files and calculates loudness-normalized gain and loudness peak values according to the EBU R128 standard, and can optionally write ReplayGain-compatible metadata.
LICENSE  = BSD

PATCHES_LEVEL = 1

CONFIGURE_TARGET = loudgain_custom_configure

CMAKE_ARGS = -DCMAKE_INSTALL_PREFIX=$(INSTALL_PREFIX)
CMAKE_ARGS += -DCMAKE_BUILD_TYPE=Release
CMAKE_ARGS += -DCMAKE_CROSSCOMPILING=TRUE

include ../../mk/spksrc.cross-cc.mk

.PHONY: loudgain_custom_configure
loudgain_custom_configure:
	$(RUN) cmake $(CMAKE_ARGS)
