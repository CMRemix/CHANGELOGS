
project bootable/recovery/
commit 471eb4e140b36c9a6092c70bf4e286961b1378e3
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Thu Mar 26 14:11:04 2015 -0700

    update-binary: support reboot_now on older recoveries
    
    Attempt to reboot using older methods in case the recovery that we
    are updating does not support init reboots
    
    Change-Id: I9d6ec23c65291221e99d67b2361a2bd150319eee

commit 378071e3f641170caa5640b4ce828a49f32ab0ce
Author: Matt Mower <mowerm@gmail.com>
Date:   Wed Jun 4 13:03:58 2014 -0500

    bootloader: Silence /misc partition error
    
    LOGE has been changed to LOGI for "Cannot load volume /misc!"
    since many devices do not define a /misc partition in fstab.
    
    Change-Id: I53c440f820fd4614b0af79e9283baa8c48453373

project build/
commit c09c72abc208f90d63c046ad1c4957c891fb7fa8
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Wed Mar 25 18:14:46 2015 -0700

    releasetools: add compatibility for full ota functions with incrementals
    
    Some device-specific releasetool functions may expect that input_zip
    and input_version are set. For incremental OTAs, target_zip and
    target_version are set instead.
    
    Set input_zip=target_zip and input_version=target_version to add
    compatibility with these functions.
    
    Change-Id: I6a04f67440618d3652396656cc1fe223d4a6b195

commit 5a5d96a8161bbb867801f1029b626eea3ebffadb
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Thu Mar 26 16:32:34 2015 -0700

    ota_from_target_files: Fix path for SkipNextActionIfTargetExists
    
    Without the leading forward slash, the check always fails.
    
    Change-Id: I57320c20ca2b384713182082b1ad5321d78dbb2b

commit f45a44eea16ea41753422be631c7c944476339cb
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Fri Mar 27 20:53:59 2015 -0700

    ota: Include full boot images when imgdiff fails
    
    When generating a non-block based incremental, inclue the full boot
    image when imgdiff fails to generate a patch. This logic is already
    used for block based incrementals.
    
    Change-Id: Idae484ea8c2553a3480961dfa413724e61c52e5f

commit c2fd04bfca162672d23e9e11766f46eae6575a95
Author: Ricardo Cerqueira <ricardo@cyngn.com>
Date:   Sun Sep 28 01:55:24 2014 +0100

    Add support for mediatek platforms
    
    This includes optional support for building the kernel with mediatek's
    build system, which is usually included with OEM source drops for this
    platform. (enabled by BOARD_USES_MTK_KERNELBUILD:=true)
    
    Change-Id: I69fb50aa17d9c171bf8a7c220a0707c4bc570733

commit 7cc5e333a6410bb654da665e792ffe60ce1c4452
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Dec 12 23:06:47 2014 -0700

    cmRemiX Version

commit 1218a6b8b491fc9e65c4679d0996a67ed347257a
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 23:06:47 2014 -0700

    Introduce New Squisher/Opticharger for Lollipop (2/2)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    Change-Id: I02b41274179cdc1793794fb11780ea60774e6e41

commit c85fd3e280dcbd51b66569b13b913254e380acde
Author: root <xyyx@mail.ru>
Date:   Fri Dec 12 23:06:47 2014 -0700

    Do not use mkf2fsuserimg.sh if we have two fs in fstab, for example:
    
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          ext4    noatime,nosuid,nodev,barrier=1,data=ordered                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           ext4    noatime,nosuid,nodev,barrier=1,data=ordered,noauto_da_alloc     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt

commit 4ee3edce67460206a4e775945ed706362a85d25e
Author: Jiangyi <sam.andrew.jiang@gmail.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    build: Add chromium prebuilt support to envsetup.sh && The core Makefile
    
    This adds a chromium_prebuilt function to envsetup.sh that is invoked by lunch to check
    whether the chromium prebuilt are up-to-date or not. If not, it will be built from source
    and then the new source built version will be pulled during brunch/mka bacon to become the
    new prebuilts for future builds.
    
    This is all opt-in through the USE_PREBUILT_CHROMIUM flag. Without it being set to 1,
    none of this would be ran, and regular operations will go on.
    
    PS13:
    -use export TARGET_DEVICE
    -replace git -C with params compatible to old git versions

commit 565c46045344ba3b34de3ea8e0a787e611747d66
Author: Ayysir <ayysir@aospal.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    Prebuilt chromium: Run a check for target device directory
    
    This should fix the issue that arises if device fails
    and device is built again, chromium will error out because it thinks
    the prebuilt files exist (which they are not, directories are just created).
    
    Signed-off-by: Ayysir <ayysir@aospal.com>
    Change-Id: I595cab268e66c738ccae9900150b36d7f9626a6e

commit d32a92c0ea3835946889bd033b935221b169b3d4
Author: rooque <victor.rooque@gmail.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    build: Fix PreBuilt Chromium refs

commit d7c04b83b29a06fd0d552b46b08c4bed0e96a23f
Author: JoseGalRe <josegalre@gmail.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    build: change style console output of prebuilt chromium
    
    Change-Id: I2c390f3c64d614e181ebcad4e9711a93d9c55d44

commit b8e39833c9e600985b23da61fc8a931f5bbba7e8
Author: mar-v-in <github@rvin.mooo.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    JDK8: JDK check should succeed with OpenJDK 8
    
    Change-Id: I1c1eaff7fa36bba2db261e0c5311bbc6d005a726

commit 529a3a07af230e6c9458906c67eebbb33de3d668
Author: JoseGalRe <josegalre@gmail.com>
Date:   Thu Dec 25 16:21:52 2014 -0700

    build: Show more hardware information about the device [3/3]

commit 3d808b65ff4be37f3298f2be283e23b7198a133f
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Thu Dec 25 16:21:52 2014 -0700

    build: Do not remove recovery resources, so TWRP can build

commit 9e391e12ba3cf443ed1a5dbec5f9987d55e6ff53
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Remove recovery resources for cwm
    
    Revert this, https://github.com/PAC-man/android_build/commit/cab57f994fe0c7c53853411eaa3575aa6b3ef8d7
    
    Change-Id: Ica036525b768f6e416b103ba60bc26d58f2e02e2
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit ce0333742d66be63cea1afd826caecbf3e241ad5
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    core/config.mk: Add SED_INPLACE
    
    Change-Id: I5fdff25e5c1d4861b3a1f9e208c6d0fa5d415115

commit 2134898c57d785607ec5f8db9053c97966c5c412
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    core: Set ro.adb.secure=0 for recovery default.prop
    
    Change-Id: I71384795580ae6650bf543128798ee312f74e0a2

commit 9779af9047823f107ed0969f76329441d01b22af
Author: LorDClockaN <davor@losinj.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Add SuperSU to releasetools
    
    Thanks to chinfire's "How to SU" guide,
    I've managed to get SuperSU zip flashing on every
    rom flash and it can easily be updated in
    vendor
    
    Also Settings part merged in from OmniRom
    
    PS2: Don't unmount /system, it gets unmounted
         from within superu.zip flash script
    
    Change-Id: I0f57f8c2b8733021c3c0b9a5fd3c343ae565a959
    Signed-off-by: LorDClockaN <davor@losinj.com>

commit 16763776fa876074ca4f47234d017c30607afe5b
Author: William Casey SEdlacek <w@sedlaceks.org>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Block Building

commit 0e1c4709bc92932d3f97657c99f0e21806c237dc
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Add a Whole bunch of Clean Options

commit 040880051167c7627157f0719e50e17014750f0d
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Add Make Dirty Option
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 89bbd2055f8e667ef43021757ba1de06fa7a253e
Author: deadman96385 <seanhoyt963@gmail.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    Kill some log spam
    
    Thanks to @Cl3Kener for taking lots of his precious time to help me find these things that were driving me up the wall.  I should have authored this commit as him but I didn't.  Sorry buddy maybe next time....
    
    Change-Id: I8d6cd504afe83954964f71eb7d8f802624d2e595
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit f15efe3d365efd72a27562327b496e359bacfaa0
Author: MrBaNkS <banksmi09@gmail.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    build: remove all stops if using different make/openjdk-java version
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 44bf8a7bfc14c2456aae3c13493698d8fc74f323
Author: Evan Anderson <evan1124@gmail.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    ccache: Use system version over prebuilt
    
    If there is a ccache binary on the
    host system use it instead of the
    AOSP prebuilt.
    
    Change-Id: I4b1e030713be22167a12bd229a4e35eda7736cd2
    Signed-off-by: Evan Anderson <evan1124@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit a74224f270183552ee2c2f0db16d24168f97a417)
    
    (cherry picked from commit a74224f270183552ee2c2f0db16d24168f97a417)

commit a37b71e0fedf2f41f2ce1e5bc28004a8c9170c45
Author: Elliott Hughes <enh@google.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    Remove libdvm dex preopt support.
    
    libdvm is dead.
    
    Change-Id: Ib8571c007f8a9f0e0eaf5c61b5d2e416b2d95089
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit d875c8eab87552602c1df2d007b5a23ca12fdb69)
    
    (cherry picked from commit d875c8eab87552602c1df2d007b5a23ca12fdb69)

commit fea39bf892782b28987de94c535aff3fab127b6e
Author: Ian Rogers <irogers@google.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Move definition of -D__ARM_FEATURE_LPAE=1 cflag to top-level.
    
    LPAE indicates better instructions can be used when atomicity guarantees are
    needed. However, LPAE's presence isn't advertised by clang/GCC. We fake an
    ARM feature to advertise its presence on architectures where it is.
    Also, add a TODO documenting that cortex-a15 is not the correct CPU variant
    for krait.
    
    Change-Id: I02a1248025c32d94eca0bc8a249dc524f1ac9c36
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    (cherry picked from commit 42d9c498021f6ccaafb1108b289bf3e5e2160fdd)
    
    Conflicts:
    	core/combo/arch/arm/armv7-a-neon.mk

commit 3012452027edb364e585834c2153bbce1e42c948
Author: David 'Digit' Turner <digit@google.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Update host linux toolchain to gcc 4.8
    
    This patch ensures the build system uses the prebuilt gcc-4.8 toolchain
    when building host Linux binaries, instead of the gcc-4.6 one.
    
    Change-Id: I7b449650714ba4314a780827e0243f2af40ec82c
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3a371706b41edccc0e4a97e09920c1b663b17a1b)
    
    (cherry picked from commit 3a371706b41edccc0e4a97e09920c1b663b17a1b)

commit 77dd00389182a84de1d2d22fe213019837d495d1
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Add Toolchain Version to Lunch Menu
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b8d1f8e56a135943175384e9719e7bfb59733dbb)
    
    (cherry picked from commit b8d1f8e56a135943175384e9719e7bfb59733dbb)

commit 91fa651b80afa6e411cd83ede96c3d0ad0e56521
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Use New 4.8 Host Toolchain from Google
    
    * While we are fixing SM Host Toolchains let's use the latest Google.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3885177ff3cdcc3374944be6d9fe984e5d999291)
    
    (cherry picked from commit 3885177ff3cdcc3374944be6d9fe984e5d999291)

commit 88a69a5de9c3806faecbc2f2a2c516a3e6b54f6e
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Add graphite flags
    
    Change-Id: I90bd416e800936b2130b82246fe0fd047774d466
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit f604a52efdb79fca5506fcd3e9c4c80799bdbb33)
    
    (cherry picked from commit f604a52efdb79fca5506fcd3e9c4c80799bdbb33)

commit da284d694f9c99ca0d02f34a93440771682804d0
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Remove 2nd cpu nonsense
    
    * Not like I'll ever use it
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b5b4b58f4596c83e1f40b7d8a2e060c90f1dc7e3)
    
    (cherry picked from commit b5b4b58f4596c83e1f40b7d8a2e060c90f1dc7e3)

commit 04948e87f2d5500f487b510290ce645cfe42fa69
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 17:24:12 2015 -0700

    Build: Add Custom Toolchain Support
    
    (cherry picked from commit 75dab12fd829083afdf3e491e2955373fb9f7e99)
    
    (cherry picked from commit 61b7c1a0e72c1ea5e6d7d205edbfd5d0491f23fe)
    
    (cherry picked from commit 8be05df23458c5f336bce9f164045cfd8b7b7bba)
    
    (cherry picked from commit 62a2e408062591a72befd2f38fcedf283c136340)
    
    (cherry picked from commit 67786fe131ca8ea5c3a192879c4a64dd1259deae)
    
    (cherry picked from commit 0159f777a1ae7174ae32a2d9a5420a4b563e13c9)
    
    (cherry picked from commit de7c8cba8acd1b2ad25ebaca7ca817cd6653b300)
    
    (cherry picked from commit 5e3429c4f499b0ce89a97b8910ecf9508f68f417)
    
    (cherry picked from commit 5e3429c4f499b0ce89a97b8910ecf9508f68f417)

commit 4d8fa7718b0da56cd5404dbcac9a63d7e874beb3
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Dec 13 09:37:17 2014 -0500

    Cleanup armv7a neon
    
    * Why don't we have cortex-a9 option and why is the fix cortex a8 being applied to all?
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 6a513af74a4a3bb8f94ab9d8d1987b94fb7e86e0)
    
    (cherry picked from commit 6a513af74a4a3bb8f94ab9d8d1987b94fb7e86e0)

commit 133571904593258b2d2cc3015e4df3efd3d56aa1
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Mon Dec 15 23:08:47 2014 -0700

    Update modular:  add strict-aliasing and make flags default instead of using a string
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 8ced76a5bdd6cd38ce6845a8bf303986cfa4a9fd)
    
    (cherry picked from commit 8ced76a5bdd6cd38ce6845a8bf303986cfa4a9fd)

commit 28fa5c4682163a63375935db9f562a1e7415ff93
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Dec 24 09:44:17 2014 -0500

    Update Graphite and Strict Aliasing
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 15a343e2ef029a83ca8feebad9c5a42952a0621a)
    
    (cherry picked from commit 15a343e2ef029a83ca8feebad9c5a42952a0621a)

commit 92a4ec6ae0f8862e5d2f31ee93f625c82605c89e
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 24 12:59:31 2014 -0500

    Initial Disable Strict Option
    
    * Still will need lots of work.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit a1430dba729cd13e6e7a04d2b00c60d929979bd0)
    
    (cherry picked from commit a1430dba729cd13e6e7a04d2b00c60d929979bd0)

commit 1430f6ae94fb0bbd18d98b639fe4078f4e8e5a5e
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 24 16:45:55 2014 -0500

    Updates/Fixes for modular graphite/strict implementation
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 0d5703ef3aa4632ff8a638b42da053055b14f475)
    
    (cherry picked from commit 0d5703ef3aa4632ff8a638b42da053055b14f475)

commit 96e0796a8151b979671c2f7bfe77e6fcec100c6b
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 18:28:43 2014 -0500

    Use Universal True instead of Yes
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 64d3fe317204e1ba769c4ac39eda93ea613f0d58)
    
    (cherry picked from commit 64d3fe317204e1ba769c4ac39eda93ea613f0d58)

commit dcf227a76f8e1b849cc2834fe0d4f09a168e4eb9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 19:14:21 2014 -0500

    Introduce USE_HOST_4_8 Flag
    
    * This will enable Host 4.6 by default for devices that can't handle Host 4.8
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    True not yes
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 659f1389ba8500794324fd705fb2c8a7b8847533)
    
    (cherry picked from commit 659f1389ba8500794324fd705fb2c8a7b8847533)

commit e48c08165d6316b3eee43dc6426686318ec72ca0
Author: Anthony King <anthonydking@gmail.com>
Date:   Thu Nov 6 20:34:13 2014 +0000

    WIP: clang supports cortex-a15 now
    
    Change-Id: I9872db2237c513f135df32c5147e47edf6eba49f
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 442dbe42044641f457b45930230c342ce1728281)
    
    (cherry picked from commit 442dbe42044641f457b45930230c342ce1728281)

commit dff2016e080e5bca11e981075d9fc2f595493256
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 19:44:02 2014 -0500

    Update Strict.mk with more violations
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit f0f90132858e72ae4ffa2f24c9fade2748c85797)
    
    (cherry picked from commit f0f90132858e72ae4ffa2f24c9fade2748c85797)

