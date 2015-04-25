slimlp_manifest
================

Local Manifest to build SlimLP for the Huawei Y300/G510/G330

Build Instructions
-----------------------------------------------------------------------------

1. Initialize repo using the SlimLP manifest (CAF branch)
    
        repo init -u git://github.com/SlimRoms/platform_manifest.git -b lp5.1

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
        For G510:
            brunch u8951
        For G330:
            brunch u8825

