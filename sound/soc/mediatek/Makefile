# MTK Platform Support

is_module = $(filter m, $(CONFIG_MT_SND_SOC_V1) $(CONFIG_MT_SND_SOC_V2) $(CONFIG_MT_SND_SOC_V3) $(CONFIG_MT_SND_SOC_6580) $(CONFIG_MT_SND_SOC_8163) $(CONFIG_MTK_NXP_TFA9897))

ifeq ($(is_module),)
obj-y += common/
else
obj-m += common/
endif

obj-$(CONFIG_MT_SND_SOC_V1) += mt_soc_audio_v1/
obj-$(CONFIG_MT_SND_SOC_V2) += mt_soc_audio_v2/
obj-$(CONFIG_MT_SND_SOC_V3) += mt_soc_audio_v3/
obj-$(CONFIG_MT_SND_SOC_6580) += mt_soc_audio_6580/
obj-$(CONFIG_MT_SND_SOC_8163) += mt_soc_audio_8163/
obj-$(CONFIG_MTK_NXP_TFA9897) += nxp_tfa9897/
