# bcm4329 -DGET_CUSTOM_MAC_ENABLE 
DHDCFLAGS = -DLINUX -DBCMDRIVER -DBCMDONGLEHOST -DDHDTHREAD -DBCMWPA2         \
	-DUNRELEASEDCHIP -Dlinux -DDHD_SDALIGN=64 -DMAX_HDR_READ=64           \
	-DDHD_FIRSTREAD=64 -DDHD_GPL -DDHD_SCHED -DBDC -DTOE -DDHD_BCMEVENTS  \
	-DSHOW_EVENTS -DBCMSDIO -DDHD_GPL -DBCMLXSDMMC -DBCMPLATFORM_BUS      \
	-Wstrict-prototypes -DOOB_INTR_ONLY -DCUSTOMER_HW2      \
	-DDHD_USE_STATIC_BUF -DMMC_SDIO_ABORT -DDHD_DEBUG_TRAP -DSOFTAP       \
	-DEMBEDDED_PLATFORM -DARP_OFFLOAD_SUPPORT -DPKT_FILTER_SUPPORT        \
	-DSET_RANDOM_MAC_SOFTAP -DCSCAN -DHW_OOB      \
	-DKEEP_ALIVE -DPNO_SUPPORT -DCUSTOM_OOB_GPIO_NUM=18                   \
	-DCONFIG_WIFI_CONTROL_FUNC -DCUSTOM_SDCC_WIFI_SLOT=3                  \
	-Idrivers/net/wireless/bcm4329 -Idrivers/net/wireless/bcm4329/include

DHDOFILES = dhd_linux.o linux_osl.o bcmutils.o dhd_common.o dhd_custom_gpio.o \
	wl_iw.o siutils.o sbutils.o aiutils.o hndpmu.o bcmwifi.o dhd_sdio.o   \
	dhd_linux_sched.o dhd_cdc.o bcmsdh_sdmmc.o bcmsdh.o bcmsdh_linux.o    \
	bcmsdh_sdmmc_linux.o


obj-$(CONFIG_BCM4329) += bcm4329.o
bcm4329-objs += $(DHDOFILES)
EXTRA_CFLAGS = $(DHDCFLAGS)
EXTRA_LDFLAGS += --strip-debug
