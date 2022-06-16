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
- Deep sleep (Only takes up half of the standby time) and no deep-sleep time when AOD is on
- Power-off charging
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

__Prebuilt vendor__ and __oss kernel__ are used for now  
Recommended firmware:
> Recovery ROM: https://bigota.d.miui.com/V12.5.11.0.RJNCNXM/miui_CEZANNE_V12.5.11.0.RJNCNXM_30f7f0b596_11.0.zip  
> Fastboot ROM: https://bigota.d.miui.com/V12.5.11.0.RJNCNXM/cezanne_images_V12.5.11.0.RJNCNXM_20220301.0000.00_11.0_cn_chinatelecom_39cae9b023.tgz

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
