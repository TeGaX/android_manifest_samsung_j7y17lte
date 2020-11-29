<div style="text-align:center"><img src="https://camo.githubusercontent.com/b328e671bc58ad7a7c8bfe422112e9cdda0046f9170a0113dd5c56b9a3329a51/68747470733a2f2f692e696d6775722e636f6d2f30476e727761552e706e67" /></div>

# BlissROMs 12.12 - Android 10 for Exynos 7870

### How to build ###

```bash
# Create dirs
$ mkdir bliss ; cd bliss

# Init repo
$ repo init --depth=1 -u https://github.com/BlissRoms/platform_manifest.git -b q

# Clone my local repo
$ git clone https://github.com/TeGaX/android_manifest_samsung_j7y17lte.git -b BlissROM .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch bliss_j7y17lte-userdebug && make clean && blissify j7y17lte | tee log.txt
# List of env
-userdebug
-user
-eng
```

## Credits
2019 @Astrako
2020 @Tenshi2112

## Contact
Telegram support group: https://t.me/joinchat/D1Jk_VbieGBXOWZt2y8O7A
