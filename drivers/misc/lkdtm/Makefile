# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

obj-$(CONFIG_LKDTM) += lkdtm.o
lkdtm-objs += core.o bugs.o heap.o perms.o refcount.o rodata_objcopy.o usercopy.o stackleak.o cfi.o fortify.o
lkdtm-$(CONFIG_PPC_64S_HASH_MMU) += powerpc.o

OBJCOPYFLAGS :=
OBJCOPYFLAGS_rodata_objcopy.o	:= \
			--rename-section .noinstr.text=.rodata,alloc,readonly,load,contents
targets += rodata.o rodata_objcopy.o
$(obj)/rodata_objcopy.o: $(obj)/rodata.o FORCE
	$(call if_changed,objcopy)

# --- marble: objs upstream restaurados ---
lkdtm-$(CONFIG_LKDTM)		+= core.o
lkdtm-$(CONFIG_LKDTM)		+= bugs.o
lkdtm-$(CONFIG_LKDTM)		+= heap.o
lkdtm-$(CONFIG_LKDTM)		+= perms.o
lkdtm-$(CONFIG_LKDTM)		+= refcount.o
lkdtm-$(CONFIG_LKDTM)		+= rodata_objcopy.o
lkdtm-$(CONFIG_LKDTM)		+= usercopy.o
lkdtm-$(CONFIG_LKDTM)		+= stackleak.o
lkdtm-$(CONFIG_LKDTM)		+= cfi.o
lkdtm-$(CONFIG_LKDTM)		+= fortify.o
KASAN_SANITIZE_stackleak.o	:= n
CFLAGS_REMOVE_rodata.o			+= $(CC_FLAGS_LTO) $(RETHUNK_CFLAGS) $(CC_FLAGS_CFI)
OBJCOPYFLAGS :=
$(obj)/rodata_objcopy.o: $(obj)/rodata.o FORCE
	$(call if_changed,objcopy)
