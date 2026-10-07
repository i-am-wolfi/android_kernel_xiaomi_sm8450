# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_SND_USB_AUDIO_QMI) += snd-usb-audio-qmi.o
snd-usb-audio-qmi-objs += usb_audio_qmi_svc.o usb_audio_qmi_v01.o


# --- marble: objs upstream restaurados ---
snd-usb-audio-y := 	card.o \
			clock.o \
			endpoint.o \
			format.o \
			helper.o \
			implicit.o \
			mixer.o \
			mixer_quirks.o \
			mixer_scarlett.o \
			mixer_scarlett2.o \
			mixer_us16x08.o \
			mixer_s1810c.o \
			pcm.o \
			power.o \
			proc.o \
			quirks.o \
			stream.o \
			validate.o
snd-usb-audio-$(CONFIG_SND_USB_AUDIO_MIDI_V2) += midi2.o
snd-usb-audio-$(CONFIG_SND_USB_AUDIO_USE_MEDIA_CONTROLLER) += media.o
snd-usbmidi-lib-y := midi.o
obj-$(CONFIG_SND_USB_AUDIO) += snd-usb-audio.o snd-usbmidi-lib.o
obj-$(CONFIG_SND_USB_UA101) += snd-usbmidi-lib.o
obj-$(CONFIG_SND_USB_USX2Y) += snd-usbmidi-lib.o
obj-$(CONFIG_SND_USB_US122L) += snd-usbmidi-lib.o
obj-$(CONFIG_SND) += caiaq/ hiface/ misc/ bcd2000/ 6fire/ usx2y/
obj-$(CONFIG_SND_USB_LINE6) += line6/
