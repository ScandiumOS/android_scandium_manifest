# [COMING SOON] ScandiumOS | Open Source Software
android based on AOSP.

# Requirements:
- Around 500GB disk space.
- A computer with at least 16GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts).

### Create ScandiumOS Folder ###
```bash
mkdir ScandiumOS
cd ScandiumOS
```

### Sync our source ###
```bash
repo init -u https://github.com/ScandiumOS/android_scandium_manifest.git -b Holocaust_A13
```
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build our source ###
```bash
. build/envsetup.sh
lunch scandium_$devicecodename-userdebug
mka scandium -j$(nproc --all)
```

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

### Credits ###
 * [**AOSP**](https://android.googlesource.com)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**ArrowOS**](https://github.com/ArrowOS)
