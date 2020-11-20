<div style="text-align:center"><img src="https://img.xda-cdn.com/bYRxY5WSZg35sxpa_Az7Cp9H0dk=/https%3A%2F%2Fi.imgur.com%2FfpLXCS2.png" /></div>

# StatiXOS - Android 11 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir statix ; cd statix

# Init repo
$ repo init --depth=1 -u https://github.com/StatiXOS/android_manifest.git -b 11

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b StatiXOS .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch statix_j7y17lte-userdebug && mka clean && mka bacon -j$(nproc --all)
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
