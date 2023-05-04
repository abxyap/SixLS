DEBUG=0
FINALPACKAGE=1
GO_EASY_ON_ME=1

THEOS_PACKAGE_SCHEME = rootless

THEOS_USE_NEW_ABI=1
TARGET = iphone:14.5:14.5
ARCHS = arm64 arm64e

THEOS_DEVICE_IP = 127.0.0.1 -p 2222


INSTALL_TARGET_PROCESSES = SpringBoard

include $(THEOS)/makefiles/common.mk

TWEAK_NAME = SixLS
SixLS_FILES = $(wildcard *.swift) $(wildcard *.m) Tweak.x
SixLS_PRIVATE_FRAMEWORKS = UserNotificationsKit
SixLS_CFLAGS = -fobjc-arc -I./Headers
SixLS_SWIFTFLAGS += -DTWEAK

include $(THEOS_MAKE_PATH)/tweak.mk
