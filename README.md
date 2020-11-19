<div style="text-align:center"><img src="https://img.xda-cdn.com/pG4hAXrYjT_uc-LxMcstI3dwF7g=/https%3A%2F%2Fimg.xda-cdn.com%2F7-P8r5wrQFS_MuRB3kPsjqf-xy0%3D%2Fhttps%253A%252F%252Fgithub.com%252FArrowOS%252Fdocumentation%252Fblob%252Fmaster%252Fmisc%252Flogo.png%253Fraw%253Dtrue" /></div>

# Arrow OS 11 - Android 11 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir arrow ; cd arrow

# Init repo
$ repo init --depth=1 -u https://github.com/ArrowOS/android_manifest.git -b arrow-11.0

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b arrow-11 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch lineage_j7y17lte-userdebug && mka clean && mka bacon -j$(nproc --all)
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
