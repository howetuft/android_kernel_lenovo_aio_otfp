ifneq ($(KERNELRELEASE),)

ifeq ($(CONFIG_MTK_COMBO),y)
	ccflags-y += -I$(src)/inc/
	ccflags-y += -I$(src)/../
	obj-y += conn_drv_init.o
	obj-y += common_drv_init.o
	obj-y += bluetooth_drv_init.o
	obj-y += gps_drv_init.o
	obj-y += fm_drv_init.o
	obj-y += wlan_drv_init.o
ifneq ($(filter "MT6630",$(CONFIG_MTK_COMBO_CHIP)),)
	obj-y += ant_drv_init.o
endif
	
	ifneq ($(filter "MT6620",$(CONFIG_MTK_COMBO_CHIP)),)
		ccflags-y += -DMT6620
	endif
	ifneq ($(filter "MT6628",$(CONFIG_MTK_COMBO_CHIP)),)
		ccflags-y += -DMT6628
	endif
	ccflags-y += -I$(src)/inc/
	ccflags-y += -I$(src)/../
	ccflags-y += -DDEBUG
	CFLAGS_conn_drv_init.o := -DDEBUG
	CFLAGS_common_drv_init.o := -DDEBUG
	CFLAGS_bluetooth_drv_init.o := -DDEBUG
	CFLAGS_gps_drv_init.o := -DDEBUG
	CFLAGS_fm_drv_init.o := -DDEBUG
	CFLAGS_wlan_drv_init.o := -DDEBUG
	CFLAGS_ant_drv_init.o := -DDEBUG

endif

else
    KERNELDIR ?= /lib/modules/$(shell uname -r)/build
    PWD  := $(shell pwd)
default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
endif
