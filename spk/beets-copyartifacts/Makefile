SPK_NAME = beets-copyartifacts
SPK_VERS = $(shell date +%Y%m%d)
SPK_REV = 1
SPK_ICON = src/beets.png

PIP = pip3
WHEELS = git+https://github.com/sbarakat/beets-copyartifacts.git\#egg=$(SPK_NAME)
SPK_DEPENDS = "beets>=1.4.9-4"

MAINTAINER = drizzt
DESCRIPTION = "copyartifacts plugin for beets. A plugin that moves non-music files during the import process."
DISPLAY_NAME = beets-copyartifacts

CHANGELOG = ""

HOMEPAGE   = https://github.com/sbarakat/beets-copyartifacts
LICENSE    = MIT

SERVICE_SETUP = src/service-setup.sh

STARTABLE = no

# Pure Python package, make sure ARCH is not defined
override ARCH=

include ../../mk/spksrc.spk.mk
