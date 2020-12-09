<div style="text-align:center"><img src="https://ae01.alicdn.com/kf/HTB1l4wctKuSBuNjSsplq6ze8pXaJ/1-18-Diecast-M-u-cho-Mitsubishi-Lancer-Evolution-X-10-H-p-Kim-M-u.jpg_q50.jpg" /></div>

# EvoX - Mitsubishi A11 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir evox-5 ; cd evox-5

# Init repo
$ repo init --depth=1 -u https://github.com/Evolution-X/manifest.git -b elle

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b EvoX-5 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j32

# Build
$ . build/envsetup.sh && lunch evolution_j7y17lte-userdebug && make bacon -j$(nproc --all)
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
