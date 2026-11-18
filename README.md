<div align="center">

<img src="assets/Banner.svg" alt="CarbonOS" width="100%">

<img src="assets/tagline.svg" alt="Forged Under Pressure" width="420">

[![Android](https://img.shields.io/badge/Android-17-00E5C7?style=for-the-badge&logo=android&logoColor=white&labelColor=000000)](https://github.com/CarbonOS-Rom)
[![Telegram](https://img.shields.io/badge/Telegram-Channel-00E5C7?style=for-the-badge&logo=telegram&logoColor=white&labelColor=000000)](https://t.me/CarbonOSaosp)
[![License](https://img.shields.io/badge/License-Apache_2.0-00E5C7?style=for-the-badge&labelColor=000000)](#license)

**A clean, minimal Android ROM built for speed, stability and personal style.**

</div>

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="getting-started"></a>
<img src="assets/h-getting-started.svg" alt="Getting Started" width="100%">

**1. Initialize the repo**
```bash
repo init -u https://github.com/CarbonOS-Rom/manifest -b 1.0 --git-lfs
```

**2. Sync the sources**
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

**3. Build**
```bash
. build/envsetup.sh
crystal <devicecodename> userdebug   # or: user
carbon b
```

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="configuration"></a>
<img src="assets/h-configuration.svg" alt="Configuration Flags" width="100%">

Add these to your `device.mk` or `BoardConfig.mk`.

### Essentials

| Flag | Description | Values |
|:-----|:------------|:-------|
| `CARBONOS_MAINTAINER` | Maintainer name shown in the ROM | `"Your Name"` |
| `WITH_GMS` | Include Google Mobile Services | `true` / `false` |

### GMS Variants *(optional)*

| Flag | Description | Default |
|:-----|:------------|:--------|
| `TARGET_USES_MINI_GAPPS` | Minimal GApps package | `false` |
| `TARGET_USES_PICO_GAPPS` | Pico GApps package | `false` |
| `TARGET_DEFAULT_PIXEL_LAUNCHER` | Ship Pixel Launcher as default *(GMS builds only)* | `false` |

> [!NOTE]
> With `WITH_GMS := true` and no variant set, the full GMS package is included.

### Interface

| Flag | Description | Default |
|:-----|:------------|:--------|
| `TARGET_ENABLE_BLUR` | System-wide blur effects | `false` |

### Features

| Flag | Description | Default |
|:-----|:------------|:--------|
| `TARGET_SUPPORTS_QUICK_TAP` | Quick Tap gesture | `false` |
| `BYPASS_CHARGE_SUPPORTED` | Bypass charging | `false` |

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="device-info"></a>
<img src="assets/h-device-info.svg" alt="My Device Info" width="100%">

> [!IMPORTANT]
> Coming in a future version.

Fill in the hardware specs shown on the *My device* page:

```properties
ro.carbon.device.name=Poco X3
ro.carbon.display=1080 x 2400, 120 Hz
ro.carbon.screen=6.67" IPS LCD
ro.carbon.soc=Snapdragon® 732G
ro.carbon.platform=SM7150-AC
ro.carbon.battery=6000 mAh
ro.carbon.camera=64MP + 13MP + 2MP
ro.carbon.front=20MP
```

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="example"></a>
<img src="assets/h-example.svg" alt="Example" width="100%">

> [!WARNING]
> This example still needs testing.

```makefile
# Maintainer
CARBONOS_MAINTAINER := "John Doe"

# GMS (mini)
WITH_GMS := true
TARGET_USES_MINI_GAPPS := true
TARGET_DEFAULT_PIXEL_LAUNCHER := true

# Interface
TARGET_ENABLE_BLUR := true

# Features
TARGET_SUPPORTS_QUICK_TAP := true
BYPASS_CHARGE_SUPPORTED := true
```

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="contributing"></a>
<img src="assets/h-contributing.svg" alt="Contributing" width="100%">

Contributions are welcome — open a pull request on the relevant repo.

**Want to maintain CarbonOS for your device?** Read the [maintainer requirements](https://github.com/CarbonOS-Rom/maintainership/issues/new/choose) and apply.

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<a id="credits"></a>
<img src="assets/h-credits.svg" alt="Credits" width="100%">

CarbonOS stands on the work of these projects:

<div align="center">

| [<img src="https://avatars.githubusercontent.com/u/24304779?s=200&v=4" width="72"><br>**LineageOS**](https://github.com/LineageOS) | [<img src="https://avatars.githubusercontent.com/u/197353021?s=200&v=4" width="72"><br>**RisingOS Revived**](https://github.com/RisingOS-Revived) | [<img src="https://avatars.githubusercontent.com/u/70501337?s=200&v=4" width="72"><br>**YAAP**](https://github.com/Yaap) | [<img src="https://avatars.githubusercontent.com/u/9610671?s=200&v=4" width="72"><br>**crDroid**](https://github.com/crdroidandroid) | [<img src="https://avatars.githubusercontent.com/u/165590896?s=200&v=4" width="72"><br>**Evolution X**](https://github.com/Evolution-X) |
|:---:|:---:|:---:|:---:|:---:|
| [<img src="https://avatars.githubusercontent.com/u/106430773?s=200&v=4" width="72"><br>**The Parasite Project**](https://github.com/TheParasiteProject) | [<img src="https://avatars.githubusercontent.com/u/38539471?s=200&v=4" width="72"><br>**PixelExperience**](https://github.com/PixelExperience) | [<img src="https://avatars.githubusercontent.com/u/82160282?s=200&v=4" width="72"><br>**PixelOS**](https://github.com/pixelos-aosp) | [<img src="https://avatars.githubusercontent.com/u/71037289?s=200&v=4" width="72"><br>**DerpFest**](https://github.com/DerpFest-AOSP) | [<img src="https://avatars.githubusercontent.com/u/43355064?s=200&v=4" width="72"><br>**SuperiorOS**](https://github.com/superioros) |
| [<img src="https://avatars.githubusercontent.com/u/68725628?s=200&v=4" width="72"><br>**Project Awaken**](https://github.com/Project-Awaken) | [<img src="https://avatars.githubusercontent.com/u/197447202?s=200&v=4" width="72"><br>**AxionOS**](https://github.com/AxionAOSP) | [<img src="https://avatars.githubusercontent.com/u/140271839?s=200&v=4" width="72"><br>**MistOS**](https://github.com/Project-Mist-OS) | | |

*…and everyone else who keeps custom ROM development alive.*

</div>

<p align="center"><img src="assets/divider.svg" alt="" width="100%"></p>

<div align="center">

<a id="license"></a>
<img src="assets/h-license.svg" alt="License" width="100%">

```
Copyright (C) 2026 CarbonOS

Licensed under the Apache License, Version 2.0
```

<img src="assets/footer.svg" alt="Made with ⬢ by the CarbonOS Team" width="320">

</div>
