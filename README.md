<div style="text-align:center"><img src="https://cdn.pling.com/img/f/d/8/5/7132442ca478bce7f1b6ed392a44c4d3cb53.png" /></div>

# ShapeShift - Android 10 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir ssos ; cd ssos

# Init repo
$ repo init --depth=1 -u https://github.com/ShapeShiftOS/android_manifest.git -b android_10

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b ShapeShift .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j32

# Build
$ . build/envsetup.sh && brunch j7y17lte userdebug
```

# 1: For the gcc issue, here is how to fix:
```bash
Go to the ROM folder
rm -rf prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9
git clone https://github.com/LineageOS/android_prebuilts_gcc_linux-x86_aarch64_aarch64-linux-android-4.9 prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9

And it will be fine :)
```

# 2: Here is how to fix toolchain after clone success:
```bash
make cleaninstall
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
