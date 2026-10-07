# SPDX-License-Identifier: GPL-2.0


# Subdirectories
obj-y += usb/


# --- marble: objs upstream restaurados ---
obj-$(CONFIG_SOUND) += soundcore.o
obj-$(CONFIG_DMASOUND) += oss/dmasound/
obj-$(CONFIG_SND) += spi/ atmel/ soc/ sparc/ ppc/ sh/ core/ hda/ parisc/ mips/ synth/ pci/ xen/ x86/ i2c/ firewire/ pcmcia/ arm/ drivers/ isa/ virtio/
obj-$(CONFIG_SND_AOA) += aoa/
obj-$(CONFIG_AC97_BUS) += ac97_bus.o
obj-$(CONFIG_AC97_BUS_NEW) += ac97/
ifeq ($(CONFIG_SND),y)
obj-y += last.o
endif
soundcore-y  := sound_core.o
