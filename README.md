A buildable device tree for  Redmi K30 Ultra (codenamed "cezanne") , written by a beginner. It may contains many non-standard commits, Just ignore these please :)

### Known issues
- Always On Display
- Fingerprint
- Maybe more...

Before starting the build, make sure you have commented out __the third line__ in `device/custom/sepolicy/common/private/property_context`
```
# Aux camera
vendor.camera.aux.packageexcludelist   u:object_r:vendor_persist_camera_prop:s0
# vendor.camera.aux.packagelist          u:object_r:vendor_persist_camera_prop:s0

# Radio
ro.telephony.use_old_mnc_mcc_format    u:object_r:telephony_config_prop:s0

# Wi-Fi Display
media.wfd.                             u:object_r:media_wfd_prop:s0
```
> Firmware used: https://bigota.d.miui.com/22.3.2/miui_CEZANNE_22.3.2_71055969ed_11.0.zip

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
