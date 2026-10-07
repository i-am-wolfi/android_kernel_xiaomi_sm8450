# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_SLIMBUS) += slimbus.o
slimbus-objs += core.o messaging.o sched.o stream.o

obj-$(CONFIG_SLIM_QCOM_NGD_CTRL) += slim-qcom-ngd-ctrl.o
slim-qcom-ngd-ctrl-objs += qcom-ngd-ctrl.o


# --- marble: objs upstream restaurados ---
slimbus-y				:= core.o messaging.o sched.o stream.o
obj-$(CONFIG_SLIM_QCOM_CTRL) += slim-qcom-ctrl.o
slim-qcom-ctrl-y			:= qcom-ctrl.o
slim-qcom-ngd-ctrl-y			:= qcom-ngd-ctrl.o