commit 62e8f59f9f1a1f1ea4c53abf612ce15b26e323b7
Author: Jake Weinstein <xboxfanj@msn.com>
Date:   Mon Dec 22 13:01:03 2014 -0500

    build: clang: use swift and VFP4 flags for krait
    
    Change-Id: I4c22d6d7d8d2dcf5de26ba3061bba58c74eaf93c
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 860fcc499f91a9644cccfb3de7b3b37570bad379)
    
    (cherry picked from commit 860fcc499f91a9644cccfb3de7b3b37570bad379)

commit 46ea361327af08b74ab5aec2aad3d021fc8583c8
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Dec 27 02:20:48 2014 -0500

    TWRP Strict Aliasing Violations
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b1ec348c6d50c8652002cc896fccc02477313be7)
    
    (cherry picked from commit b1ec348c6d50c8652002cc896fccc02477313be7)

commit ae42b4d898c584e413d495dab6922d0e6334e365
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Dec 27 03:21:14 2014 -0700

    strict-aliasing: Fix warning levels for clang or not clang
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit ff049aa0fb7b40556ad48618eadd01663cbb76af)
    
    (cherry picked from commit ff049aa0fb7b40556ad48618eadd01663cbb76af)

commit 0d56443c74d69023c9d094835d8b8b45468ab151
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Dec 27 18:15:49 2014 -0700

    strict-aliasing:  update module list
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 00ba0c7d0e09258eb4026a58f90721d641a9c450)
    
    (cherry picked from commit 00ba0c7d0e09258eb4026a58f90721d641a9c450)

commit 4f968da6747f41204e0e21b4901a94b170b62c99
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Mon Dec 29 11:00:23 2014 -0500

    Initial Modular O3 Implementation
    
    * Due to the many number of local makefiles that somehow seem to sometimes override -O3 in Lollipop I'm using -O2 + individual -O3 flags instead of just -O3.  I noticed there was a larger size difference when doing this so it seems to work better from what I can tell.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    derp
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    ftree-loop-vectorize not recognized
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Guard O3 like Graphite
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    O3: Libziparchive is a hater
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Updated O3 List
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 25d8c51cf240b38ba87c5a7ef0f29b6fb7b61e67)
    
    (cherry picked from commit 25d8c51cf240b38ba87c5a7ef0f29b6fb7b61e67)

commit c8d7af715d409b920f40e51bc2d7d59c29a92c9a
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 16:46:13 2014 -0500

    Attempt to tune for Krait Modularly
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit ce30849f0c936fa9606062334bbc79eb627b4185)
    
    (cherry picked from commit ce30849f0c936fa9606062334bbc79eb627b4185)

commit c37a63eda5a0c98134bd6393981d7e439ede842f
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:39:14 2014 -0500

    Return some GCCONLY flags used in Kitkat
    
    * and keep them away from clang too!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3fe59b017364f110fdf226e02f1790fc2772d0ea)
    
    (cherry picked from commit 3fe59b017364f110fdf226e02f1790fc2772d0ea)

commit bce603bd6fcfd32d79ffec6e24d37034a8e307c9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:52:16 2014 -0500

    Keep Krait Tunings off the Host Modules
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 0e2c474b8d599ca911f6d8ce2f04ca3933bfa2fb)
    
    (cherry picked from commit 0e2c474b8d599ca911f6d8ce2f04ca3933bfa2fb)

commit 51095a5c493df594d700b0cac29562ef8977d436
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:55:05 2014 -0500

    -mvectorize-with-neon-quad not supported by clang
    
    * Will move to GCCONLY
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit dc4fcef6055be0b532b468c997c20c68044606e5)
    
    (cherry picked from commit dc4fcef6055be0b532b468c997c20c68044606e5)

commit 283cc0a1308adb1e552666b867ce00033bfaecd9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:56:23 2014 -0500

    GCCONLY: Add -mvectorize-with-neon-quad
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b72cdd79ea283f4f5accc296add6677277ef0031)
    
    (cherry picked from commit b72cdd79ea283f4f5accc296add6677277ef0031)

commit cee1e0bb65f3cbe6162609dc22cfbefdb58cc6d9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 01:43:49 2014 -0500

    Update the Krait Ignore List
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 72b10173b9b3810f8d039cafe2754e66b90eaf39)
    
    (cherry picked from commit 72b10173b9b3810f8d039cafe2754e66b90eaf39)

commit 0d5f8680f173e43a0da165555ee5991a57e90a44
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 08:34:23 2014 -0500

    Bluetooth: The Most poorly written code in Android
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit df207552867bbeae8f31618ec36738851d27f371)
    
    (cherry picked from commit df207552867bbeae8f31618ec36738851d27f371)

commit 82b393ff9736861486dad56d1ff857d6b9d0a01e
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 13:10:43 2014 -0500

    armv7-a-neon: Apply Correct mfpu and mfloat tunings per arch
    
    * Before everything was neon and soft float.  Now let's allow for per cortex tuning. Benchmarks should go up.  See here for better references https://github.com/CyanogenMod/android_build/commit/8907b775376211e73a566e8c9ef65e5b76cba1af
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit e63fba92b06f8833a4d57ef52c00dfa7ffcadc32)
    
    (cherry picked from commit e63fba92b06f8833a4d57ef52c00dfa7ffcadc32)

commit c290b2f3cbcc15f24bb11419e2f11f7bb5efa3c2
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 2 21:57:00 2015 -0500

    Remove webview related files from -O3 and GCC Only Optimizations
    
    This causes FCs on some applications.  I haven't experienced it but it makes no sense to really make these files larger anyways.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit a28f8e66579ec22528a578d1df844da2b489792e)
    
    (cherry picked from commit a28f8e66579ec22528a578d1df844da2b489792e)

commit ac5dd8cb91be52e4cd2bee135e7cfac0500b8f82
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 13:45:17 2014 -0500

    Clang doesn't support -mfpu=neon-vfpv4
    
    * Which is unfortunate.  I would be much better if I didn't have to hack this crap
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 6ee82e88fa5b7302d2b9984bc93168aca1749b90)
    
    (cherry picked from commit 6ee82e88fa5b7302d2b9984bc93168aca1749b90)

commit 6e90dd14769d6d7f0002780173316a8a2daf147f
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Jan 3 00:01:31 2015 -0500

    libwebviewchromium: Haters Gonna Hate
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 48eb1ecbb5d1d97c508eb7e285e375bbb8824fcb)
    
    (cherry picked from commit 48eb1ecbb5d1d97c508eb7e285e375bbb8824fcb)

commit d4472a6f055a54a2959090ac861f470111a90c5f
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Jan 14 18:45:00 2015 -0500

    Order Matters
    
    Put Graphite last since it will help optimize code size after -O3 and all of the other stuff.  Credits @pbeeler.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 29d6c5d482fc27c81d0184a93795d6706a97cf0f)
    
    (cherry picked from commit 29d6c5d482fc27c81d0184a93795d6706a97cf0f)

commit eacc223af3d40df20f6c12d797197f0c4be50fe6
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Jan 14 18:49:14 2015 -0500

    Update Copyright Year to 2015
    
    * New year!!!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 9e39753fd61c1d9f0d2a73186a8bb1d475425629)
    
    (cherry picked from commit 9e39753fd61c1d9f0d2a73186a8bb1d475425629)

commit cf75937d5f2e63ecf763bd4d145ff3581c7e5432
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 13:49:30 2015 -0500

    Missing Separator
    
    * Must have missed it in rebase... :/
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c42a61a5edd6d9adebb5ed25471c8ff50c33d954)
    
    (cherry picked from commit c42a61a5edd6d9adebb5ed25471c8ff50c33d954)

commit 455bf217f9f3b242e0809c7da0c347ae5ac0def9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 14:10:29 2015 -0500

    O3: Ignore Annoying warnings that crop up with -O3
    
    * These are warnings, not errors! Please don't stop my build!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c89528ad587b3eefddb1656623c4e1c95ca8167e)
    
    (cherry picked from commit c89528ad587b3eefddb1656623c4e1c95ca8167e)

commit 9557c1383075f29ecec8cfea58cd2f8da9323d63
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 20:23:13 2015 -0500

    Update graphite again
    
    Seems the order change in the binary file caused a two more graphite errors which we fix here
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 878e16fce0084d7a4239d8cbc1482d7f09a9b9dc)
    
    (cherry picked from commit 878e16fce0084d7a4239d8cbc1482d7f09a9b9dc)

commit 80c890f097c20b8a92abf91d16a7a0f6c4272edd
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 07:15:52 2015 -0500

    Introduce Modular TARGET_USE_PIPE
    
    * Allow for -pipe to be used. This flag actually has no effect on the generated code, but it makes the compilation process faster. It tells the compiler to use pipes instead of temporary files during the different stages of compilation, which uses more memory. On systems with low memory, GCC might get killed. In that case, do not use this flag.
    
    * From my personal experience, compilation time was ~5 minutes less using pipes on a "make -j8" build on my personal computer.  Times may improvement more when doing like a make -j16 or -j24 on a build server with lots of RAM. Also note that this may not speed things up on a SSD hard drive due to the faster write speeds, I only tested this on a regular hard drive.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c5e99ee9ca8edcfa0055c66cb5f3a22c8220fe4c)
    
    (cherry picked from commit c5e99ee9ca8edcfa0055c66cb5f3a22c8220fe4c)

commit e7bc4bcbc165a65f86a5c374f2d263ff1982343a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 17:40:33 2015 -0700

    Shrink the codes

commit e66bb9356b797d4954c9a8f9304ec6b733a25249
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Dec 14 23:09:53 2014 -0500

    Show Custom Toolchain being used
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Full Path is Too Long
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Make these the same
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Hardcode this to 4.8
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit dedf9915f301bd5b422a3ffe59db1efbdddd968a)
    
    (cherry picked from commit dedf9915f301bd5b422a3ffe59db1efbdddd968a)

commit 79b4bbe06667a22c10120b5da471c8bf33db3a7d
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 18:22:07 2015 -0700

    build: show info of all Optimization features being used

commit 587825c2adc9f7d2057de99eea5b425f2a74d330
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 18:47:52 2015 -0700

    dumpvar: fixed sabermod kernel version

commit 8f0abb8abf36c45db0111ecafb9ee1a2439643df
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 19:19:34 2015 -0700

    strict : disabled more module for cmRemiX Rom

commit 03657e7f69ce46c7d48d464fffa69ba6fa7030d0
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 20:08:40 2015 -0700

    graphite: one more module for new SM 1-14-2015

commit 6683c933b4dcd81fe19c141194272e17230bbe44
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 20:17:17 2015 -0700

    Introduce Modular Link Time Optimization
    This is the codes from @MWisbest, Get the idea to
    for modular from Chet Kener & Pbeeler

commit 128b2c62234c0858951e80d3b9a94b80c478882a
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Mon Jan 19 11:50:28 2015 -0500

    Introduce FLOOP_NEST_OPTIMIZE
    
    For more info with regards to how this works see http://en.wikipedia.org/wiki/Loop_nest_optimization
    
    It's highly aggressive so you'll notice I had to disable several dozen modules.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 411b03fd963dcbdb4cfeb7922c59011e99592db2
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Jan 19 12:01:40 2015 -0700

    dumpvar: add FLOOP_NEST_OPTIMIZE info

commit 761533a78d62d586ccc20d7655e329cc2f8765d2
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Fri Jan 23 14:11:11 2015 -0500

    Do not remove recovery resources for twrp
    
    Change-Id: I7f36cd0f43e4244e65630c915072747efda8efe1
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    
    (cherry picked from commit ebed41c60d1496d0bf961601bc33ee02b2f8e816)
    
    (cherry picked from commit ebed41c60d1496d0bf961601bc33ee02b2f8e816)
    
    (cherry picked from commit 4e86588887474f641f296cf9ed18160efb3ce879)
    
    (cherry picked from commit 4e86588887474f641f296cf9ed18160efb3ce879)
    
    (cherry picked from commit e72abe13cdc34eaa7f81b57f77b102d6876e53d1)
    
    (cherry picked from commit e72abe13cdc34eaa7f81b57f77b102d6876e53d1)

commit f02cc95e039c63841855b5cc183641969c4b1af8
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Jan 24 01:40:34 2015 -0700

    various fixed and update

commit 636d1cabdc9a50599ba4f1209bae7edf9a74e123
Author: johnnyslt <ionut.darescu@gmail.com>
Date:   Sat Jan 24 20:53:54 2015 -0700

    Add changelog generator (2/2)
    
    How to use :
    
    two methods
    
    1.- export CMREMIX_CHANGELOG=true
    
    2.- add flag CMREMIX_CHANGELOG=true in BoardConfig.mk or BoardConfigCommon.mk
    
    Ported by @cristianomatos and verified by @alviteri
    
    (cherry picked from commit 1785e3196939a468b61431bc4c67b31673bef30b)

commit d88f7f7daef9a4cf1105fc011ddb75c335b7bc10
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:16:00 2015 -0700

    SM Modular:  Fix wrong indef's
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	core/O3.mk
    	core/gcconly.mk
    
    (cherry picked from commit bf8d4a3fd2df31f6d795c1a11896ed5ab1eec385)
    
    Conflicts:
    	core/O3.mk
    	core/strict.mk

commit d5cb54233c360367ea9b5160c87f8c298b3f1516
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:17:28 2015 -0700

    Move flags and disable modules lists out of build (1/2)
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    (cherry picked from commit 6f45ca92e1fa15e39eee76a1c35aa7e6863c4fb7)
    
    Conflicts:
    	core/O3.mk
    	core/graphite.mk

commit 6460e23980730911371f5e18b19b9cac0ab815cf
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:17:28 2015 -0700

    Have -O3 skip when thumb is used to reduce code size. (1/2)
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 3617505a97f07888ed3698b1880d7b8854669169)
    
    (cherry picked from commit 3617505a97f07888ed3698b1880d7b8854669169)

commit e9348cfecec8ae1d229f93e5748ab5d883707811
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:20:06 2015 -0700

    arm neon:  Pass arch variant cflags to the kernel.
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    (cherry picked from commit 05a3f4d9446a759f21f482f4bb101eda0f18bf95)
    
    Conflicts:
    	core/combo/arch/arm/armv7-a-neon.mk

commit 0b4b80c2c852e1702334e7a13f0acb53ee9e51e4
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:20:06 2015 -0700

    O3: Only filter arm: Only arm uses thumb.
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit f12f0fb482656e892add0b03e1d5248dcbf4db34)
    
    (cherry picked from commit f12f0fb482656e892add0b03e1d5248dcbf4db34)

commit 642960a07826f25aa62ea47f23c9806178d321e2
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 25 18:03:25 2015 -0700

    Move Strict flags and disable modules lists out of build (1/2)

commit d76d36c958d7b12f88cd9baea724b4e8b54f0aee
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 25 22:59:14 2015 -0700

    add and removed various optimzization settings

commit e81807ebc2d4c3eccf4e02b6f7b9034a33253e77
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Jan 26 22:52:13 2015 -0700

    kernel: Add custom toolchain for kernel build again after rebase
    
    example: TARGET_GCC_VERSION_ARM := 4.9

commit c2f4bcfa5ad29238f0669c146dfbfd6a681de859
Author: SferaDev <sferadev@gmail.com>
Date:   Mon Jan 26 22:52:13 2015 -0700

    Don't stop if JDK version doesn't match
    
    Change-Id: I5e77c70724c7d81544673715ed09e0a53ce32730
    
    (cherry picked from commit 1cbdadbfeae0321b1cd9859cd2ed2572b5fdc39b)

commit 920df55c903f5d9b14850def31a1037377e3d5aa
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    build: change O3 OPTIMIZATIONS

commit 15dec3d74629e6ca226e9c3e579b2407dd71c390
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    Fix annoying issue with clang not understanding -mfpu=neon-vfpv4
    
    Credits to @Cl3Kener
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 5b4267469a9d4c2e183c07157928b4bcf203a72a)
    
    (cherry picked from commit 5b4267469a9d4c2e183c07157928b4bcf203a72a)
    
    (cherry picked from commit 235ff9aa3b0302d04aab3e4d52248e91e21a16a3)
    
    (cherry picked from commit 235ff9aa3b0302d04aab3e4d52248e91e21a16a3)

