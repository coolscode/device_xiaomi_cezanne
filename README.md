## A simple build guide for AOSP-based ROM on _cezanne_ is in [Wiki](https://github.com/coolscode/device_xiaomi_cezanne/wiki) now!
A buildable device tree for the __Redmi K30 Ultra__ (codenamed _"cezanne"_) written by beginners, borrowing a lot from the RMX3031, chopin, atom and the original cezanne device tree. It may contains many non-standard commits, Just ignore these please :P

💖 Thanks a lot to  
> RMX3031: [@ManshuTyagi](https://github.com/ManshuTyagi) ,  
chopin: [@Yuyuko](https://github.com/Yuyuko1024) ,  
atom: [@HuaLiMao-AQ](https://github.com/HuaLiMao-AQ) , [@Jale Shaw](https://github.com/xjl12) ,  
cezanne: [@Xayah](https://github.com/XayahSuSuSu) , [@nzlov](https://github.com/nzlov) , [@ZhcnPanda](https://github.com/ZhcnPanda) , [@Raspberry Kan](https://github.com/Raspberry-Monster)  
and others contributed to it.

### Known issues
- Volume adjustment when taking a call
- Deep sleep when AOD is on
- Occasional high brightness on screen unlock via UDFPS
- SELinux: Permissive
- Maybe more...

### NOTICE
Before starting the build, make sure you have __commented out the third line__ in `device/custom/sepolicy/common/private/property_context`  
If not, it will cause __bootloop__

```
# Aux camera
vendor.camera.aux.packageexcludelist   u:object_r:vendor_persist_camera_prop:s0
#vendor.camera.aux.packagelist          u:object_r:vendor_persist_camera_prop:s0

# Radio
ro.telephony.use_old_mnc_mcc_format    u:object_r:telephony_config_prop:s0

# Wi-Fi Display
media.wfd.                             u:object_r:media_wfd_prop:s0
```

__Prebuilt vendor__ and __prebuilt kernel__ are used for now  
Recommended firmware:
> Recovery ROM: https://bigota.d.miui.com/V13.0.2.0.SJNCNXM/miui_CEZANNE_V13.0.2.0.SJNCNXM_3842b0be60_12.0.zip  
> Fastboot ROM: not released yet

Recommended Recovery:
> OrangeFox R12.1: https://github.com/coolscode/ofrp_device_xiaomi_cezanne/releases/tag/v1.1

now the twrp recovery cannot handle the fbe encryption of android 12
to access data partition in recovery, you have to get over encryption, elaborated methods are here
1) get adb shell under recovery
2) `mount /dev/block/dm-1 /vendor`
3) edit __fstab.mt6889__, __fstab.mt6885__ and __fstab.emmc__ with the same modification:  
`busybox vi /vendor/etc/fstab.mt6889`, `busybox vi /vendor/etc/fstab.mt6885`, `busybox vi /vendor/etc/fstab.emmc`  
navigate to the 22nd line, the line starts with /dev/block/by-name/userdata
at the tail of this line, change __'fileencryption'__ to __'encryptable'__

If you have ideas to improve the device tree, open a pull request or join us at any time!


---
Device configuration for Redmi K30 Ultra

=========================================

The Redmi K30 Ultra (codenamed _"cezanne"_) is a high-end smartphone from Xiaomi.

It was announced on August 2020. Release date was August 2020.

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
SoC     | Mediatek MT6889Z Dimensity 1000+ (7nm)
CPU     | Octa-core (4x2.6 GHz Cortex-A77 & 4x2.0 GHz Cortex-A55)
GPU     | Mali-G77 MC9
Memory  | 128GB 6GB RAM, 128GB 8GB RAM, 256GB 8GB RAM, 512GB 8GB RAM
Shipped Android Version | 10.0 with MIUI 12
Storage | 128/256/512 GB
Battery | Li-Po 4500 mAh, non-removable
Display | 1080 x 2400 pixels, 20:9 ratio, 6.67 inches, AMOLED, 120Hz, HDR10+, 500 nits
Camera  | 64MP(wide) 13MP(ultrawide) 5MP(telephoto macro) 2MP(depth)
## Device picture

![Redmi K30 Ultra 5G ](https://fdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-redmi-k30-ultra-1.jpg "Redmi K30 Ultra 5G")
