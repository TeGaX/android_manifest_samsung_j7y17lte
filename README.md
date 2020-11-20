# Resurrection Remix 8 - Android 10 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir rr ; cd rr

# Init repo
$ repo init --depth=1 -u https://github.com/ResurrectionRemix/platform_manifest.git -b Q

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b RR-8 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch rr_j7y17lte-userdebug && make clean && make bacon -j$(nproc --all)
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
