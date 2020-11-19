<div style="text-align:center"><img src="https://www.xda-developers.com/files/2019/03/POSP-Potato-Open-Sauce-Project-810x298_c.png" /></div>

# POSP - Android 10 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir posp ; cd posp

# Init repo
$ repo init --depth=1 -u https://github.com/PotatoProject/manifest.git -b croquette-release

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b potato .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch potato_j7y17lte-userdebug && mka clean && mka bacon -j$(nproc --all)
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
