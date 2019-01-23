## TWRP device tree for Xiaomi Mi Max and Xiaomi Mi Max (hydrogen/helium)

Add to `.repo/local_manifests/helium.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/xiaomi/helium" name="android_device_xiaomi_helium" remote="TeamWin" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_helium-eng
make -j8 recoveryimage
```

Kernel sources are available at: https://github.com/LineageOS/android_kernel_xiaomi_msm8956
