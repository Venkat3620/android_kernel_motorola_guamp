ifneq ($(filter m y,$(CONFIG_INPUT_TOUCHSCREEN_HIMAX_V3_MMI_ENABLE_PALM)),)
	EXTRA_CFLAGS += -DHIMAX_PALM_SENSOR_EN
endif

ifneq ($(filter m y,$(CONFIG_INPUT_HIMAX_V3_MMI_ENABLE_DOUBLE_TAP)),)
	EXTRA_CFLAGS += -DHIMAX_V2_SENSOR_EN
endif

ifneq ($(filter m y,$(CONFIG_INPUT_HIMAX_V3_MMI_ENABLE_MULTI_BIN)),)
	EXTRA_CFLAGS += -DHIMAX_V2_MULTI_BIN
endif

obj-$(CONFIG_INPUT_HIMAX_V3_MMI) += himax_v3_mmi.o

himax_v3_mmi-objs += himax_platform_QCT_SPI.o
EXTRA_CFLAGS += -D__HIMAX_PLATFORM_SPI__ \
		-DHX_ZERO_FLASH

himax_v3_mmi-objs += himax_common.o
himax_v3_mmi-objs += himax_debug.o
himax_v3_mmi-objs += himax_ic_incell_core.o
himax_v3_mmi-objs += himax_inspection.o

# Support IC
obj-$(CONFIG_INPUT_HIMAX_V3_MMI) += himax_v3_mmi_hx83102d.o
himax_v3_mmi_hx83102d-objs += support_ic/himax_v3_mmi_hx83102d/himax_ic_HX83102d.o
