# Needed since this subdir is symlinked in the main Kernel tree
# without this our samsung subdir is NOT cleaned.
clean-files := *.o *.ko

#
# Maxwell BT
obj-$(CONFIG_SCSC_BT) += scsc_bt.o
scsc_bt-y += scsc_bt_module.o scsc_shm.o scsc_avdtp_detect.o scsc_bt_dump.o

ccflags-y += $(CONFIG_SAMSUNG_MAXWELL_EXTRA)
## See sibling scsc/ Makefile for an explanation of the reasons of
## the following ifeq/else
ifeq ($(CONFIG_SCSC_DEBUG), m)
ccflags-y += -DCONFIG_SCSC_PRINTK
else
ccflags-$(CONFIG_SCSC_DEBUG) += -DCONFIG_SCSC_PRINTK
endif

