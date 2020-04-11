old-dtb := $(dtb-y)
old-dtbo := $(dtbo-y)
dtb-y :=
dtbo-y :=
makefile-path := platform/t18x/lanai/kernel-dts

BUILD_18x_ENABLE=n
ifneq ($(filter y,$(CONFIG_ARCH_TEGRA_18x_SOC) $(CONFIG_ARCH_TEGRA_186_SOC)),)
BUILD_18x_ENABLE=y
endif

dtb-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01.dtb
dtb-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-android.dtb
dtb-$(BUILD_18x_ENABLE) += tegra186-p3636-0002-p3509-0000-a01.dtb
dtb-$(BUILD_18x_ENABLE) += tegra186-p3636-0002-lanai.dtb
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-adafruit-sph0645lm4h.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-adafruit-uda1334a.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-fe-pi-audio.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-hdr40.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-m2ke.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-respeaker-4-mic-array.dtbo
dtbo-$(BUILD_18x_ENABLE) += tegra186-p3636-0001-p3509-0000-a01-respeaker-4-mic-lin-array.dtbo

ifneq ($(dtb-y),)
dtb-y := $(addprefix $(makefile-path)/,$(dtb-y))
dts-include += $(makefile-path)
endif
ifneq ($(dtbo-y),)
dtbo-y := $(addprefix $(makefile-path)/,$(dtbo-y))
endif

dtb-y += $(old-dtb)
dtbo-y += $(old-dtbo)
