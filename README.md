# MiuiCamera-Pissarro

1. Clone this repository to `device/xiaomi/miuicamera-pissarro`
2. Clone [this](https://github.com/samrth012/vendor_xiaomi_miuicamera-pissarro) repository to `vendor/xiaomi/miuicamera-pissarro`
3. Add the line below to `device.mk`
    ```makefile
    $(call inherit-product, device/xiaomi/miuicamera-pissarro/device.mk)
    ```
4. Include device policy in `BoardConfig.mk`
    ```makefile
    include device/xiaomi/miuicamera-pissarro/BoardConfig.mk
    ```
5. Also add overlay: Add MIUI camera to aux whitelist
   ```makefile
        <string-array name="config_cameraAuxPackageAllowList" translatable="false">
        <item>com.android.camera</item>
        </string-array>
    ```
