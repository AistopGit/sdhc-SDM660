# Qualcomm SDM630/636/660 eMMC Host Controller Driver

This is a driver for the eMMC Host Controller found in devices based on the Qualcomm SDM630/636/660 SoC. The driver works in conjunction with sdport.sys, which implements SD/SDIO/eMMC protocol and WDM interfaces, to provide the host register interface.

## Notes

This driver provides a functional miniport implementation for the Qualcomm SDM630/636/660 eMMC Host Controller. 

However, it does not have support for many more recent features such as:

- UHS-I speed modes.

- HS400

The driver contains dirty fixes, such as disabled PIO and hardcoded voltage.

## Credits

This driver is based on Microsoft's [SDHC sample](https://github.com/microsoft/Windows-driver-samples/tree/main/sd/miniport/sdhc) and utilizes several request handling fixes from [dwcsdhc](https://github.com/worproject/Rockchip-Windows-Drivers/tree/master/drivers/sd/dwcsdhc).