# SPDX-License-Identifier: GPL-2.0


# Subdirectories
obj-y += backlight/


# --- marble: objs upstream restaurados ---
obj-$(CONFIG_APERTURE_HELPERS) += aperture.o
obj-$(CONFIG_SCREEN_INFO) += screen_info.o
obj-$(CONFIG_STI_CORE) += sticore.o
obj-$(CONFIG_VGASTATE) += vgastate.o
obj-$(CONFIG_VIDEO) += nomodeset.o cmdline.o
obj-$(CONFIG_HDMI) += hdmi.o
screen_info-y			  := screen_info_generic.o
screen_info-$(CONFIG_PCI)         += screen_info_pci.o
obj-$(CONFIG_VT) += console/
obj-$(CONFIG_FB_STI) += console/
obj-$(CONFIG_LOGO) += logo/
obj-y += fbdev/
obj-$(CONFIG_VIDEOMODE_HELPERS) += videomode.o display_timing.o
ifeq ($(CONFIG_OF),y)
obj-$(CONFIG_VIDEOMODE_HELPERS) += of_videomode.o of_display_timing.o
endif
