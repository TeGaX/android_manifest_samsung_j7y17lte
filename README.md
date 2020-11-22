<div style="text-align:center"><img src="https://img.xda-cdn.com/c0mIjR8lsiHM7l4KXowPzoLHRUE=/https%3A%2F%2Fimg.xda-cdn.com%2FnUBKZfMRYCotfvNioAnDwWlUuak%3D%2Fhttp%253A%252F%252Fi.imgur.com%252FBE3pE0l.png" /></div>

# crDroid 7 - Android 11 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir crdroid-7 ; cd crdroid-7

# Init repo
$ repo init --depth=1 -u https://github.com/crdroidandroid/android.git -b 11.0

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b crdroid-7 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch lineage_j7y17lte-userdebug && mka clean && mka bacon -j$(nproc --all)
```

# For the gcc issue, here is how to fix:
sudo apt-get install gcc-aarch64-linux-gnu # GNU C compiler for the arm64 architecture
sudo apt-get install g++-aarch64-linux-gnu # GNU C++ compiler
mka bacon -j$(nproc --all) CROSS_COMPILE=aarch64-linux-gnu-

And it will be fine :)

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