commit 18c632ef9b9fa46c05cc5a9aa6e9d231e8bb4d6c
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    arm neon: Strip TARGET_CPU_VARIANT then export it to the kernel.
    
    Also make -mfpu=neon-vfpv4 for all cortex-a15 types.
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    (cherry picked from commit b58ccc5c3dfb6ef36d6aecd9ca353298896e3c5e)
    
    Conflicts:
    	core/combo/arch/arm/armv7-a-neon.mk
    
    (cherry picked from commit 6cda883f582099fca3f155f46a8e2d885c4252fc)
    
    (cherry picked from commit 6cda883f582099fca3f155f46a8e2d885c4252fc)

commit 1bf3059bc3a18e111d0ab608c096edaf5a6ac585
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    arm neon: denver:
    
    use -march=armv8-a instead of -mcpu=cortex-a15
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 01ca9fac721f54ab5634ac643c817c18103e19b8)
    
    (cherry picked from commit 01ca9fac721f54ab5634ac643c817c18103e19b8)
    
    (cherry picked from commit 67af787a69fb429704f3fca6cc0f8e41f4cfb933)
    
    (cherry picked from commit 67af787a69fb429704f3fca6cc0f8e41f4cfb933)

commit 2d14896f6912d6b878485ae23f2f1115f17de462
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 03:06:04 2015 -0700

    arm neon: unbreak
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Unbreak #2
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit ce439710eddfd2c5130f117380afd3d4a5aa93de)
    
    (cherry picked from commit ce439710eddfd2c5130f117380afd3d4a5aa93de)

commit 33668646636fe891702ea62f85eb3ee4747ca495
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Jan 28 00:12:50 2015 -0700

    build: instroduce GNU11 Modular (Pbeeler) and fixed LTO

commit 60316394782ea618f6a0779dc55d2987f92bd4b7
Author: David Viteri <davidteri91@gmail.com>
Date:   Wed Feb 4 22:37:39 2015 -0700

    Build: Changelog (3/3)
    
    Thanks David (crDroid Andrroid)
    Conflicts:
    	core/Makefile

commit a19566c3134fbf0b6954acc8e4f23f295158c8ac
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Wed Feb 4 22:37:39 2015 -0700

    Remove the recovery resources
    
    Twrp updated their resources to /twres
    
    Change-Id: I8910f5a2aab8b9d1da626bedca6dbe2d729e28aa
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    
    (cherry picked from commit 21c931146143494fcc327eddfd8f01fedff4311e)
    
    (cherry picked from commit 21c931146143494fcc327eddfd8f01fedff4311e)
    
    (cherry picked from commit 446e899cc9ad294315eab12872113c0cfa32af94)
    
    (cherry picked from commit 446e899cc9ad294315eab12872113c0cfa32af94)
    
    (cherry picked from commit dc64cd4879e71594556ea2f431719ed6add61340)
    
    (cherry picked from commit dc64cd4879e71594556ea2f431719ed6add61340)
    
    (cherry picked from commit 5cf706a7c997db558d98d85660ea1f4a284a3ef5)
    
    (cherry picked from commit 5cf706a7c997db558d98d85660ea1f4a284a3ef5)

commit c9788cb74455b74adb8e208b762e92bbedd1d93e
Author: nemith <bennetb@gmail.com>
Date:   Wed Feb 4 22:37:39 2015 -0700

    Fix up the recovery.fstab for adv recovery
    
    Add options to allow for more complex recovery.fstabs with
    multiple fstypes.
    
    Change-Id: Id4b25c4a81d972b6670cd7ea05b3b8b83d6f18a9
    
    (cherry picked from commit d754a51908ec544417d7d8cdfd52609d29a13712)
    
    (cherry picked from commit d754a51908ec544417d7d8cdfd52609d29a13712)
    
    (cherry picked from commit 005d20427d6ab81b4a48823db916dbf32d8a4fe9)
    
    (cherry picked from commit 005d20427d6ab81b4a48823db916dbf32d8a4fe9)
    
    (cherry picked from commit c862701be9b7b43845e0e05faa35e6c03ed65f01)
    
    (cherry picked from commit c862701be9b7b43845e0e05faa35e6c03ed65f01)
    
    (cherry picked from commit 85658d34c95324241476c428b3e1c017f6609a7e)
    
    (cherry picked from commit 85658d34c95324241476c428b3e1c017f6609a7e)

commit c834311487e29bd85cb0c5b7a704f7fc6285dcf0
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Feb 4 23:06:14 2015 -0500

    gcconly: Change -floop-nest-optimize to enable by module
    
    * This optimization is super aggressive and causes play store crashes.  I want to focus on the most important modules first (bionic/art) and see if I can at least get those without breaking anything (like the Play store crashes we were experiencing before)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 85976f03db36776c2a591d8bb54cf3fdfa45db29)
    
    (cherry picked from commit 85976f03db36776c2a591d8bb54cf3fdfa45db29)
    
    (cherry picked from commit 2223c25aba286615b130a297836491061334808f)
    
    (cherry picked from commit 2223c25aba286615b130a297836491061334808f)

commit 8c4ecb5686ff6d7575806b21f3e23f1af68ec2a7
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Feb 4 23:19:45 2015 -0500

    List Art Modules in nest optimization
    
    * Let's try art first
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 29a1852c15d96d58ff52a25ad673523d5fd58e25)
    
    (cherry picked from commit 29a1852c15d96d58ff52a25ad673523d5fd58e25)
    
    (cherry picked from commit e66e53b1b7ee0411174677bedcb1ef50f019f738)
    
    (cherry picked from commit e66e53b1b7ee0411174677bedcb1ef50f019f738)

commit bd26be56d95fc31e17d6adb5c6f390aa0f49c3de
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Feb 5 00:53:13 2015 -0500

    Add Bionic to Nest Optimization List
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 9b44f2bed6782c82ff4979c629e146602cd17876)
    
    (cherry picked from commit 9b44f2bed6782c82ff4979c629e146602cd17876)
    
    (cherry picked from commit 5b46ee4212fdfb4a870f57b5aa89090b8bb3eb18)
    
    (cherry picked from commit 5b46ee4212fdfb4a870f57b5aa89090b8bb3eb18)

commit cf59768fa67c2d68669adecd92af11e9604999e9
Author: arter97 <qkrwngud825@gmail.com>
Date:   Fri Feb 6 19:30:35 2015 -0700

    arm: add support for BoardConfig to append CFLAG
    Defining BOARD_GLOBAL_CFLAGS from BoardConfig will add a global CFLAG to be used with the entire ROM compilation
    
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit f5ef3847eba897f555425962a7115864a06de8a7
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Feb 7 20:52:54 2015 -0700

    no need this settings

commit 7ad6d6acdcd20a916b31d56a6b007f84dc21d302
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 12 21:01:29 2015 -0700

    Revert: Do not use mkf2fsuserimg.sh if we have two fs in fstab, for example:
    
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          ext4    noatime,nosuid,nodev,barrier=1,data=ordered                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           ext4    noatime,nosuid,nodev,barrier=1,data=ordered,noauto_da_alloc     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt (reverted from commit 232b0c465eb098e47bdf16bc48fd9cb7a570bb6d)

commit 735b4597d38080f06ab113c965acc572c8454b0e
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Fri Feb 20 13:13:37 2015 -0800

    Revert "build: Handle custom boot images properly"
    
    We don't want to force this since we need to be able to
    re-sign boot images with proper keys, which requires rebuilding
    of the images.
    
    This also has an error in it from merging (dropped _MK).
    
    This reverts commit 22913dea82299eac7e1a5e754102b89af4796a0d.
    
    Change-Id: Id1353e9883c3f24bbc10e685f43bede779430025

commit 0d67b2471640468142e68e1c80cb2ab0d44a7197
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Mon Feb 23 00:38:24 2015 +0000

    Revert "Revert "build: Handle custom boot images properly""
    
    This is still needed, per this discussion here:
    http://review.cyanogenmod.org/#/c/76919/
    
    This reverts commit 78d216bc157021e111a31a6606622cef4b9d383d.
    
    Change-Id: If494c2c6468185bc0e10cdb92847a9f8429b79c4

commit 065db7d74248634a57417b793ff762849299b386
Author: Josue Rivera <prbassplayer@gmail.com>
Date:   Mon Feb 23 00:40:20 2015 -0700

    Add ro.cmremix.device for OTA porpuses
    
      * Due to unified builds disabling some id props, Slim OTA wasn't working
         working properly. Lets add a new prop just for our needs
    
    oldChange-Id: Ic2b3acb3dd4944160449f228cb69ec2c9f08775c
    Signed-off-by: Josue Rivera <prbassplayer@gmail.com>
    
    Conflicts:
    	tools/buildinfo.sh
    
    Change-Id: I745e0aa9e58040dc672815b2bf591ca17a65b21c

commit dd69f7f499d98c9d97990a1768b3bda2d8ec4cd5
Author: kantjer <kantjer@gmail.com>
Date:   Mon Feb 23 00:43:04 2015 -0700

    Add ro.cmremix.model for OTA purposes
    
    Change-Id: I5d4baf0548e098d629e900580758a6d582d3cc2b
    
    Conflicts:
    	tools/buildinfo.sh

commit c3aef1047fead554b0080bf9a7da498558bbde5b
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Sat Dec 6 12:44:40 2014 +0100

    updater-script: Format system before installing ROM
    
    Change-Id: Ib266d6c1bde64a028a4d06bca40c5c1a1431edd0

commit 42b3f88be1c79f51414c565715f2b6d605afaabe
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Feb 25 01:55:59 2015 -0700

    arm: compile all thumb with -mthumb-interwork and cleanup -O3
    
    To enable this option use ENABLE_ARM_THUMB_INTERWORK := true
    
    This may slightly increase binary size but will include more arm
    instructions for increased performance.
    
    https://gcc.gnu.org/onlinedocs/gcc/ARM-Options.html
    
    Change-Id: I0ba0a2d34b84e34309c20ce0cbb85ea3ee6dda15
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	core/binary.mk

commit e4fbc9c9281ae2af1d8b0d7d7bc1092ad4413d09
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Feb 25 02:00:33 2015 -0700

    Add Global posix thread aka pthread Support (1/2)
    
    this flag enables multithread support much like what I did in kitkat.
    
    https://github.com/SaberMod/android_build-OLD/commit/93d376380dffae1ec96eeb0ef00a7e663d107ca4
    
    Change-Id: Id5559ec460b2ba84ed9cfe7a47b0ac59544e1d61
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 3f7f927f90906c0f82c806fb36e5f910da998193
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Feb 25 02:16:32 2015 -0700

    build: add pthread to dumvar build info

commit 3d29745462fe4a892807b56d566a7e3e1eff61af
Author: fattire <f4ttire@gmail.com>
Date:   Mon Feb 16 01:19:08 2015 -0500

    repopick: Always expand paths to the repo executable.
    
    Change-Id: I4e89a530f98e3a28973c57adaf9046e9c21f1290

commit 90d935003a9f50a8b91040e1cc0a86040aa8c9cb
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 11:22:32 2015 -0500

    Mock Location should be off!
    
    * Unless you don't want people to know your exact location.  Users can try it then if they like
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit e7821da2b75384a0e85c5c7fe36e04ffd453d7fe
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:32:21 2015 -0500

    Do Not Odex Eng Builds
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 2c8bcce813cf5b29a767631b4bb565afec7263a2
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:40:46 2015 -0500

    Do not build test stuff for eng builds
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 2a846903f9747ca3760bc90afff0f882f9021c15
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:42:26 2015 -0500

    Remove Debug from Eng
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 377b0704532d353ca9211fcce29bc9bde96cc484
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 11:16:04 2015 -0500

    Remove ro.kernel.android.checkjni
    
    * JNI, the Java Native Interface, provides a way for code written in the Java programming language interact with native (C/C++) code. The extended JNI checks will cause the system to run more slowly, but they can spot a variety of nasty bugs before they have a chance to cause problems.
    
    * Forget the bugs I don't ever want to see OptiPop run slowly
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 50b4fbc1c8cdb7ed875648f3be7a8b16aa684282
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 12:34:14 2015 -0500

    Eng: Include in user build filter
    
    * Let's make eng builds similar to user builds.  (but with some of the eng build perks as well)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit ca0ecb09dbae709b7ecd275ccf273b3c731cfaad
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Feb 26 11:27:41 2015 -0700

    armv7-a: More Specific Tunings per CPU
    
    * Also add some substitutions and ignores for clang.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Conflicts:
    	core/clang/arm.mk
    	core/combo/arch/arm/armv7-a-neon.mk

commit 1319b7996d5227fde4b2e781e4c0b64f0d20dc50
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Nov 16 17:52:59 2014 -0500

    Do Not Build Recovery Or Use it
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit bd653fcf365e3341eb0346d7ec90c9ab865eb2e3
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Nov 12 22:34:31 2014 -0500

    Lollipop Audio Only
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Hangover Derp
    
    * You should try it sometime
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit fef383d42cba64e69012fe4ccf3d1970bac95ee6
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 23:07:28 2014 -0500

    Remove Annoying Goldfish Stuff
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 4c2562cd5975e4bc0a925315be8c3a9e804f35f9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:34:10 2014 -0500

    Build Stk and CellBroadcastReceiver
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit aebdb9848b925b9529399d38612329df6f991849
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:33:02 2014 -0500

    Build Launcher3 instead of 2
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit ffd52fb27b509c8046ee0d3072cfaad5c66c87c3
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:27:57 2014 -0500

    Allow Prebuilt APKs
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 9db83697ccda4d710f90583e99c8a81f8729efb9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:25:00 2014 -0500

    Do Not Build QuickSearchBox
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 3bb476aa6491907dbccf3e6e403c26a49429d582
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:28:48 2014 -0500

    Unsecure
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 1ced1a068dda9cb786df288d2d9dacfd3799bf11
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Nov 6 07:45:15 2014 -0500

    Remove Default Combos
    
    * I never use these
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 260f9c229a7f95593772a050858d72b596043b63
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Mon Nov 17 14:15:02 2014 -0500

    Add F2FS Compatibility
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Add Missing Unmount
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Remove Duplicate
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Try 3 Options for Mount
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Move Format Script to Bin
    
    * If backup script can be there so can this.  Besides there is no extras folder here anyways
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Update this command for Lollipop
    
    * The previous command worked fine in Kitkat but this command is now what was needed to get the job done
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 6f6819b1fa315adf2333f8e95a541bd68e060218
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:46:02 2014 -0500

    Makefile: OTA File by Date
    
    * This will keep things from getting confusing
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 7fafd792157e060957ce94c0a2c32498fe8a28b1
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:50:24 2014 -0500

    Remove MOAR Bloat
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 790a371eb33ff4cb552d5af69f0e5c3731b72ba7
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 26 11:44:11 2015 -0700

    Kill Bloat with Fire!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 374f1d839675aef4292d0150cab178999b58ea14
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Feb 26 20:48:11 2015 -0700

    Build: cmRemiX up sounds and update (2/2)
    
    Base on Build: slim up sounds and update (2/2)
    reference on sdk and full base builds to slims make file.
    As well remove both copy command in sdk build. This is handled already on slims
    make file.
    
    Change-Id: I9b0146df1a43cfc5282288012fc59509e0badedf

commit e093dfe66a6f44a9c071aa9fc3cb73d311e16d06
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Feb 28 02:00:33 2015 -0700

    build slim launcher again for more testing

