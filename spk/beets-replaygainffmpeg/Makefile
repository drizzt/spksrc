SPK_NAME = beets-replaygainffmpeg
SPK_VERS = $(shell date +%Y%m%d)
SPK_REV = 1
SPK_ICON = src/beets.png

PIP = pip3
WHEELS = git+https://github.com/drizzt/beets-replaygainffmpeg.git\#egg=$(SPK_NAME)
SPK_DEPENDS = "beets>=1.4.9-4 ffmpeg"

MAINTAINER = drizzt
DESCRIPTION = "ffmpeg replaygain plugin for beets \(ripped from beets master git\)."
DISPLAY_NAME = $(SPK_NAME)

CHANGELOG = ""

HOMEPAGE   = https://github.com/drizzt/beets-replaygainffmpeg
LICENSE    = MIT

SERVICE_SETUP = src/service-setup.sh

STARTABLE = no

# Pure Python package, make sure ARCH is not defined
override ARCH=

include ../../mk/spksrc.spk.mk
