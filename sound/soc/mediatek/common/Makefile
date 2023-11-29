is_module = $(filter m, $(CONFIG_MT_SND_SOC_V1) $(CONFIG_MT_SND_SOC_V2) $(CONFIG_MT_SND_SOC_V3) $(CONFIG_MT_SND_SOC_6580) $(CONFIG_MT_SND_SOC_8163) $(CONFIG_MTK_NXP_TFA9897))

ifeq ($(is_module),)
obj-y += auddrv_devtree_parser.o auddrv_underflow_mach.o
else
obj-m += auddrv_devtree_parser.o auddrv_underflow_mach.o
endif
