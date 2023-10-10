include $(srctree)/drivers/misc/mediatek/Makefile.custom

EXTRA_CFLAGS += -DUSE_SSUSB_QMU


musb_hdrc-$(CONFIG_USB_MTK_HDRC) := musb_core.o
musb_hdrc-$(CONFIG_USB_MTK_HDRC)	+= musb_gadget_ep0.o musb_gadget.o
musb_hdrc-$(CONFIG_USB_MTK_HDRC)	+= musb_virthub.o musb_host.o
musb_hdrc-$(CONFIG_DEBUG_FS)		+= musb_debugfs.o
musb_hdrc-$(CONFIG_DEBUG_FS) += musb_debugfs.o
