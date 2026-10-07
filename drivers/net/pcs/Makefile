# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_PCS_XPCS) += pcs-xpcs.o
pcs-xpcs-objs += pcs-xpcs-plat.o pcs-xpcs-nxp.o pcs-xpcs-wx.o pcs-xpcs.o

obj-$(CONFIG_PCS_QCOM) += pcs-xpcs-qcom.o


# --- marble: objs upstream restaurados ---
pcs_xpcs-$(CONFIG_PCS_XPCS)	:= pcs-xpcs.o pcs-xpcs-plat.o \
				   pcs-xpcs-nxp.o pcs-xpcs-wx.o
obj-$(CONFIG_PCS_XPCS) += pcs_xpcs.o
obj-$(CONFIG_PCS_LYNX) += pcs-lynx.o
obj-$(CONFIG_PCS_MTK_LYNXI) += pcs-mtk-lynxi.o
obj-$(CONFIG_PCS_RZN1_MIIC) += pcs-rzn1-miic.o
