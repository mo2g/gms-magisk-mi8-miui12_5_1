# gms-magisk-mi8-miui12.5.1

小米 8 升级 MIUI V12.5.1 稳定版，通过 magisk 安装 gms 套件

感谢 qin meng 提供的 [教程](https://zhuanlan.zhihu.com/p/387997993)

# 强烈建议在刷包前通过 TWRP 备份 boot 分区 和 system 分区。

> 我不是专职手机开发，所以没办法保证通用性。如手机环境不同容易遇到意外问题

## 可自行替换 apk 为自己想要的版本,然后放入对应的文件夹，zip 打包

1. [Google Service FrameWork](https://www.apkmirror.com/uploads/?q=google-services-framework) -> GoogleServicesFramework.apk

2. [Google Play Service](https://www.apkmirror.com/uploads/?q=google-play-services) -> GmsCore.apk

3. [Google Play Store](https://www.apkmirror.com/uploads/?q=google-play-store) -> Phonesky.apk

## 可能用到的工具

1. [TWRP for dipper](https://dl.twrp.me/dipper/)

2. [Magisk](https://github.com/topjohnwu/Magisk/releases)

# GMS-Magisk 模块基础结构

```
module.zip
├─META-INF
│  └─com
│      └─google
│          └─android
│               ├── update-binary
│               └── updater-script
├─system
│    └─product
│        ├─etc
│        │  ├─permissions
│        │  │      privapp-permissions-platform.xml
│        │  │
│        │  └─sysconfig
│        │          google-hiddenapi-package-whitelist.xml
│        │          google.xml
│        │
│        └─priv-app
│            ├─GmsCore
│            │      GmsCore.apk
│            │
│            ├─GoogleServicesFramework
│            │      GoogleServicesFramework.apk
│            │
│            └─Phonesky
│                    Phonesky.apk
│
├── customize.sh
├── module.prop

```

![bc5c7a34fee614e08839b511a5840873.jpg](https://i.loli.net/2020/01/30/fOFvI2o9KXqEkJr.jpg)

**这意味着除了以上重要文件 其他的文件如果您不需要的话 可以删掉**

**这是 [Pinkdoge 模块模板](https://github.com/Pinkdoge/magisk-module-template) 您也可以去看看**

**这是 [Magisk 官方新模块模板](https://github.com/HANA-CI-Build-Project/magisk-module-template) 您也可以去看看**

**[Magisk 面具新版模板模块制作教程](https://www.coolapk.com/feed/16056941?shareKey=YWI0MDFiYWE1Y2E3NWUyYzA3ODc~&shareUid=1124169&shareFrom=com.coolapk.market_10.0.1) 感谢@碎念**

有关模块和存储库的更多信息 请查看 [Magisk 官方文档](https://topjohnwu.github.io/Magisk/guides.html)
