## A simple build guide for AOSP-based ROM on _cezanne_ is in [Wiki](https://github.com/coolscode/device_xiaomi_cezanne/wiki) now!
A buildable device tree for the __Redmi K30 Ultra__ (codenamed _"cezanne"_) written by beginners, borrowing a lot from the RMX3031, chopin, atom and the original cezanne device tree. It may contains many non-standard commits, Just ignore these please :P

💖 Thanks a lot to  
> RMX3031: [@ManshuTyagi](https://github.com/ManshuTyagi) , [@Nishant Kumar](https://github.com/nishant6342) ,  
chopin: [@Yuyuko](https://github.com/Yuyuko1024) ,  
atom: [@HuaLiMao-AQ](https://github.com/HuaLiMao-AQ) , [@Jale Shaw](https://github.com/xjl12) ,  
cezanne: [@Xayah](https://github.com/XayahSuSuSu) , [@nzlov](https://github.com/nzlov) , [@ZhcnPanda](https://github.com/ZhcnPanda) , [@Raspberry Kan](https://github.com/Raspberry-Monster) ,  
xaga: [@Wbscript](https://github.com/wbs306) ,  
rubens: [@YuKongA](https://github.com/YuKongA) ,  
RMX2020: [@Sarthak Roy](https://github.com/sarthakroy2002) ,   
RM6785: [@ѕαмαя νιѕρυтє](https://github.com/SamarV-121) ,  
begonia: [@Simone Esposito](https://github.com/DarkJoker360) ,  [@Zinadin Zidan](https://github.com/ZIDAN44) ,  
cannon: [@LinkBoi00](https://github.com/LinkBoi00) , [@Vaisakh Murali](https://github.com/mvaisakh) ,  
ares: [@Tkpointz](https://github.com/Tkpointz) , [@SagarMakhar](https://github.com/SagarMakhar) ,  
Phh-Treble: [@Pierre-Hugues HUSSON](https://github.com/phhusson)  
and many others contributed to it.

### Known issues
- Bluetooth audio (new)
- Hands-free volume adjustment when taking a call
- Deep sleep when AOD is on
- Power-off Charging frame
- DT2W & DC-Dimming
- SELinux: Permissive
- Maybe more...

### NOTICE
__Before starting the build, make sure you have applied [patches](https://github.com/coolscode/patches) for [AcmeUI](https://github.com/AcmeUI) (branch 'taffy') source code with__ 
```
git clone https://github.com/coolscode/patches
bash patches/apply.sh acme
```

__Prebuilt vendor__ and __prebuilt kernel__ are used for now  
Recommended firmware:
> Recovery ROM: https://bigota.d.miui.com/V13.0.3.0.SJNCNXM/miui_CEZANNE_V13.0.3.0.SJNCNXM_4645d9915a_12.0.zip  
> Fastboot ROM: not released yet

Recommended Recovery:
> OrangeFox R12.1: https://github.com/coolscode/ofrp_device_xiaomi_cezanne/releases  

__Now the OrangeFox Recovery cannot handle the fbe encryption of android 13. Prepare an OTG-USB storage or use adb sideload to flash packages for now!__

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
