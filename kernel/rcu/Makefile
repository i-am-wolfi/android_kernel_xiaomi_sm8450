# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_RCU_TORTURE_TEST) += rcutorture.o


# --- marble: objs upstream restaurados ---
obj-y += update.o sync.o
obj-$(CONFIG_TREE_SRCU) += srcutree.o
obj-$(CONFIG_TINY_SRCU) += srcutiny.o
obj-$(CONFIG_RCU_SCALE_TEST) += rcuscale.o
obj-$(CONFIG_RCU_REF_SCALE_TEST) += refscale.o
obj-$(CONFIG_TREE_RCU) += tree.o
obj-$(CONFIG_TINY_RCU) += tiny.o
obj-$(CONFIG_RCU_NEED_SEGCBLIST) += rcu_segcblist.o
