# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_INTERCONNECT_CLK) += icc-clk.o


# --- marble: objs upstream restaurados ---
CFLAGS_core.o				:= -I$(src)
icc-core-objs				:= core.o bulk.o debugfs-client.o
obj-$(CONFIG_INTERCONNECT) += icc-core.o
obj-$(CONFIG_INTERCONNECT_IMX) += imx/
obj-$(CONFIG_INTERCONNECT_MTK) += mediatek/
obj-$(CONFIG_INTERCONNECT_QCOM) += qcom/
obj-$(CONFIG_INTERCONNECT_SAMSUNG) += samsung/
