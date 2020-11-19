<div align=”center”>![AncientOS](https://raw.githubusercontent.com/Ancient-Lab/manifest/ten/ancient.png)</div>
# Ancient OS / Ancient OS Weeabooify - Android 10 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir ancient ; cd ancient

# Init repo for normal Ancient OS
$ repo init --depth=1 -u https://github.com/Ancient-Lab/manifest.git -b ten|
# For Ancient OS Weeabooify
$ repo init --depth=1 -u https://github.com/Ancient-Lab/manifest.git -b ten-weeaboo

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b AncientOS .repo/local_manifests

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
