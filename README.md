# Rooting-a-Nokia-device

## Introduction
Rooting a Nokia device can unlock a plethora of possibilities for customization, improved performance, and access to a broader range of applications. This guide is a culmination of my personal experience in successfully rooting a Nokia 1 device, and I believe the steps are adaptable for other Nokia models as well.

## Why Rooting a Nokia Device Is Challenging
Rooting Nokia devices presents unique challenges due to several factors:
- **Secure Bootloader:** Nokia devices often come with a securely locked bootloader, which is the first step in the rooting process. Unlocking it can be complex and requires specific tools and instructions.
- **Firmware Variations:** Different models and regions have varying firmware versions, making a one-size-fits-all approach difficult.
- **Sparse Resources:** There is a lack of comprehensive, model-specific rooting guides for Nokia devices, which makes the process more daunting for beginners.
- **Risk of Bricking:** Incorrect rooting steps have a higher risk of bricking Nokia devices due to their specific software and hardware configurations.

## Rooting instructions
1. Download and extract the latest OTA update
2. Copy boot.img to desktop
3. Copy magisk apk file to the mobile device
4. Install Magisk on the device
5. Copy boot.img to the device
6. Patch the copied img file using magisk
7. Copy the patched img file file to PC
8. Follow one of the following two methods to flash the patched img file

#### Using SPF flash tool

1. Download Smart Phone Flash (SPF) Tool for Linux (Tested v5.2208)
2. Extract it and run ```flash_tool```
3. Load the scatter files in SPF Tool
4. Uncheck everything except the boot partition to be flashed
5. Click on the path of the stock boot img and select the patched boot img file
6. Click on the download button
7. Connect device to PC via USB cable
8. Wait for process to complete

#### Using fastboot
Note: This method might factory reset the device. Re-install Magisk on boot and grant root access when prompted.
1. ```adb reboot-bootloader```
2. ```fastboot devices```
3. Unlock the bootloader: ```fastboot oem key <insert md5 hash of serial number>```
4. Flash the patched image file: ```fastboot flash boot <path to patched img>```

## Contributing
Contributions to this repository are welcome! Whether it's refining the existing guide, adding support for more Nokia models, or providing translations, your input is valuable.

## Disclaimer
Rooting a device comes with its risks. This guide is provided "as is," without warranty of any kind. By following these instructions, you're doing so at your own risk.

Happy Rooting!


