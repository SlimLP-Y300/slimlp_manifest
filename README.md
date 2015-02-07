slimlp_manifest
================

Local Manifest to build SlimLP for the Huawei Y300

Build Instructions for SlimLP Y300 (U8833)
-----------------------------------------------------------------------------

1. Initialize repo using the SlimLP manifest (CAF branch)
    
        repo init -u git://github.com/SlimRoms/platform_manifest.git -b lp5.0-caf

2. Add my local manifest

        mkdir .repo/local_manifests
        Copy slimlp_huawei.xml to .repo/local_manifests

3. Then sync up the repositories
 
        repo sync

4. Initialize the build environment

        source build/envsetup.sh
    
5. Build the ROM

        For Y300:
            brunch u8833

NOTE:
   
   The JNI Generator [patch] included in android_device_huawei_msm7x27a-common is required for building the rom in my Arch Linux environment.
   For Ububtu based distros, this patch should not be needed to build the ROM so can be deleted.


[patch]:https://github.com/SlimLP-Y300/android_device_huawei_msm7x27a-common/blob/lp5.0/patches/external_chromium_org/0001-Fix-JNI-Generator.patch