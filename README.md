# Evolution-X

### How to build ###

```bash
# Create dirs
$ mkdir evox ; cd evox

# Init repo
$ repo init --depth=1 -u https://github.com/Evolution-X/manifest -b ten

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b evox .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch aosp_j7y17lte-user && mka clean && mka bacon -j$(nproc --all)`
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
