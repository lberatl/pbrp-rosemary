#PBRP device tree for Redmi Note 10S (rosemary)

The Redmi Note 10s (codenamed _"rosemary"_) is a high-end, mid-range smartphone from Xiaomi.


| Basic                   | Spec Sheet                                                                                                                     |
| -----------------------:|:------------------------------------------------------------------------------------------------------------------------------ |
| CPU                     | Octa-core                                                                                                                      |
| Chipset                 | Mediatek Helio G95                                                                                                            |
| GPU                     | Mali-G76 MC4                                                                                                                   |
| Memory                  | 6/8 GB RAM                                                                                                                     |
| Shipped Android Version | 11.0                                                                                                                           |
| Storage                 | 64/128 GB                                                                                                              |
| Battery                 | Non-removable Li-Po 5000 mAh battery                                                                                           |
| Display                 | 1080 x 2400 pixels, 19.5:9 ratio (~440 ppi density)                                                                            |
| Camera (Back)(Main)     | 64MP + 8MP + 2MP + 2MP                                                                                |
| Camera (Front)          | 13MP                                                                                                     |

## Device picture
![image](https://github.com/lberatl/pbrp-rosemary/assets/75970161/ad68e379-16eb-45fa-b787-6bfd5b182459)


### Blocking checks

- [X] Correct screen/recovery size
- [X] Working Touch, screen
- [X] Backup to internal/microSD
- [X] Restore from internal/microSD
- [X] reboot to system
- [X] ADB

### Medium checks

- [X] update.zip sideload
- [X] UI colors (red/blue inversions)
- [X] Screen goes off and on
- [X] F2FS/EXT4 Support, exFAT/NTFS where supported
- [X] all important partitions listed in mount/backup lists
- [X] backup/restore to/from external (USB-OTG) storage
- [X] [backup/restore to/from adb](https://gerrit.omnirom.org/#/c/15943/)
- [X] decrypt /data
- [X] Correct date

### Minor checks

- [X] MTP export
- [X] reboot to bootloader
- [X] reboot to recovery
- [X] poweroff
- [X] battery level
- [X] temperature
- [X] set brightness
- [X] vibrate
- [X] screenshot
- [X] partition SD card

## Building

```bash
source build/envsetup.sh
lunch omni_rosemary-eng
mka bootimage
```

> ***NOTE: For OrangeFox/TWRP builds, you can build recovery with [this patch](https://github.com/ItsVixano/android_bootable_recovery/commit/d8f3043a212e15db63ccf76ea0f09a55308e2bdf) if you want to get 60FPS on recovery***

### Special thanks
Woomymy 