commit a3fe33ffcc8c1a80a8c0ea1f9ab2e459b1cb97c3
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Feb 27 20:34:55 2015 -0700

    Qcom Clang v3.5 Optimization (MusterMaxMueller)
    
    -clean up code:
        -moved "COMPILER_RT_CONFIG_EXTRA_STATIC_LIBRARIES"
        -some refactoring
    
    -fix
        -"my_ndk_stl_cppflags" is now used correctly
        -use "llvm-as" and "llvm-link" executable from qCLANG
        -inject "-marm" or "-mthumb" according to "LOCAL_ARM_MODE"
    
    -workarounds to compile compiler_rt and libc++ with qCLANG:
        -compiler-rt doesnt like hwdiv with thumb. its set by default with mcpu=krait2. so force to use only for arm.
         see http://infocenter.arm.com/help/topic/com.arm.doc.dui0473c/DUI0473C_using_the_arm_assembler.pdf (p. 7-10 Table 7-3 Predefined macro) and qCLANG documentation (p. 45)
         maybe somone can helpout and explain why this must be forced?
        -libc++abi doesnt like the integrated assembler. so dont use it. https://android-review.googlesource.com/#/c/110170/
    
    -add workaround for "CONLYFLAGS"
    
    -play it safe and set "-fno-signed-zeros -fno-trapping-math -fassociative-math -freciprocal-math" although "-funsafe-math-optimizations" should be enough.
     did some testing and performance decreased if flags werent set. but maybe i messed up when i tested.
    
    -more optimization:
        -if "-arm-expand-memcpy-runtime" is not set then "-mllvm -arm-opt-memcpy" wont be used. so it wasnt used in the previous commit. now it should
        -dirty workaround to set "-mllvm -aggressive-jt". maybe someone has a clean and simple solution?
        -prepare to force using qCLANG for selected MODULES
        -minimal preparation for LTO
    
    seems to work good so far. also compiled bionic, art and jpeg with qCLANG.
    art seems to decrease performance. i will manually set/change flags for art and test again.
    
    TODO:
      -Make more performance comparisons to aCLANG. it seems good even compared to GCC
      -Use ccache
      -Where does it make sense to use qCLANG instead of GCC?
      -Compile Android with qCLANG wherever possible. http://www.linuxplumbersconf.org/2013/ocw/system/presentations/1131/original/LP2013-Android-clang.pdf and https://events.linuxfoundation.org/sites/events/$
      -Test -falign-os only when -Os is set
      -Test -falign-functions -falign-labels when -Ofast is set
      -Test -fdata-sections -finline-functions
      -"-fparallel" where to use? see 3.6.4
      -"-ffp-contract=fast" maybe to dangerous
    -clean up code:
        -moved "COMPILER_RT_CONFIG_EXTRA_STATIC_LIBRARIES"
        -some refactoring
    
    -fix
        -"my_ndk_stl_cppflags" is now used correctly
        -use "llvm-as" and "llvm-link" executable from qCLANG
        -inject "-marm" or "-mthumb" according to "LOCAL_ARM_MODE"
    
    -workarounds to compile compiler_rt and libc++ with qCLANG:
        -compiler-rt doesnt like hwdiv with thumb. its set by default with mcpu=krait2. so force to use only for arm.
         see http://infocenter.arm.com/help/topic/com.arm.doc.dui0473c/DUI0473C_using_the_arm_assembler.pdf (p. 7-10 Table 7-3 Predefined macro) and qCLANG documentation (p. 45)
         maybe somone can helpout and explain why this must be forced?
        -libc++abi doesnt like the integrated assembler. so dont use it. https://android-review.googlesource.com/#/c/110170/
    
    -add workaround for "CONLYFLAGS"
    
    -play it safe and set "-fno-signed-zeros -fno-trapping-math -fassociative-math -freciprocal-math" although "-funsafe-math-optimizations" should be enough.
     did some testing and performance decreased if flags werent set. but maybe i messed up when i tested.
    
    -more optimization:
        -if "-arm-expand-memcpy-runtime" is not set then "-mllvm -arm-opt-memcpy" wont be used. so it wasnt used in the previous commit. now it should
        -dirty workaround to set "-mllvm -aggressive-jt". maybe someone has a clean and simple solution?
        -prepare to force using qCLANG for selected MODULES
        -minimal preparation for LTO
    
    seems to work good so far. also compiled bionic, art and jpeg with qCLANG.
    art seems to decrease performance. i will manually set/change flags for art and test again.
    
    TODO:
      -Make more performance comparisons to aCLANG. it seems good even compared to GCC
      -Use ccache
      -Where does it make sense to use qCLANG instead of GCC?
      -Compile Android with qCLANG wherever possible. http://www.linuxplumbersconf.org/2013/ocw/system/presentations/1131/original/LP2013-Android-clang.pdf and https://events.linuxfoundation.org/sites/events/$
      -Test -falign-os only when -Os is set
      -Test -falign-functions -falign-labels when -Ofast is set
      -Test -fdata-sections -finline-functions
      -"-fparallel" where to use? see 3.6.4
      -"-ffp-contract=fast" maybe to dangerous
    Use Qualcomm Snapdragon LLVM Compiler 3.5 (https://developer.qualcomm.com/mobile-development/increase-app-performance/snapdragon-llvm-compiler-android) for Android Lollipop 5.0.2 for devices with Qualcomm CPU
    
    As far as I know nobody has done that yet. Except me :)
    
    This commit changes the toolchain for CLANG from the default one which comes with Android (aCLANG) to the Qualcomm Snapdragon LLVM Compiler 3.5 (qCLANG) mentioned above.
    The toolchain will be used for almost all places where the default Android CLANG (aCLANG) is used for compiling TARGET modules.
    BUT ONLY if "USE_CLANG_QCOM := true" is set. Otherwise it is using aCLANG.
    So you can merge this commit and the build will be the same as before except you specifically define "USE_CLANG_QCOM := true".
    
    WARNING:
    THIS IS NOT TESTED FOR STABILITY YET.
    READ CAREFULLY
    It is very likely that using this toolchain, especially with the optimizations flags, will introduce BUGS!
    
    I would suggest:
    IF YOU USE IT DONT MAKE BUG REPORTS FOR YOUR OFFICIAL ROM OR KERNEL OR ANY APPS.
    Make reports in the development thread. See below.
    The ROM compiles, boots and starts. Also if Bionic is compiled with Qualcomm Snapdragon LLVM Compiler 3.5 (qCLANG).
    Androbench, Antutu, Basemark 2.0 , Geekbench 3, Vellamo are 'completing' the bechmarks. That only means they didnt crash after a few tries.
    This is a work in progress.
    Only tried this on my personal device (Sony Xperia Z Ultra [C6833] with Krait 400) with Validus ROM (https://plus.google.com/communities/109330559573276360638).
    And this kernel: https://github.com/Tommy-Geenexus/android_kernel_sony_msm8974/
    If you use Validus ROM for Sony Xperia Z line you have to change the androideabi toolchain manually to the default one from google. Otherwise the device wont boot. (18.02.2015)
    
    At the moment this is only tested with Krait 400/Snapdragon 800 but in theory should also work with Scorpion.
    According to Documentation there is also support for armv8/aarch64 :) But support is not implemented in this commit.
    
    Install instructions:
    
      1. You have to make an account in order to download the toolchain!
      2. You need to download the toolchain  and extract it to {your android dir}/prebuilts/clang/linux-x86/host/*
      3. Add the repo (https://github.com/mustermaxmueller/clanglibs) to your manifest and copy it to {your android dir}/vendor/clanglibs/  For example: <project path="vendor/clanglibs" name="mustermaxmueller/clanglibs" remote="github" revision="master"/>
      5. Add "USE_CLANG_QCOM := true" to your Boardconfig.mk/BoardconfigCommon.mk of your device.
      6. Add "-marm" to "$(combo_2nd_arch_prefix)TARGET_arm_CFLAGS" in {your android dir}/build/core/combo/TARGET_linux-arm.mk because Qualcomm CLANG defaults to thumb. See Documentation!
      7. make a clean compile! Also delete ccache!
      8. give feedback
    
    I could have made the installation easier by uploading the toolchain to Github but I do not know if I am allowed to. And I am no lawyer so...
    
    Annotation:
      1. You should only get measurable performance benefits if you compile Bionic with CLANG! See here: https://github.com/mustermaxmueller/android_bionic/commit/7e6ab8ff68eca94c00c098d81005929de3d86e2c
      2. Documentation for the toolchain: {your android dir}/prebuilts/clang/linux-x86/host/llvm-Snapdragon_LLVM_for_Android_3.5/Snapdragon_LLVM_ARM_35_User_Guide.pdf
      3. The Flag "-muse-optlibc" is not Documented. It forces the compiler to use "libclang_rt.optlibc-krait2.a"
      4. The implementation is not beautiful but it works :)
      5. Wont compile if not aCLANG is used for the following modules: libcompiler_rt libc++ libc++abi
      6. "frameworks/rs/driver/runtime/build_bc_lib_internal.mk" still uses aCLANG. There might be some other places I missed.
      7. Host is compiled with aCLANG because qCLANG does not understand x86
    
    TODO:
      -make compiler-rt, libc++ and libc++ compile with qCLANG (I guess this will improve performance alot)
      -Test for stability
      -Make performance comparison to aCLANG *Ooops*
      -Use ccache
      -Where does it make sense to use qCLANG instead of GCC?
      -Compile Android with qCLANG wherever possible. http://www.linuxplumbersconf.org/2013/ocw/system/presentations/1131/original/LP2013-Android-clang.pdf and https://events.linuxfoundation.org/sites/events/files/slides/2014-ABS-LLVMLinux.pdf
      -Test -falign-os only when -Os is set
      -Test -falign-functions -falign-labels -falign-loops only when -Ofast is set
      -Test -fdata-sections -finline-functions
    
    Development Thread:
    http://forum.xda-developers.com/android/software-hacking/wip-compile-android-5-0-2-qualcomm-llvm-t3035162

commit 253c8e3a037188f5bd2045e20665c3a2ef6b781e
Author: JoseGalRe <josegalre@gmail.com>
Date:   Tue Mar 3 14:36:10 2015 -0700

    build: optimizations for devices with low-RAM [1/2]
    
    Change-Id: I339042fc3d5b072297e4748be71ad6770367917d
    
    Conflicts:
    	envsetup.sh

commit c0f5422d93bd994cd3a2bb488bac98afa2246189
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 9 17:59:28 2015 -0700

    build: update clang qcom optimization & removed fastmath keep -O3
    
    Change-Id: Ia629fcabf627b5bccdf5d3bce18596dd64c8d2b2

commit e27e82181f01746683c0454cb187d335c435976a
Author: Łukasz Domeradzki <JustArchi@JustArchi.net>
Date:   Tue Mar 24 16:50:56 2015 -0700

    JustArchi's ArchiDroid Optimizations V4
    
         _             _     _ ____            _     _
        / \   _ __ ___| |__ (_)  _ \ _ __ ___ (_) __| |
       / _ \ | '__/ __| '_ \| | | | | '__/ _ \| |/ _` |
      / ___ \| | | (__| | | | | |_| | | | (_) | | (_| |
     /_/   \_\_|  \___|_| |_|_|____/|_|  \___/|_|\__,_|
    
    Copyright (C) 2015 Łukasz "JustArchi" Domeradzki
    ----------------------------------------------------------------------------------------------------------------
    This is the squashed commit of countless hours spent on trying to optimize Android to the maximum and push it to the limits.
    Please give proper credit if you decide to cherry-pick this commit. It includes countless number of full builds and tests, almost 200 hours (KK), and additional 100 hours (LP) spent on compiling and testing
    ----------------------------------------------------------------------------------------------------------------
    WARNING! These modifcations are pretty DANGEROUS and may cause problems during compiling or running. You may also need to implement some fixes on your own.
    ----------------------------------------------------------------------------------------------------------------
    Pre-requirements:
    - GCC 4.8, both androideabi and armeabi. Fortunately for us, Lollipop already uses GCC 4.8, but it's in outdated versions and has some internal compiler errors with O3 flags this commit applies. Therefore, I suggest:
    1. SaberMod 4.8 arm-linux-androideabi -> https://github.com/ArchiDroid/Toolchain/tree/sabermod-4.8-arm-linux-androideabi (original source: https://gitlab.com/SaberMod/arm-linux-androideabi-4.8/tree/master)
    2. ArchiToolchain 4.9 arm-eabi -> https://github.com/ArchiDroid/Toolchain/tree/architoolchain-4.9-arm-linux-gnueabi-generic
    (Please notice that ArchiToolchain is available in many variants, you may want to select the one that suits you best, e.g. Cortex A9 onex)
    
    - (Optional) Target user, instead of userdebug. You should build with user variant instead of userdebug, as user variant in general pre-optimizes some parts and disables additional debug modules, i.e. dalvik debugging, procmem/procrank binaries and so.
    This can be done by multiple ways, e.g. using proper lunch command (i.e. lunching cm_i9300-user instead of cm_i9300-userdebug) or "brunch device user", such as "brunch i9300 user", if your android_build includes my CM commit -> https://github.com/CyanogenMod/android_build/commit/73db70d928f4a7af1d4a0a255327c6ff5d8ffbc9
    ----------------------------------------------------------------------------------------------------------------
    Important notes:
    - This commit has been tested on up-to-date CM-12.0 (Android 5.0.2), SaberMod's androideabi, and ArchiToolchain's eabi toolchains. Other ROMs and toolchains may, or may not, work out of the box with it.
    - You can ask for help in such cases in the XDA thread linked on the bottom of the commit.
    - You're applying these optimizations on your own risk, I highly suggest to understand what each of the flag does, and not trying to blindly "apply them all" and hope for the best. Also, due to various hacks and issues in various trees and devices, I can't assure you that what works for me, will also work for you.
    - Fortunately for you, my test device is Samsung Galaxy S3 with the nightmare Exynos4 SoC, so it's likely that it should work for major of the (better done) devices.
    - As pointed in pre-requirements, stock AOSP toolchains are outdated and have many internal compiler errors. This commit probably can work on stock AOSP toolchains, but you'll need to get rid of some flags that are causing those errors on AOSP toolchains (e.g. -O3 for thumb)
    - Due to O3 optimization, code is significantly larger and may cause problems with oversized images especially for older devices. For example, I couldn't apply O3 because building TWRP recovery failed due to the fact that it didn't fit on recovery's block in my device. In such case you have two options. You can use my little hack that ignored recovery size, so compiler doesn't yell about that (but you obviously can't flash such images), or you need to go back either to O2 or Os (for thumb), up to you.
    ----------------------------------------------------------------------------------------------------------------
    Important changes:
    - Optimized for speed yet more all instructions - ARM and THUMB (-O3)
    - Optimized for speed also parts which are compiled with Clang (-O3)
    - Turned off all debugging code (lack of -g)
    - Eliminated redundant loads that come after stores to the same memory location, both partial and full redundancies (-fgcse-las)
    - Ran a store motion pass after global common subexpression elimination. This pass attempts to move stores out of loops (-fgcse-sm)
    - Performed interprocedural pointer analysis and interprocedural modification and reference analysis (-fipa-pta)
    - Performed induction variable optimizations (strength reduction, induction variable merging and induction variable elimination) on trees (-fivopts)
    - Didn't keep the frame pointer in a register for functions that don't need one. This avoids the instructions to save, set up and restore frame pointers; it also makes an extra register available in many functions (-fomit-frame-pointer)
    - Attempted to avoid false dependencies in scheduled code by making use of registers left over after register allocation. This optimization most benefits processors with lots of registers (-frename-registers)
    - Tried to reduce the number of symbolic address calculations by using shared “anchor” symbols to address nearby objects. This transformation can help to reduce the number of GOT entries and GOT accesses on some targets (-fsection-anchors)
    - Performed tail duplication to enlarge superblock size. This transformation simplifies the control flow of the function allowing other optimizations to do a better job (-ftracer)
    - Performed loop invariant motion on trees. It also moved operands of conditions that are invariant out of the loop, so that we can use just trivial invariantness analysis in loop unswitching. The pass also includes store motion (-ftree-loop-im)
    - Created a canonical counter for number of iterations in loops for which determining number of iterations requires complicated analysis. Later optimizations then may determine the number easily (-ftree-loop-ivcanon)
    - Assumed that loop indices do not overflow, and that loops with nontrivial exit condition are not infinite. This enables a wider range of loop optimizations even if the loop optimizer itself cannot prove that these assumptions are valid (-funsafe-loop-optimizations)
    - Moved branches with loop invariant conditions out of the loop (-funswitch-loops)
    - Constructed webs as commonly used for register allocation purposes and assigned each web individual pseudo register. This allows the register allocation pass to operate on pseudos directly, but also strengthens several other optimization passes, such as CSE, loop optimizer and trivial dead code remover (-fweb)
    - Sorted the common symbols by alignment in descending order. This is to prevent gaps between symbols due to alignment constraints (-Wl,--sort-common)
    ----------------------------------------------------------------------------------------------------------------
    
    For more information, support, troubleshooting and discussion about my optimizations, please refer to my thread on XDA -> http://forum.xda-developers.com/showthread.php?t=2754997
    
    Conflicts:
    	core/Makefile
    	core/clang/config.mk
    	core/combo/TARGET_linux-arm.mk
    
    Change-Id: I7881bf14525c955934f79f1c58647134657cf823

commit ffb69a8fe79e2c342393e6faf71ae3d8ce24de02
Author: MaDc0w <MaDc0w@pac-rom.com>
Date:   Fri Mar 20 00:29:11 2015 -0700

    build: Rainbow unicorn puke [1/2]
    
    Change-Id: I393dd013194d73b293b361a42d42fa171ceee837
    
    Conflicts:
    	core/Makefile
    	envsetup.sh

commit 1ade499c9a1b2c6e6f011e6ebceb5f275ddff7f3
Author: JoseGalRe <josegalre@gmail.com>
Date:   Fri Mar 20 00:31:49 2015 -0700

    build: move chromium call...
    
    Change-Id: Ia91e750470f4af67487bf3e52d208bedc3a585dd
    
    Conflicts:
    	core/Makefile

commit 72a595eb3caa187067ddd1990d0af34f83ab9aec
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Sun Mar 8 16:29:37 2015 -0400

    build: Prebuilt Chromium files check
    
    Change-Id: Ic12f1d2559417f74af787e635d1ab882d07d9d00
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit 5e47d5ed9ff162d15b95dfbdf87fbb127ffd1943
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 14:16:59 2015 -0700

    build: removed gnu11++ optimization and fix SM version info
    
    Change-Id: I5dcd750856a7d7ef38dd8c0e339c8755724043f5

commit 4bea41e01a2d784c221fb94e60e177cc9d787814
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 24 00:04:48 2015 -0700

    build: -Wno-error=maybe-uninitialized
    
    Change-Id: I322f0d1951b461e44f3ebf913dab3afbb43bcb47

commit 7448f26066f58946216c741dab1193438f29074f
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 00:37:27 2015 -0700

    build: add cmremix version info
    
    Change-Id: I0fecd60a97b5c46f3262d5f030c6a23b2d2de5d0

project cmRemiX/
commit 3f2093da9b3d93d025b2ee8ebc3532458f277165
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:19:07 2015 -0700

    track SM arm-linux-androideabi-4.9

commit 581ec8c90d6489009147719e5b1cf26c302de605
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 12:25:26 2015 -0700

    CMRemix Optimizations

commit fe5caf6ab62ef029df087f233f8cde3f88406421
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:07:05 2015 -0700

    Switch to CMRemix Center

commit 8c652a1dace3d84396372826f9b963fa926e4e4f
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:08:44 2015 -0700

    derp

project device/qcom/common/
commit 54173c76997ed6fa71cfc104f2febf8171d7cdc2
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:47:59 2015 -0500

    power-8610: Add support for system performance profiles.
    
    Change-Id: I2f5002ffa0b1c63486056023a3cc6137559bcebd

commit d3b0b55c9839edc15cbc121cdd0bc8dd183fffe7
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:51:16 2015 -0500

    power-8610: Various updates to Power HAL
    
    Change-Id: If266f0a95a85bfc8dc8458ce7d71e569fa715c2f

commit 20913b8e440ad562d3e2e988b41de93fa138d1b6
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:52:35 2015 -0500

    power-8610: Add support for POWER_HINT_LOW_POWER
    
    Change-Id: Id25095ed549a84c07167f87f62f4e8add9a4cfec

commit a16b5835b16286e1b0d9ce4fda171b5417625660
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:54:12 2015 -0500

    power-8610: Remove the HMP boost hint
    
    Change-Id: I134c2656d806978ef683f70980be27d2bc60eb51

commit 8b1a74a93a41f593496bfbc2e484f369d3c29512
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:55:01 2015 -0500

    power-8610: Increase the boost a bit
    
    * eliminate a lot of jank. We're racing with input boost here.
    
    Change-Id: Ibce4ec734b4a9df82277b8e79425a87454b58dcd

commit f583378d3b7519c1530f28d19cf1322ab5ee37ff
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:56:13 2015 -0500

    power-8610: Remove unnecessary hint
    
    * This has the unfortunate side effect of actually *enabling* KSM,
      which we don't really need on this hardware.
    
    Change-Id: Idc3960fcb60169c2429d74309de50e52083664da

project external/whispersystems/WhisperPush/
commit 3a4cee933cca6940a8e8aa019f835db57151c886
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:54:00 2015 +0300

    Automatic translation import
    
    Change-Id: If0ed51471157bebd0a3a8cef9b6554b848b27a6e

project external/wpa_supplicant_8/
commit ad050d5c53eb81b00592d37f4e530b082f7b024b
Author: Diogo Ferreira <diogo@underdev.org>
Date:   Mon Mar 23 13:10:49 2015 +0000

    wpa_supplicant: Force the p2p channels to reuse frequencies used by STA
    
    In the mediatek platform the performance of p2p connections will
    degrade significantly if different frequences are used for STA and
    P2P.
    
    Change-Id: I8bd7e4a3f10177c99d273eccb88c8590fcbe3d34

project frameworks/av/
commit b2de0c19b11c8b83873510eb6c629cf4cfd62b1e
Merge: cf8c5de c29fb05
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:24:13 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

commit eb994da9ce6d24ce673c733e1e457c059ce08c70
Author: Ricardo Cerqueira <ricardo@cyngn.com>
Date:   Tue Nov 11 15:47:16 2014 +0000

    camera: Add support for mediatek cameras
    
    Change-Id: I69ea758645922c433844ab191a737de2ff2e1491

commit e126d3f0781676ad229522703c2d42d23f51d4ed
Author: Diogo Ferreira <defer@cyngn.com>
Date:   Mon Sep 15 15:44:39 2014 +0100

    mediatek: Port AV changes
    
    This ports the changes required to perform video decoding
    and enconding.
    
    The changes are ported from the mediatek BSP for mt6592
    with the minimum required feature set and confined to
    allow co-existance with changes from other vendors.
    
    [Trimmed down for L]
    
    Change-Id: I3709de0e5b9e4e0f68a71e182549e72a3dab26a7

commit da2439cc11b7c1b0281d7f5b53a597017e9b77d1
Merge: b2de0c1 e126d3f
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:21:37 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

project frameworks/base/
commit e7b2addb3dfd73ccfc6fe1fbc66f2763af87c74d
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Mar 23 00:00:45 2015 +0100

    systemui: don't use SIM display name if there isn't available info
    
    If there is no SIM info, then don't try to use SIM name.
    Also don't try to process all the network info data to obtain a network name, if we
    are able to extract it from SIM.
    
    Change-Id: I9b4ab296b7647ebab50925b8614beb820d2c6ace
    JIRA: BUGDUMP-1081990
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit abd644074d14c5b20863a38d2c09f77af7c90706
Author: maxwen <max.weninger@gmail.com>
Date:   Sat Feb 14 03:01:10 2015 +0100

    Fix screen pinning on devices without navbar
    
    Change-Id: I8451702f6af329be198bad6a1c07cf78a9de28a7

commit fd9d050c010ab28f1220735910cc9addc53bd0ac
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Mar 7 04:06:14 2015 +0200

    Move default value for Settings.Secure.ADVANCED_MODE to core
    
    * Move it out of SettingsProvider so it can be used in other packages
    * Upgrade DB version to force enable advanced mode when the overlay is true
    
    Change-Id: I7caf5dbda570b1b087f37fa18f8d0c14824d9a6f

commit df8fb0ace3c4a8871e56bb33d441b56c13f97da0
Author: Michael Zoech <michi.zoech@gmail.com>
Date:   Tue Dec 9 19:18:06 2014 -0800

    Move arrow_pointer hotspot to better match actual tip
    
    Hotspot position of (6,6) does not fully match the actually tip of the
    arrow_pointer cursor image. The position where the click is registered
    is visibly off. This can be verified by enabling "Pointer location" in
    the developer options.
    
    This patch changes the hotspot to (5,5) which better resembles the
    actual tip of the arrow.
    
    Change-Id: Id3c11181c42698c421b90c54e01c1f5f8ec27612

commit 834ff45b2c71576f7d324c18e5ea2fe4d3a5103e
Author: Samuel Asteberg <samuel.asteberg@sonymobile.com>
Date:   Wed Feb 25 15:51:05 2015 +0100

    SystemUI needs the SET_WALLPAPER permission
    
    If changing wallpaper when low on memory, retrieving the default
    wallpaper may return null, which triggers error handling in
    ImageWallpaper. This error handling tries to perform
    WallpaperManager.clear(), but for that it needs SET_WALLPAPER
    permission, which it does not have.
    
    For users with apps that auto change wallpaper, this issue can
    be frequent in low-memory conditions.
    
    The solution is to add the permisson.
    
    Change-Id: I81503c1667e3952c2dd15599969f7dcc51623e5b

commit 6f3815eede07c9d920091f6467db945a3c4ed738
Author: tiger_huang <tiger_huang@htc.com>
Date:   Thu Feb 26 14:45:32 2015 +0800

    Prevent unexpected rotation while going back to keyguard
    
    The original logic would let the app hidden by keyguard be able to
    decide the orientation. While going back from a show-when-locked app
    to keyguard, there would be a short time that keyguard is unable to
    decide the orientation, which causes WMS uses the wrong orientation
    from the wrong app.
    
    https://code.google.com/p/android/issues/detail?id=155640
    
    Change-Id: Ibc17bfe4603f68b241dc7380459ec9de42a3e259

commit 6e57098d78a366a6ba629a23241df79e9ae8239f
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 19:03:29 2015 -0700

    Frameworks/base: Don't allocate another identity matrix
    
    There is already an identity matrix in Matrix. Don't allocate another
    one for VectorDrawable.
    
    Change-Id: I51735f262d6680e043b0009707ec42acb2d0d1ad

commit 0c668d01496788783062137ae14c812852ff6005
Author: tiger_huang <tiger_huang@htc.com>
Date:   Thu Jan 29 19:54:12 2015 +0800

    Layout the window to be displayed if it would be resized
    
    This patch fixes an issue which caused the resumed app to get the
    wrong insets at first.
    
    https://code.google.com/p/android/issues/detail?id=120421
    
    Change-Id: I38c58121465372d1d66a7a98e386b0396d7d0f89

commit 8c50fce63ecfa1692176acd5775a94b370cc6319
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Tue Mar 17 18:22:51 2015 +0800

    [ActivityManager] Avoid killing unrelated processes.
    
    Kernel will reuse process id, when wrap-around happens,
    there may be just after a pid is freed, a new thread/process
    uses the pid immediately.
    
    For examples, there may be a process with pid 1234 killed
    by lowmemorykiller or itself (app.killed=false).
    Before the death recipient enters AMS, a new thread/process
    is started with pid 1234, then when appDiedLocked executes,
    this new pid 1234 will be killed again.
    
    It is especially easy happens to zygote:
    During zygote starting process, it will stop 5 daemons threads.
    And restart the 5 threads after fork is called, so it has
    larger pid range to hit the resue case.
    https://code.google.com/p/android/issues/detail?id=160661
    
    Solution:
    If the dead event is from binder, it is not necessary
    to call killProcessQuiet again, because it should really
    be dead.
    Keep no checking for killProcessGroup because zygote does
    not have record under /acct/, and also the parameter uid
    has restriction that will not kill another application
    which reuses the pid.
    
    Change-Id: Iec4a4884ae641c4d036f4d024ce463f7a351a17b

commit 27aed0cb7d01ce9d055cb4aa24af27d8afdb5fb7
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 25 20:25:01 2015 -0700

    Revert "Frameworks: follow charging notification settings also for wireless charging"
    
    This reverts commit 8626fd990f3905b1a79be485a730a21904655775.

commit 6606134bb832422c68edaa5d5b1607f640620bef
Author: Petr Sedlacek <petr@sedlacek.biz>
Date:   Fri Feb 6 21:55:30 2015 +0100

    Frameworks: follow charging notification settings also for wireless charging
    
    Originally, system would play a fixed notification sound when wireless
    charging starts from com.android.server.power.Notifier.java regardless
    of the Charging sounds settings. This removes the notification from
    Notifier.java which means the system will notify about wireless charging
    in the same (configurable) way as for normal wired charging.
    
    Change-Id: I034fc95f8ac3554ef1d463ac94bebd5a448e1a3f

commit 27f6e046c80f6722f0dd0eabd1b3cd0eaf8ccaba
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Feb 24 15:54:38 2015 -0800

    pm: Deal with a nuked package that was granted extra permissions
    
    Change-Id: I4c78c1b79903ab90a528811765155b2aaae39754

commit 4f58946665f6a62b575fabe513f6a1c44ba35b93
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 25 20:25:44 2015 -0700

    Revert "Temp restore permission for HARDWARE_ABSTRACTION_ACCESS"
    
    This reverts commit c54885a1097eaa50f59baf91b034aed22ee9eeb4.

commit 0738c80a249bfb03728bfe7b57e97c5aa214cdb3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Mar 26 02:51:30 2015 +0200

    Make forward/reverse lookup default overlay
    
    Change-Id: Ic0b9ebbc11edc661ec9c9563a8eabeaf7e014a46

commit 49ef7ec7f0507fd3efdde6e80a9baaa874db4fe2
Author: Raju Yadav <raju.yadav@sonymobile.com>
Date:   Mon Dec 22 14:54:13 2014 +0100

    systemui: Handle case when network has been lost
    
    If the network is immediately lost after becoming
    available the onAvailable callback may not yet
    have finished and is working with a lost network.
    In this case networkCapabilities may be null, so
    handle that.
    
    Change-Id: I588586ae0e844667cca4e2fd992d9694432a2198

commit f93856fb6bf72facf9d562226dbe035369d39ec0
Author: Daniel 2 Olofsson <daniel2.olofsson@sonymobile.com>
Date:   Tue Nov 13 15:16:23 2012 +0100

    Fix to crash when clicking text link without view activity
    
    A generated quick link to telephone number gets clicked and
    crashes if corresponding activity doesn't exist in device.
    It attempts to open up an activity to view content which will
    in turn generate an uncaught ActivityNotFoundException.
    Solved by catching exception when launching activity for the
    specified content.
    
    Change-Id: I47364519f1eceb5b978b29382107deae1891c7da

commit 0a57c9aa7b90587229fb9633ff4f890b608fb3b8
Author: Mykola Kondratenko <mykola.kondratenko@sonymobile.com>
Date:   Thu Mar 12 15:20:38 2015 +0100

    hwui : fix memory leak due to duplicate in shadow cache
    
    New ShadowTask with the ShadowDescription key that already
    exists in the shadow LruCache will leak as it is not being
    added.
    
    Fix adds check for the existing key that is common in the hwui
    code but missing for the TessellationCache::precacheShadow
    function.
    
    Change-Id: I37fd5ec82f8b8da5d1ec0f2ab9fd04c5f8534367

commit e37046b3c7a0b0bef7d79d9854cad49165592f2e
Author: Mathias Jeppsson <mathias.jeppsson@sonymobile.com>
Date:   Mon Mar 23 09:00:30 2015 +0100

    Sort Bluetooth devices in quick settings by name
    
    To avoid Bluetooth devices moving randomly in list, sorting by name.
    
    Change-Id: I4f8e9f98fa29f9670678a3bb6051a6fcf7ae0b9d

commit 7d7937c1ef0ed7bde00f6236f520923d23705a8a
Author: longyu.huang <longyu.huang2014@gmail.com>
Date:   Thu Mar 26 06:17:08 2015 -0700

    can not launch recents app after change time to earlier
    
    [Preconditions]
    set Home Button to launch recent apps
    
    [operating steps]
    1.long pres Home Button to launch recent apps activity
    2.press Back Button and enter Settings
    3.change current time to a earlier time
    4.long press Home Button has no response
    
    Change-Id: I354d9e273cd386a6876ad6795f6a0b1f6a2eff92

commit 847b6d50ee803e143524d3d4c9ffc99e0dd58299
Author: Lin Ma <lma@cyngn.com>
Date:   Wed Mar 25 17:44:52 2015 -0700

    Fix ro.telephony.default_network setting parsing
    
    * The code that parses ro.telephony.default_network is broken,
    instead of reading numbers separate by comma, it reads the first
    number and replicates it for other slots. Settings like "8,1" will
    be written to the db as "8,8"
    
    Change-Id: I6b77000e00ada02ec89b09c752a9b337a6a8182b

commit 3add7e086071c5c1fc5f5fbb06ba7337490e0001
Author: Lin Ma <lma@cyngn.com>
Date:   Thu Mar 26 18:42:52 2015 -0700

    Fix ro.telephony.default_network setting parsing - fix build error
    
    Change-Id: I600f0d1081eb9effe59d4a40975978e968c2b349

commit 714f5ff96f61435f6f10449f78168c7022364546
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 17 10:40:00 2015 -0700

    framework: add KillSwitch stubs
    
    Change-Id: Ie6cec065df0f821d9a5b8ab7bb3032fe7655389f
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 319cf9f25824036cbccb157073a41802754e13de
Author: Scott Mertz <scott@cyngn.com>
Date:   Fri Mar 27 01:07:33 2015 -0700

    SettingsProvider: fix index out of bounds error
    
    - If the property has less comma separated values than
      actual phones, this routine will throw an
      ArrayIndexOutOfBoundsException
    
    Change-Id: I8bb5e79f3ff107f6941d23f7035a41eaf05ba461

commit 37d9de4065ab84c2ed98500686abe0918ed9aed1
Author: d34d <clark@cyngn.com>
Date:   Mon Mar 23 14:40:24 2015 -0700

    Themes: Don't add android overlay if target is android
    
    If basePackageName equals "android" we are already overlaying the
    framework so there is no need to overlay it a second time.  This is
    the case for the system's resources as well as cases where explicit
    assets are being requested for a package, which could be the android
    package.
    
    Change-Id: I5c881e71bc4d733fc8dbd7f752874ba34ab50f69

commit 37d1cf590739234410976ab0f773e15470da035e
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 29 05:29:18 2015 +0200

    livedisplay: Don't depend on automatic brightness
    
     * Some devices will have this disabled or unavailable. Create the
       controller from DisplayPowerManager and give it a kick during
       screen power changes.
    
    Change-Id: I02af7e1bb3087bcf458a8238560b3c25b02637ac

commit 50991edd8da66ada289ce58851f735dcad1eaaa5
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Sun Feb 1 10:39:20 2015 +0800

    SystemUI: Fix no LED indication for missed call when screen off
    
    When device is going to sleep, showKeyguard() will be invoked to show
    lock screen. It shouldn't clear the LED notification at this moment.
    
    Do not clear the LED notification in showKeyguard(). This should only
    happen when user is actively viewing notification.
    
    Change-Id: Id81b9e854df9510d436f6eb8185ee4411c914dd9
    CRs-Fixed: 783613

commit 1cc245649c7a329c9dd6c473fc57c8d1686a21d2
Author: Kishore Srivenkata Ganesh Bolisetty <bsrivenk@codeaurora.org>
Date:   Mon Jan 5 17:40:39 2015 +0530

    frameworks/base : Enable Aggressive trim settings
    
    This change will enable aggressive trim settings for targets
    up to 1gb. The change can be turned on/off from system properties.
    By default, the properties are set for targets up to 1GB.
    
    Change-Id: I233dddbff07e7ec1fe2ee96402fe1d411903beb5
    CRs-Fixed: 783020

commit a30539b8ddad3e749b903ceecb9688921f988164
Author: Lijuan Gao <lijuang@codeaurora.org>
Date:   Wed Dec 3 13:36:51 2014 +0800

    bootanimation_main: Disable boot animation when device is triggered by alarm
    
    When the phone is triggered by alarm, it's better to show the deskclock
    directly instead of bootanimation as the new requirement from customers.
    So disable bootanimation in such case.
    
    Change-Id: Id8e92a492cc2281f1fe4c620fdaa8c293c4aa369

commit 1d81f20ba254b02337a1677525be02ce7722a6f5
Author: tiger_huang <tiger_huang@htc.com>
Date:   Thu Nov 13 18:22:44 2014 +0800

    Clear the previous states before setting the new app visibility
    
    If setAppVisibility() is called multiple times in a short interval
    while the screen is turned off between the calls, the visibility of
    the app would be wrong. For example, the user may see the app under
    the launcher, not the wallpaper under the launcher.
    
    The flow to the issue:
    1. Screen is on.
    2. AM calls setAppVisibility() token=App A's token, visible=true
    3. Screen is turned off.
    4. AM calls setAppVisibility() token=App A's token, visible=false
    
    Note:
    a. In 2., WM would put App A into mOpeningApps, and tell it to be
       visible.
    b. In 4., because the screen is off now, App A would not be removed
       from mOpeningApps. App A might be told to be invisible directly
       through setTokenVisibilityLocked(), but it would be told to be
       visible again in handleAppTransitionReadyLocked() later.
    
    Change-Id: Icf3d69031ea2822245008248ec8f12bd57218880

commit 38820d793d98b6e99bc98ecc50b5e12586cdb4e2
Author: tiger_huang <tiger_huang@htc.com>
Date:   Fri Jul 11 18:41:48 2014 +0800

    Remove the window whose client process has died or become zombie
    
    Window Manager Service would fail to report window-resized to the
    process which has become zombie. This would cause the window to
    freeze screen continuously. In this case, we assume the process has
    died and remove its window to recycle resources and to prevent it from
    freezing the screen.
    
    Change-Id: Ic7384731bf9a1fa8b9602d4f1dbee7492db126c5

commit 6661e3b08bfcc25137c1fd7fb722d2bc05e4a516
Author: Dohyun Lee <dohyun.lee@lge.com>
Date:   Mon Mar 23 09:16:34 2015 +0900

    DimLayer : remove unnecessary surface transaction calls
    
    There is the case that adjustSurface()  get called even if
    the size of the surface of DimLayer is not changed actually.
    Since changing the size of a surface is processed synchronously
    in the SurfacFlinger, there is usually a few milliseconds delay
    (up to 1 vsync interval) when we launch an application.
    This patch avoids such cases.
    
    Change-Id: Ib1f76d54f9f2364ac54b70120e4b781e8534e750
    Signed-off-by: Dohyun Lee <dohyun.lee@lge.com>

commit fb579600774f3788964d5a55dc6ef44ff87f665c
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Mar 28 02:49:27 2015 -0700

    BlurLayer: Remove unnecessary surface transactions
    
     * As with the previous commit, do the same for the blur layer.
    
    Change-Id: If56210f2d07091f24872a1be6d6e3eaa8fdcebe9

commit baee473f14e8bc55b1765bd2fd886c0584fc6476
Author: Dohyun Lee <dohyun.lee@lge.com>
Date:   Sat Mar 21 17:03:04 2015 +0900

    Assign more reasonable width and height of a window surface
    
    When the surface of a window is created during relayoutWindow,
    there is the case that the width and height of the surface are
    not given appropriately, e.g. the staring windows.
    In this case, the width and height are set to 1, which cause
    resizing the size of the surface during setSurfaceBoundariesLocked.
    Since setting the size of a surface is processed synchronously
    in the SurfaceFlinger, there is usually a few milliseconds
    delay (up to 1 vsync interval) when we launch an application.
    
    To remove such cases, this patch assign the width and height
    more reasonably like below:
    
     1. If FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS is set then assign
        the size of the display we can use.
       (i.e. DisplayInfo.logical[Width|Height])
    
     2. Otherwise, assign the width and height of the portion of
        the display that is available to applications.
        (i.e. DisplayInfo.app[Width|Height])
    
    Change-Id: Ie8265b9ff0fdb6ecc4577687935adf7cfb4439ad
    Signed-off-by: Dohyun Lee <dohyun.lee@lge.com>

commit aaf5b39359dcf786c86a62b57879a606c7fa89c2
Author: Amit Shekhar <ashekhar@codeaurora.org>
Date:   Fri May 9 10:57:52 2014 -0700

    frameworks/base: Fix delay in sending AUDIO_BECOMING_NOISY intent
    
    AUDIO_BECOMING_NOISY intent is sent as background intent which causes
    delay in receiving pause event. This delay caused audio leak. By
    marking the event as FLAG_RECEIVER_FOREGROUND, this intent is
    received sooner by Application.
    
    Change-Id: Ib978cf8322dcddbc01f59824f95fa7800f9c35af
    CRs-Fixed: 652549

commit d0885c1edabbdfba6c0ff7e469351629830dafe0
Author: Maunik Shah <mshah@codeaurora.org>
Date:   Tue Apr 22 20:32:55 2014 +0530

    Fixes large number of thumbnails leads to low memory
    
    Due to huge number of pictures taken either by camera or
    sceenshots, thumbnails of those pictures fills the internal
    storage quickly in low internal memory device
    
    Change-Id: If77e24c20feb89cd1755d308d6f3bc0348c528f9
    CRs-Fixed: 650808

commit 5921201a66e45d73600aff10b80f0d381e0eff04
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:45:29 2015 -0700

    Revert "Make forward/reverse lookup default overlay"
    
    This reverts commit 66ef0e3abc8ed9c59553a1ae905e308118a679cd.

commit 481230ac7f61c4cb5a0cc7720627c275ea363b0c
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Mar 30 02:15:08 2015 +0200

    keyguard: refresh carrier info on subId changes
    
    Currently, the SPN_STRINGS_UPDATED_ACTION intent receives the phoneId and subId, but sometimes
    during boot the SubscriptionManager isn't be updated yet, which lead to SPN and PLMN were mapped
    with an invalid id in the KeyguardUpdateMonitor, and CarrierText not being updated, although
    in the phone implementation the data is correct.
    This change updates the carrier info also on SUBID changes, so in case the subid were
    updated after SPN_STRINGS_UPDATED_ACTION, all SPN and PLMN can be mapped properly to the
    correct SUBID and CarrierText update with the right values.
    
    Change-Id: Ia4243ee8781a31942cb4370489df17f9c970e41f
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 443f003d086520562bdf3eaf2bd0b868e75f2901
Author: Jason Sams <jsams@google.com>
Date:   Thu Mar 26 14:47:17 2015 -0700

    Fix potential npe
    
    bug 19805515
    
    Change-Id: Id36b145d3ce1c81311e88f5cdd2441880e98f737

commit d5c9d4632fb4321650d091b3628f7becaa701db8
Author: Jason Sams <jsams@google.com>
Date:   Thu Mar 26 15:29:56 2015 -0700

    Catch errors for unknown object types.
    
    bug 19805334
    
    Change-Id: I71e172b8123076896737d352403f8ddefca544b6

commit e1ff27cf0147b05f64bfb9dbdc63b3c975d4cc87
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:22:49 2015 -0700

    Frameworks/base: Fix request removal in VoiceInteractionSession
    
    Fix and simplify removeRequest.
    
    Bug: 19797138
    Change-Id: I0eca877e3109c9f39cebd4c888f166ce334fcc0e

commit 585659de27ffdd5c7c7c997078b041d496858865
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:47:42 2015 -0700

    Frameworks/base: Change String == to equals in Preference
    
    Bug: 19797138
    Change-Id: I496b12c425da45ee098db12e72ad843c22444ba3

project frameworks/opt/net/wifi/
commit edbc0d618f2f47640c8ecc8d65f4b2b01b28cd5f
Merge: 5a16c4c 67d21c2
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:27:21 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

project frameworks/opt/telephony/
commit 1f567a1761820a24df3f4f2ec6c872b0c5ea7e5a
Author: Hu Chunming <chunmi@codeaurora.org>
Date:   Tue Feb 10 16:05:04 2015 +0800

    Fix issue that DDS can not get back to primary sub and network mode shows incorrect in settings.
    
    ModemBindingpPolicyHandler sends pref network mode to RIL, but even if
    it fails, it also updates network mode to telephony DB.
    
    Update the DB only on success of setting network mode for all subs.
    
    CRs-Fixed: 789724
    
    Change-Id: I1121d75226415d3b08c58a4aa1b6a3a060712511

commit 6758cae097904ed08cb974e8491e12360fbbc8a2
Author: Susheel nyamala <snyamala@codeaurora.org>
Date:   Fri Feb 13 14:27:03 2015 +0530

    Fix initial attach apn bug with OMH profile for LTE
    
    During apn list creation, OMH profiles are queried from sim card and
    if found they will be used for initial attach, data call setup. These
    OMH profiles are applicable only for Cdma networks, and if used for any
    other networks will result in issues. Currently, there is a check to avoid
    using OMH profiles for Gsm RATs, but that check is failing for Unknown RAT
    case and OMH profiles are being picked up for initial attach request.
    
    Modify the existing condition to check for Cdma network, to make sure OMH
    profiles are used only for Cdma.
    
    Change-Id: If88030d2c37069d0a59af9eb096db835095cb804
    CRs-Fixed: 794383

commit 3c019b06a3f479c1e9691295f058108b120b533d
Author: Chaitanya Saggurthi <csaggurt@codeaurora.org>
Date:   Thu Feb 5 18:37:59 2015 +0530

    Add dummy SUB record in CDMA NV mode
    
    Add dummy SUB info record when NV is ready in CDMA NV mode.
    
    CRs-Fixed: 789989
    
    Signed-off-by: Adnan <adnan@cyngn.com>
    Change-Id: Ie658087efaa9f93a329773d2d8f0601d083f3701

commit e08a543970be4e60a18adb044d15a11341cb0c67
Merge: 7063661 3c019b0
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:26:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project hardware/qcom/audio-caf/msm8916/
commit cb739e9aa15cfae45d49fed57a7a5ed4cf779204
Author: Ethan Chen <intervigil@gmail.com>
Date:   Fri Mar 27 19:35:25 2015 -0700

    hal: Correctly set backend to best available parameters
    
    * For the case where CALL/IN_COMMUNICATION, new_bit_width and
      new_sample_rate were unconditionally reset to 0, resulting
      in a sample rate/bit width change always occurring.
      Don't do this for CALL/IN_COMMUNICATION as the original
      logic intended.
    
    Change-Id: Ib647cec084f4af9a044f90935dd57257bba0ec06

commit 5646b80672c61fc3a092a1ef73a77c020539d4ad
Author: Ethan Chen <intervigil@gmail.com>
Date:   Fri Mar 27 17:35:48 2015 -0700

    hal: Reduce debug verbosity
    
    Change-Id: Ie7a429ce3fdd8cc818af70ec0191d470d532bb3d

project hardware/qcom/audio-caf/msm8960/
commit df794795c6531f7d40fcb83efbc96940d6c26b70
Author: Ethan Chen <intervigil@gmail.com>
Date:   Tue Mar 31 11:25:54 2015 -0700

    alsa_sound: Remove orphaned QCOM_COMPRESSED_AUDIO flag
    
    Change-Id: I2a13b6cd61fdbff3305ae102e6addc0ddc5cbd26
    (cherry picked from commit a855be6336e99193169ad4c7073171a1883eb8ac)

project hardware/qcom/display-caf/msm8226/
commit 9adc0650dc738b0b15f978972bd77f8f3dd49903
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Wed Mar 25 20:49:35 2015 -0500

    msm8226: add missing symlink to common.mk in msm8974
    
    Change-Id: I4d6912383261423d1e49ac7abcc07f823b9d984d

project hardware/qcom/display-caf/msm8610/
commit e931f9e1db0017871f995ae53366e092be01afc6
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Wed Mar 25 20:49:35 2015 -0500

    msm8610: add missing symlink to common.mk in msm8974
    
    Change-Id: I4d6912383261423d1e49ac7abcc07f823b9d984d

project kernel/samsung/trlte/
commit 17661d34de75a067eef3794d86632d105d718957
Author: Junjie Wu <junjiew@codeaurora.org>
Date:   Wed Dec 3 18:29:35 2014 -0800

    cpufreq: Return directly in __cpufreq_get if policy is NULL
    
    __cpufreq_get() checks whether policy->cur matches frequency returned
    by cpufreq device driver and acts accordingly. However, policy could
    be NULL if the CPU is being hotplugged. Current implementation crashes
    when trying to dereference the NULL policy.
    
    Return the frequency provided by cpufreq device driver directly if
    policy is not available.
    
    Change-Id: I1f2ba4028c259392bf730db37dbec2d8c5ae3fa4
    Signed-off-by: Junjie Wu <junjiew@codeaurora.org>

commit ab35aa23cfe0f9839db50f1fbee0137223676aa2
Author: Junjie Wu <junjiew@codeaurora.org>
Date:   Tue Nov 18 16:49:42 2014 -0800

    cpufreq: Protect against hotplug in cpufreq_register_driver()
    
    cpufreq_register_driver() could race with CPU hotplug during
    bootup. Since hotplug notification is not registered when
    subsys_interface_register() is being executed, it's possible
    cpufreq's view of online CPUs becomes stale before it registers
    for hotplug notification.
    
    Register for hotplug notification first and protect
    subsys_interface_register() against hotplug using
    get/put_online_cpus().
    
    Change-Id: I26b2908f1d167c2becc4e8664c357bb7c6162406
    Signed-off-by: Junjie Wu <junjiew@codeaurora.org>

commit ef084a9cff659bae01a1ded641fb9b885801ea59
Author: Maria Yu <aiquny@codeaurora.org>
Date:   Tue Jul 8 12:16:17 2014 +0800

    cpufreq: Add if cpu is online check in show
    
    Make sure CPU is online before proceeding with any "show"
    ops. Without this check, the show can race with hotplug
    and try to show the details of a stale or non-existent
    policy.
    
    CRs-Fixed: 689522
    Change-Id: Ie791c73cb281bcfc4d722f7c8c10eee07cb11f2e
    Signed-off-by: Maria Yu <aiquny@codeaurora.org>

commit 4108fb6937458f248dbb3c06f2cbf49c013c57d0
Author: Maria Yu <aiquny@codeaurora.org>
Date:   Tue Jul 8 12:29:23 2014 +0800

    cpufreq: Use correct locking for cpufreq_cpu_data
    
    Use write lock when updating cpufreq_cpu_data,
    and read lock when getting the policy pointer.
    
    CRs-Fixed: 689522
    Change-Id: I454f0d575157b3411d369e04097386f50aeaaa1c
    Signed-off-by: Maria Yu <aiquny@codeaurora.org>

commit 9e720a9bee614935602eb70cda7118be79271aad
Author: imoseyon <imoseyon@gmail.com>
Date:   Thu Mar 12 23:03:13 2015 -0700

    Revert "cpufreq: force cpuN policy to match cpu0 when setting min freq"
    
    This reverts commit 0b9948790567748d7dd34a74ff593277d4fc13c2.

commit 14fa0cd2e14b0704e3e9b4accf851eb9eadd209b
Author: imoseyon <imoseyon@gmail.com>
Date:   Thu Mar 12 23:03:20 2015 -0700

    Revert "cpufreq: force cpuN policy to match cpu0 when changing freq or gov"
    
    This reverts commit 3a6afd3e14e441950ffe80699688db53e374905d.

commit 4500208a8b9cd753942a5c60ac3311550f9429a2
Author: imoseyon <imoseyon@gmail.com>
Date:   Sun Mar 22 16:18:25 2015 -0700

    cpufreq: prevent min/max freq changes in kernel space via sysfs
    
    * mpdecision and msm_thermal are the two culprits

commit ffe1c022af11c86d0b6c80cc12f945cae735ad4c
Author: imoseyon <imoseyon@gmail.com>
Date:   Wed Mar 25 17:57:12 2015 -0700

    cpufreq: revert maxfreq change prevention code for upcoming V2
    
    * but keep the minfreq change prevention code

commit 524ab8fa4ba5323c48b145b44a72221b64c59f9e
Author: imoseyon <imoseyon@gmail.com>
Date:   Fri Mar 27 21:40:45 2015 -0700

    cpufreq/thermal: frequency mitigation preventer V2
    
    My previous implementation wasn't working 100% of the time, and
    also prevented some frequency based thermal events.
    
    V2 should fix all of that and allow normal temp based thermal events
    to happen. Once enabled (disabled by default) via sysfs (full_fm),
    it will prevent userspace process from lowering maxfreq unless core
    temp has exceeded the default threshold of 80C.

commit 5cb55c0d5ae6c4ecc6b2930920e507b50d6436ab
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 21:50:21 2015 -0700

    update defconfig

project packages/apps/AudioFX/
commit f9079c48c9db162d13e2ad4abe5a1db9d8a01941
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:13 2015 +0300

    Automatic translation import
    
    Change-Id: I2ac8c8e442b1e904e7476e78e475eac7597c1de2

project packages/apps/Bluetooth/
commit 68431a78c1e5c6b8523ce7b18d1be3c71c399f55
Author: Sai Aitharaju <saia@codeaurora.org>
Date:   Thu Jan 22 17:56:21 2015 +0530

    Bluetooth App: Fixed the HDP disconnection notification failure
    
    When a HDP connection is disconnected, HDP disconnection
    notification isn't sent to Application as the Health
    ChannelCallback was skipped. Fixed the issue by placing
    the NULL check at the appropriate position.
    
    CRs-Fixed: 785322
    Change-Id: Ib1bc5c7677c1583b7fe582fe27f157880e764ad9

commit 1c1573858cfd53dda32103047e7534a842aaf605
Author: Hu Wang <huw@codeaurora.org>
Date:   Tue Dec 9 15:34:40 2014 +0800

    Bluetooth: Fix BQB AVRCP case AVRCP_PAS_BV_08
    
    In this case, remote will ask for player application setting value
    texts. If music player doesn't reply value texts, AVRCP should
    reply with empty value text.
    Change code to handle GET_VALUE_TEXT separately.
    
    Change-Id: I93c33fb7653fd8d147afe0e3d3cdd15261622df6
    CRs-Fixed: 764390

commit ffabe89cf27412c8833a2251e9e58f36964ffda4
Author: venkata Jagadeesh <vjagad@codeaurora.org>
Date:   Thu Feb 5 11:05:10 2015 +0530

    Bluetooth: GAP: Call system.exit in cleanup
    
    As we are not clearing the internal static memory during bt off,
    paired device list will be updated from internal memory
    instead of bt_config.xml and paired list will be different for
    different user logins.
    If we call system exit it will kill the process and clean intenal
    memory
    
    Change-Id: I69b5485e2202413692c685a595de9ce96985f669
    CRs-Fixed: 798825

commit 5c887b844806f5279b3434036e76963d27b5090e
Author: Juffin Alex Varghese <jalex@codeaurora.org>
Date:   Fri Jan 30 18:57:11 2015 +0530

    Bluetooth-OPP: Check socket congestion status before writing the data
    
    This change will ensure that data will be send to socket only after
    congestion is cleared. Otherwise, if socket is already in congestion
    and send the data before clearing, will cause transfer failure.
    
    CRs-Fixed: 790313
    Change-Id: I8847a9f3473d97cd6fadf24e293ac179418df457

project packages/apps/BluetoothExt/
commit 2e5469a4c603575e15207ee316a997fde1d5aaac
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:21 2015 +0300

    Automatic translation import
    
    Change-Id: I7683ee1bc96195e700c04e96f833cef5dd9f38aa

project packages/apps/CMFileManager/
commit 6e039982eb0d6f8bc39d8690f67b2622ec1efcb0
Author: Matt Garnes <matt@cyngn.com>
Date:   Mon Mar 23 17:52:59 2015 -0700

    Support ambigous file extension mimetypes.
    
    Previously, CMFileManager operated under the assumption that file
    extensions map to exactly one mimetype. This is not true in some cases,
    such as .3gp files, which can have an audio or video mimetype.
    
    Add support so that in mime_types.properties we can specify a comma
    separated list of mimetype info that are matched with a given extension.
    If an AmbiguousExtensionHelper subclass implementation is provided for one of these
    extensions, this is used to determine the correct mimetype for the file.
    
    Change-Id: Ie73d6ad646692dfeac112ac50c1c6436e6b5559b

commit 8b1fef1fb52c2f0f5268e1a99b415e83f0db04a0
Author: André Rivotti Casimiro <acasimiro@cyngn.com>
Date:   Mon Mar 30 11:08:06 2015 +0100

    make sure MountPointInfo and DiskUsageInfo runs in the UI Thread.
    
    At some point the original View was dettached and both mMountPointInfo and mDiskUsageInfo handler's were null which means the Ruannable wasn't executed.
    
    Change-Id: I883af543b19bc644e451109675c241a8c84e5d64
    (cherry picked from commit d7558cf8cdbcc377264c3ff1f05e2c202380c97e)

commit 3a7e64a1b55a8cdd0b2053fd6b16c294c3137d05
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 30 10:07:09 2015 -0700

    CMFileManager: account for displayed dialogs during activity tear down
    
    Repro:
     - Start copying a large file (>100 MB)
     - Leave CMFM and trigger a config change
       (e.g. set text size to small in Settings -> Display)
     - Return to CMFM
     - Observe: window leak in logcat
    
    Change-Id: Ic875d4f86edf0446b889e6442126bd76a692a7c6

commit a81e287b351758191166c3e2b1cc5f6be94c6df3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:49:21 2015 +0300

    Automatic translation import
    
    Change-Id: I761573acfc3cdd1fb7885b1cc173b4dcc113ac87

commit e1913eb1fb84fc782bd3bb5d49ff75ed3b89ca06
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 31 09:49:39 2015 -0700

    CMFileManager: change warning drawables used in dialogs for visibility
    
    Change-Id: I5256322a460f8fab268a6f36022aece2bdabd677

project packages/apps/CMRemixCenter/
commit 103ea6423ac51bb351aafc1d455259dd7db8b6b7
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:55:24 2015 -0700

    CMRemix's fy

project packages/apps/Calculator/
commit 02c812388c96949733bd6cb2ee2f33b23cfadbbd
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 27 15:48:10 2015 -0700

    Calculator: allow for deletion when selector is next to a separator
    
    Repro:
     - Open calculator and enter "1234"
     - Observe: calculator edit text reformats to "1,234"
     (Or regional equivalent)
     - Place selector to the immediate right of the separator ","
     - Use the delete key
     - Observe: no deletion occurs
    
    Change-Id: I810c1e8fb0f15bed8c9d173cb39e6cd9290a24f5

commit d7a11b45483cd8d7900fb91177f6ed0370798f9e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:28 2015 +0300

    Automatic translation import
    
    Change-Id: I28cb2066b789d137530a09c60065c2837a4d614a

project packages/apps/Calendar/
commit e1cc82977982965a5458abbf295496178d53879d
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:41 2015 +0300

    Automatic translation import
    
    Change-Id: I481b993408c8583b2d413e41bed2b38ad63c8afe

project packages/apps/Camera2/
commit 40d8dce70728e2970675df8b04a47db66d8a634d
Merge: 982bcc1 7a11a41
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:30:20 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 0a2eab16cc617fcb3c6b4a40c7456db555602ab1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:51 2015 +0300

    Automatic translation import
    
    Change-Id: I685a9acbcc6a2c99e20bc0ab68db574000d488db

commit 023f0648edca49e3b1e56e6240262821613cc57e
Merge: 40d8dce 0a2eab1
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:48:09 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/Contacts/
commit 01b69c2bf03243ace3c6854b3616412a7d979345
Author: Matt Garnes <matt@cyngn.com>
Date:   Thu Mar 19 16:30:37 2015 -0700

    Summarize local phone storage in MemoryStatusActivity.
    
    As the first item in the list, find the number of Contacts stored on the
    device with PhoneAccountType.ACCOUNT_TYPE.
    
    Depends on http://review.cyanogenmod.org/#/c/91855/ to display
    correctly.
    
    Change-Id: Ib421a1e9e2fa99310f5591c8db75c9a48b93b3ee

commit 70c46843046817655a92cba33217dbf44809d19b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:49:45 2015 +0300

    Automatic translation import
    
    Change-Id: I29826c35f016619dc01d73618d4bfe9ab13e4380

project packages/apps/ContactsCommon/
commit aa1e73422689ba21ad2aa909446b63908a455886
Author: Matt Garnes <matt@cyngn.com>
Date:   Thu Mar 19 16:53:37 2015 -0700

    Store all local contacts in only one account.
    
    In 1122a58d3e8b4f85ffbc97aecbf76f57b2711065, a second local account was
    introduced. This is used in many more places than the original
    phone-local (introduced in 7189fda4cbcd162555d59ee335709173ee46bbea)
    so change all references to this local account to use the new one.
    
    There are several places where exactly one local account is assumed,
    such as in ContactProvider. We should combine all local contacts into
    one account name and type.
    
    Change-Id: I1781d009557ece05e9eaa078847756c428a8fbbd

project packages/apps/DeskClock/
commit ba1a197833a1cd35897aa823f610f66754060a6d
Author: Diogo Ferreira <diogo@underdev.org>
Date:   Wed Mar 25 15:31:08 2015 +0000

    TimerReceiver: Correctly show the remaining time for 100 hours
    
    If you open the Clock countdown time and input 99h99m99s it will
    actually translate to 100 hours, 40 minutes and 39 seconds as
    expected.
    
    When leaving the app it will show a notification with the remaining
    time and if there are more than 100 hours it will fail to show
    that part and only show "40 minutes remaining".
    
    This patch fixes allows for 100 as a valid input.
    
    Change-Id: Ib3621691aaa3a449262cb9e3601d39283bb808f8

commit 106cfa2bca37303a93e1826c04d88783aa15b52d
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Wed Mar 25 15:31:42 2015 -0700

    Hide flip setting if the phone doesn't have the required hardware sensor.
    
    (╯°□°)╯ sʞɔolɔ
    
    Change-Id: Iba38e37bffe91d0d5bd9bb8922b4c168386ebfd9

project packages/apps/Dialer/
commit 08affcd02b32799b8aef75e7a3e1d6fa8017d8fa
Merge: 8fccd14 a59cffd
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:30:52 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit c286b7c48edb71f0fa55baf31e0912fc8a3f150a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:49:56 2015 +0300

    Automatic translation import
    
    Change-Id: I6d183d3b7b0520cf7a13ebb27055e385393812cf

commit 5f9504cac52cd79ded50e095bfe434037d9a7c2c
Merge: 08affcd c286b7c
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:49:46 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/Eleven/
commit 92ad21c7a59997573c70f91814943a546a2d7e4b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:06 2015 +0300

    Automatic translation import
    
    Change-Id: I3146069beab8e56c5583ac8c3068b8f2ba65daa3

project packages/apps/Email/
commit 8ee3601a81b4107c4ccd7fe1f3032f18af7cba79
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 27 00:57:30 2015 +0200

    Update strings for crowdin
    
    Change-Id: Ib59198e1321db5b3c6889432c842d42dd040cea4

commit 7e5d7969c7a4f143f82b08e91ba1007244eefd8e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:15 2015 +0300

    Automatic translation import
    
    Change-Id: Ifd737704c6917543e69c08bcf3800ecc309a0f4e

project packages/apps/Exchange/
commit fb3d125ebe6c3a0714683e50459519f0c981c41f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:55:16 2015 +0300

    Automatic translation import
    
    Change-Id: I9be8c909a2859ab23b18d31d7d89f1e379db46df

project packages/apps/Gallery2/
commit d158308a312acccedabe33b688454dece97134f5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:24 2015 +0300

    Automatic translation import
    
    Change-Id: Iaa89ae9514149bc83e12c34fc8e200532adbccca

commit f70b3710833e40c589ca5dea70085ff314a59bbc
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sun Feb 8 06:49:41 2015 +0000

    Moar materialize changes
    
    Change-Id: I2a4987c1220dfb772289c6638648702d26600aa7

project packages/apps/InCallUI/
commit c2f1d5b718cd9d09aded6ec06c338e43fd00bca3
Merge: e7d9602 6240812
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:31:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 4dfef8cbe64c0b6cfc45a1d40e17cfba4685f2e5
Author: Matt Garnes <matt@cyngn.com>
Date:   Fri Mar 27 18:05:42 2015 -0700

    Allow hiding volume boost feature with overlay.
    
    Some devices do not support it, or do not support it well. Allow us to
    hide it with an overlayable config flag.
    
    Change-Id: I2c3b0b5d3a6e738b311b365f5855c41f7d08ab9a

commit e09dd44611fb5db0adf84e174b1e9bcbdcaf2bfe
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:31 2015 +0300

    Automatic translation import
    
    Change-Id: Ie8bc55494250d5ccae3efa590d2f37eefce0c92d

commit 84deef9a0ae0ed6125684fe53945bd1f865cfd48
Merge: c2f1d5b e09dd44
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:56:36 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/LockClock/
commit 6741b1e37158069969f78c444dfad1e96e32afa4
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:40 2015 +0300

    Automatic translation import
    
    Change-Id: I6293d07ab2144e1169e14dcdf4f2ef2bcf2d0940

project packages/apps/Mms/
commit 6ba0152cffd3e47c53dbcd81e00be8bee6cae207
Author: Craig Schmitt <craigschmitt@cmshome.net>
Date:   Mon Jul 7 18:26:29 2014 -0500

    MMS: Add feature to auto-enable mobile data for MMS send or receive.
    
      Feature is default overlayable via "enable_data_for_mms".
    
    Signed-off-by: Adnan <adnan@cyngn.com>
    Change-Id: I1b79d42fb7ef16de4aedf5557ae6f3f82dd3a7c3

commit 86c2354ca87dfdf511ee487d3a86a7ec3a4a1fb3
Author: Danesh M <daneshm90@gmail.com>
Date:   Thu Mar 26 19:44:03 2015 -0700

    Mms : Dismiss compose activity, if deleting last message and no text
    
    Change-Id: Iedfbddec88e30cb3aa4f76a8c59c44c24603671c

commit 066f6b42113d532223ee65aa531f54b4abeb6704
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Wed Mar 25 01:23:07 2015 -0700

    Mms - remove Subject listener first when remove the subject
    
    epro:
    - Go to messaging-> add subject ->add an attachment
    - Delete subject and then delete the attachment
    
    Result:
      Still show Mms,Can not converting to text message
    
    Change-Id: I410f018385807862a80be48d4dfeb6cb513f5a1b

commit 1d4f0cbead9fe4958213381e33d8a7ad8dea7089
Merge: a6e39f9 066f6b4
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:32:14 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 4071e1dc3a821c364692fb5019a5c5578edaf78f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:46 2015 +0300

    Automatic translation import
    
    Change-Id: I21f4284af735d645ebbb1c4e2b2cd58ad03c07e6

commit bdca85d8efd9b7683dc4ecd97b98b990b40d314a
Merge: 1d4f0cb 4071e1d
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:57:19 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 8334d601983767cfc8d5274a15271b1a8ee54ed3
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Mon Mar 30 06:03:55 2015 -0700

    Mms-add Calendar event type of loading Calendar draft
    
    Repro:
    - Go to messaging-> add subject ->add an Calendar
    - back save as a draft->then type it->the Calendar cant see
    
    Change-Id: I1a54e5712a9ab4e16b9d3b793cff617e5d60218e

commit 05d424a484a25eb40e063ffb812802a085c1d5c1
Merge: bdca85d 8334d60
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:38:04 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/Settings/
commit 20c5bcc0b3c354da52bd990ebb87f21a9608c45e
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Mar 23 18:22:17 2015 -0700

    Settings: prompt to fill new profiles out only once
    
    On rotate, this popup would keep coming up, even after the user
    expressed yes/no.
    
    Change-Id: Iac47797f8a9538d0bedf1db4a41209578df544f3
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit f70bbd33aa5491a957874d4bd112a88a82bfa78e
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Mar 23 18:21:36 2015 -0700

    Settings: fix mobile network switch being unchecked
    
    Sometimes when connected to Wifi, the mobile data switch gets checked
    off, even though mobile data is enabled.
    
    Change-Id: I4d28366f9c7aa63d20b215d39bdcb04f7b6e83dc
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 1d490b26a8055d35addec913b1c7d7d9e3ba7815
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Fri Mar 27 20:14:44 2015 -0700

    Settings: Remove "advanced mode" toggle if its defaulted to enabled.
    
    Change-Id: I0c0fe0bab337d0c8c6d48e20228aa26c86a2475f
    
    Conflicts:
    	src/com/android/settings/DeviceInfoSettings.java

commit d7c7ea7d68c6c19622aaf68bf453ee65e93446af
Author: Matt Garnes <matt@cyngn.com>
Date:   Wed Mar 25 16:25:26 2015 -0700

    Fix incorrect ManageApplications options menu order value.
    
    Change-Id: I5c9b7d1ce9e03fa0efe593efd76b4ad2899a126a

commit 4f4630bee458a3b5711ca55dcca057cdc4449600
Author: Shareef Ali <shareefalis@gmail.com>
Date:   Thu Mar 26 14:22:10 2015 -0400

    Setting: LiveDisplay: fix percentage not showing when the dialog shows up.
    
    Change-Id: Ifee1b49eb9c39e6110a7bff19a34b4734f962afd

commit b4c15e41f68f918a3babc69d3ea340659464bbd7
Author: heydabop <heydabop@gmail.com>
Date:   Fri Mar 27 01:18:01 2015 -0500

    Remove duplicate strings
    
    Change-Id: I708c8093cbaf9df734bc9d9d0cff2fa920882af0

commit 640e8fc8085fc416b8fe7e25302e84805894c425
Author: Toha <tohenk@yahoo.com>
Date:   Sat May 10 21:52:23 2014 +0700

    Use actual storage type of sdcard/usb (2/2).
    
    Currently, storage volume description for mount/unmount/format determined at
    build time using PRODUCT_CHARACTERISTICS. For device which has only a sdcard or
    only support usb storage, displayed description is correct. For device which has
    both storage, the displayed description is totally wrong.
    
    Use of actual storage type at runtime can eliminate the needed to specify
    product characteristics, either default or nosdcard.
    
    Change-Id: I9f8d53a4648d960f1009b1fe94787eecd4343427

commit d58f1b5ea7cb59fdb62a2dfa3e30962e0fbf7732
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 24 03:26:17 2015 +0200

    Fix build
    
    Change-Id: I6b7406d5ac2886ec5a5bb3ecbfa8ec414d90bb23

commit 23b678fe5e64e2b67dc096f58e078b9e8059a998
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Mar 29 18:24:36 2015 -0700

    Storage Settings: Allow user to trigger a volume rescan
    
    This change allows to trigger a rescan of a volume with the next restrictions:
    - Internal volumes if they are emulated
    - Primary volumes
    - Non-Removable volumes
    
    Ported from: http://review.cyanogenmod.org/44586
    
    Change-Id: I7e75a324938d8081fd715f702d50f1fdceabd96d
    
    Conflicts:
    	src/com/android/settings/deviceinfo/StorageVolumePreferenceCategory.java

commit 28ba5b126a0e54823af08edd8270628acfc551f1
Author: Adnan <adnan@cyngn.com>
Date:   Wed Mar 18 18:17:34 2015 -0700

    Settings: Change media storage erase strings.
    
      "Erase SD card" doesn't make sense the the user
      when speaking about internal media storage. So distinctly
      state that we're going to delete the internal media storage
    
      JIRA: ALCATELTCL-275
    
    Change-Id: I4b01400d34b321320b8869e163625ddcd23afc9e

commit 5105f9e188470da2f80296cd9770dad5fc487b86
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 01:41:59 2015 -0700

    use CMRemix Center now

project packages/apps/ThemeChooser/
commit 06ead06c28d89211f67587ffc908ac53886feace
Author: d34d <clark@cyngn.com>
Date:   Thu Mar 26 11:37:33 2015 -0700

    Protect app theme from CM11 themes causing crash
    
    If a CM11 theme overlays the theme chooser and changes the parent
    of the AppTheme style to a Holo style, the theme chooser will crash
    due to windowActionBar being set to true in Holo.
    
    Change-Id: I770c82ac66e4f41c88dffbbe0dca0e4a846b0a9c

commit dc9a97feb8d4a2717ec8d79186aa1be71287d0b5
Merge: 5e1a5f4 06ead06
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:33:41 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

commit 21db69f556f08b972de6aa0fad34066d4965afb3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:51:41 2015 +0300

    Automatic translation import
    
    Change-Id: I25a557b8d6137c1f1d1886b3e109ba3551d494d6

commit 7661b2bb2df518b2fb0153520540a7aabe81628b
Merge: dc9a97f 21db69f
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:39:36 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

project packages/apps/UnifiedEmail/
commit 1011e62ae812ef733b8e285aa4f22b4e608986c5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 27 02:24:15 2015 +0200

    Improve strings
    
    Change-Id: I5bd562779fcd3a85a3e03a0432ea0413d26f52a5

commit 4238eba27fddf2d67f34dfc395ecd30e8a508000
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:52:01 2015 +0300

    Automatic translation import
    
    Change-Id: Ia3a6e69a5426464173b71a3b1d917dafdf08695f

commit 225fb227d23031da36bcf8e973f4324701ddaf17
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Mar 29 03:44:57 2015 +0200

    email: fix back button
    
    If conversation_topmost_overlay is not ready to take the focus, if the drawerlayout
    has the focus (this happens always that the drawerlayout is shown in a conversation view)
    then the onBackPressed event never get dispatched to the mail activity, and press
    the back button doesn't have effect.
    Just double check that the conversation_topmost_overlay view can take focus. In case it
    can't take the focus don't response we handled the keyup event.
    
    Also, add a double check over the drawer slide event to prevent burger menu to be displayed
    when the back arrow button should be the one displayed.
    
    Change-Id: I964eb1eb779af13c9b2c07b77049147c2ff1f2d9
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 9a8de2eb5f90fa3cc16799e4951cb48aaa235272
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Mar 29 12:44:02 2015 +0200

    email: fix recents's suggested contacts query
    
    Change-Id: Ibf5e0c426467911644b97c6cc020345e0e297706
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

project packages/inputmethods/LatinIME/
commit 10c614a858cf89f588f615a60f060b485cc75194
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:55:23 2015 +0300

    Automatic translation import
    
    Change-Id: I2465c57be3ee8d916f0d7c3d987ae9539d5f1f01

project packages/providers/DownloadProvider/
commit 1a9da5b6f1390df847c0cbfc7ebdf12292d15e31
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:26 2015 +0300

    Automatic translation import
    
    Change-Id: Ibbc67e28ce7e312fc66deb7b60f9e69716f14524

project packages/providers/ThemesProvider/
commit e989ef7492ce30022d004c9c34f86770078bc164
Author: d34d <clark@cyngn.com>
Date:   Sat Mar 28 12:58:27 2015 -0700

    Fix version upgrades where "holo" may still be used
    
    The stock theme was renamed from holo to system for CM12 but there
    are old upgrades that still need to check for "holo" when updating
    columns in the database.  The name change occurerd in the upgrade
    to version 11, all upgrades before that now explicitly call out
    "holo" instead of "system" to ensure the upgrade process completes
    as expected.
    
    This patch also fixes up the preview generation during the upgrade
    to version 6.
    
    Change-Id: I246d417f10c264c44a1741019589e50b968096e4

project packages/services/Telecomm/
commit 2e18c0609c827738171709a3e40f92eff69df1dd
Merge: 1952939 e556309
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:33:05 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/services/Telephony/
commit 693743e2cc6f440349e3bfa7f5ba5078aa6bc35f
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Mon Mar 23 13:32:29 2015 -0700

    TelephonyService: Don't change preferred network type on multi RAT capable devices.
    
      69efa99f1 introduced setting the preferred network type to 2g on the other
      sim on a DSDS. However, on a CDMA/GSM multisim device, this should be
      avoided.
    
      Thus we introduce ro.ril.multi_rat_capable to discriminate against
      mutli rat capable devices.
    
    Change-Id: I16524a52e0d350a03f48d7d4cb8307fce556979d

commit a680d3eee3892b629cda6556580315a4fb28c886
Merge: dcf9233 693743e
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:33:25 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 89d55c2ab8501860c72dc74fee8c27a7f69422d8
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:32 2015 +0300

    Automatic translation import
    
    Change-Id: Ibca17b4acd084e5f7dc44ef23284117db9a28e82

commit 65ba4b6b0bcb879471978eebb7a5432b2cf2d0c0
Author: Lin Ma <lma@cyngn.com>
Date:   Mon Mar 30 17:38:33 2015 -0700

    TeleService: pass phone ID to APN setting
    
    Change-Id: I3df6c42bc97a68f9e58431e0585a957056912e37

commit 59de23f75e7ae69809989bec7347d652c56415c4
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 30 19:22:44 2015 -0700

    Telephony: KK upgrade path to re-enable components for MSim
    
    Change-Id: Ie21b80d9b6b39ba30fddd6fd268d80cca7f6cb10

commit ae48d903bc93e6e33c3bb28787196e9024aa23e1
Merge: a680d3e 59de23f
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:47:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 2f7296cfed91ef344b89a1934b1316a7e9c10d4f
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 31 13:34:56 2015 -0700

     Telephony: check equality when verifying enabled state
    
    Change-Id: I2dea47a180e30abb0423d8b20395e08d3406bca8

commit 3a7ba60cf236d84131da86af909d7a83bafff148
Merge: ae48d90 2f7296c
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 10:38:38 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/wallpapers/Basic/
commit c0add95c5ee616df31aff1c25ad418c2f3ef6efb
Author: Diogo Ferreira <diogo@underdev.org>
Date:   Sat Mar 28 21:46:52 2015 +0000

    PolarClock: Don't draw on invisible surfaces
    
    This sometimes crashes the device when the activity is recreated
    due to rotation or other reconfigurations.
    
    In some events, namely when the surface visibility changes we
    were drawing a frame which, depending on timing, might end up
    locking/drawing/unlocking a surface that was previously destroyed
    which would crash the app.
    
    Change-Id: I6c4381ce03882658307386a351336894845966e3

project packages/wallpapers/Galaxy4/
commit 8e74e606f57963a980798d0a4674ea9e6854fc34
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:41 2015 +0300

    Automatic translation import
    
    Change-Id: I108e5cfe9f6fc0da0930c60c49b5a80368362faa

project packages/wallpapers/PhaseBeam/
commit 4d56991c85404c994a5273bdb6daed5d178921c7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:47 2015 +0300

    Automatic translation import
    
    Change-Id: If1a3c8cacaff9d9df8eee74cb594e0411290a849

project packages/wallpapers/PhotoPhase/
commit 01d8ba8d4cebe245a19e301d64352f7be3843238
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:53 2015 +0300

    Automatic translation import
    
    Change-Id: I787229f334517816307e7371d82a8e5d2a1e437a

project prebuilts/gcc/linux-x86/arm/arm-eabi-4.9/
commit 85604217db8cf297d4f9780f00ca8717cce96de6
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Mar 17 13:54:49 2015 -0600

    03-17-15
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit c8aaabad93195db5a5944ed2b18c6f680203d0b0
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Mar 21 22:06:08 2015 -0600

    03-21-15
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

project system/core/
commit 4b1cefed923c7bff8ca3a4d7c9e55b06879fa4e2
Merge: 7466283 92d5ea9
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:25:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project vendor/cm/
commit 2ca5d3999b35d328f0969a264009bffe0faf889d
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 27 11:42:11 2015 -0700

    vendor: add sepolicy entry for killswitch service
    
    Change-Id: Ib3c44c50138f5715d92addbf8df7ed591785b550
    Signed-off-by: Roman Birg <roman@cyngn.com>

project vendor/cmremix/
commit ca43c5fd3596c7a28e4e58c24449ef30c16c2e67
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 28 23:18:49 2015 -0700

    update sabermod.mk

commit 593522ec3b88076f6b1f0da1f60f7df4db234bd6
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 00:14:12 2015 -0700

    cm-12.1 Use SM GCC 4.9 to build

commit 5748ee85bdec51b25eec21a123277ecd11cd3071
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 11:49:47 2015 -0700

    fixed sm.mk

commit 3aa692a82cbc6ff9d3b6c61ceff264512f088053
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:40:36 2015 -0700

    change CMRemix version

commit 3ec5bc424a847da8547e50f734d918ce485e1a05
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 30 01:08:25 2015 -0700

    TARGET_NDK_VERSION := 4.9

commit e96c58201b0a25e9dcdd800c1061fe8b6db9cc21
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 04:04:49 2015 -0700

    update ota version

project vendor/samsung/
commit e9fb886f2f23701c9e3e0b55343fc3da1c66ac7e
Merge: cb8d668 9024b30
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Fri Mar 27 08:44:39 2015 -0500

    Merge pull request #602 from sbrissen/cm-12.0
    
    KK ril update for p4notelte and t0lte
