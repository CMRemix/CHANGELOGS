
project bootable/recovery/
commit 471eb4e140b36c9a6092c70bf4e286961b1378e3
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Thu Mar 26 14:11:04 2015 -0700

    update-binary: support reboot_now on older recoveries
    
    Attempt to reboot using older methods in case the recovery that we
    are updating does not support init reboots
    
    Change-Id: I9d6ec23c65291221e99d67b2361a2bd150319eee

project build/
commit ee869c36d4737173427c46427a07a599ed1befa2
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Dec 12 23:06:47 2014 -0700

    cmRemiX Version

commit f07fba533f4acc67d091bc110cac9f8cae12fe0e
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 23:06:47 2014 -0700

    Introduce New Squisher/Opticharger for Lollipop (2/2)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    Change-Id: I02b41274179cdc1793794fb11780ea60774e6e41

commit 3f682239fe439d8dec4991c426edb1a4b5db7f62
Author: root <xyyx@mail.ru>
Date:   Fri Dec 12 23:06:47 2014 -0700

    Do not use mkf2fsuserimg.sh if we have two fs in fstab, for example:
    
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          ext4    noatime,nosuid,nodev,barrier=1,data=ordered                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           ext4    noatime,nosuid,nodev,barrier=1,data=ordered,noauto_da_alloc     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt

commit faabba3596d1e74aef33e4bb13f6cf20686a71bf
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

commit 489b78c3f3973174d8c3f48a2fab6c70a88c9763
Author: Ayysir <ayysir@aospal.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    Prebuilt chromium: Run a check for target device directory
    
    This should fix the issue that arises if device fails
    and device is built again, chromium will error out because it thinks
    the prebuilt files exist (which they are not, directories are just created).
    
    Signed-off-by: Ayysir <ayysir@aospal.com>
    Change-Id: I595cab268e66c738ccae9900150b36d7f9626a6e

commit e0f889a07e183123cb45a27b98e590cdcc1af938
Author: rooque <victor.rooque@gmail.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    build: Fix PreBuilt Chromium refs

commit f5d611fac3a1a6a3050cf0ee23d05ac9cd040d71
Author: JoseGalRe <josegalre@gmail.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    build: change style console output of prebuilt chromium
    
    Change-Id: I2c390f3c64d614e181ebcad4e9711a93d9c55d44

commit ea98e8eaa18ef72ed86126275c47cdd55c77f820
Author: mar-v-in <github@rvin.mooo.com>
Date:   Sun Dec 21 22:13:45 2014 -0700

    JDK8: JDK check should succeed with OpenJDK 8
    
    Change-Id: I1c1eaff7fa36bba2db261e0c5311bbc6d005a726

commit 5965b9a5ea6de53fcccf8cd286e62f7c68d1034e
Author: JoseGalRe <josegalre@gmail.com>
Date:   Thu Dec 25 16:21:52 2014 -0700

    build: Show more hardware information about the device [3/3]

commit a27bb09d3e3efc6f2f56bcffcbc675818b4fa8cd
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Thu Dec 25 16:21:52 2014 -0700

    build: Do not remove recovery resources, so TWRP can build

commit 57dffb1f3fedca08664c06ba192d1ea9d5c67c59
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Remove recovery resources for cwm
    
    Revert this, https://github.com/PAC-man/android_build/commit/cab57f994fe0c7c53853411eaa3575aa6b3ef8d7
    
    Change-Id: Ica036525b768f6e416b103ba60bc26d58f2e02e2
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit 9576751871d295bc0ab4362e61e7ffa9ff647f55
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    core/config.mk: Add SED_INPLACE
    
    Change-Id: I5fdff25e5c1d4861b3a1f9e208c6d0fa5d415115

commit 3784fdd5b02eb8d3e41c161eb846f99c559bfe8d
Author: Bjorn Hutmacher <bjorn.hutmacher@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    core: Set ro.adb.secure=0 for recovery default.prop
    
    Change-Id: I71384795580ae6650bf543128798ee312f74e0a2

commit 43eb293c604fa24bb04005ce252fbf64251550ca
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

commit 1f1bffaf0ea5636d62c97fa52971eedcedcaf21c
Author: William Casey SEdlacek <w@sedlaceks.org>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Block Building

commit 5d091b34037f454fe972e980d103c50248cec211
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Add a Whole bunch of Clean Options

commit 247b761851883b021784503dc6882e0ab7bb7142
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 14:14:32 2014 -0500

    Add Make Dirty Option
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 73667c3845dfb317694ca2d1c9c9788a08702681
Author: deadman96385 <seanhoyt963@gmail.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    Kill some log spam
    
    Thanks to @Cl3Kener for taking lots of his precious time to help me find these things that were driving me up the wall.  I should have authored this commit as him but I didn't.  Sorry buddy maybe next time....
    
    Change-Id: I8d6cd504afe83954964f71eb7d8f802624d2e595
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 4e5993ebed6d66674091b40514aeedee0af05093
Author: MrBaNkS <banksmi09@gmail.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    build: remove all stops if using different make/openjdk-java version
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 07e90f3dc7d239324fe711cd7edbf0336edb369a
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

commit ff05e1a7720cf41708bde2ea73f43fe093c83e4a
Author: Elliott Hughes <enh@google.com>
Date:   Wed Dec 31 19:44:19 2014 -0500

    Remove libdvm dex preopt support.
    
    libdvm is dead.
    
    Change-Id: Ib8571c007f8a9f0e0eaf5c61b5d2e416b2d95089
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit d875c8eab87552602c1df2d007b5a23ca12fdb69)
    
    (cherry picked from commit d875c8eab87552602c1df2d007b5a23ca12fdb69)

commit 8583c9b3f00943d7f714852239391d6828b79ea2
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

commit e030045dd0589cdc45db8d41f732ed13ae48cd88
Author: David 'Digit' Turner <digit@google.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Update host linux toolchain to gcc 4.8
    
    This patch ensures the build system uses the prebuilt gcc-4.8 toolchain
    when building host Linux binaries, instead of the gcc-4.6 one.
    
    Change-Id: I7b449650714ba4314a780827e0243f2af40ec82c
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3a371706b41edccc0e4a97e09920c1b663b17a1b)
    
    (cherry picked from commit 3a371706b41edccc0e4a97e09920c1b663b17a1b)

commit 7ca167436289b4256cf56edabfd7e7a3bf7f7c7d
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Add Toolchain Version to Lunch Menu
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b8d1f8e56a135943175384e9719e7bfb59733dbb)
    
    (cherry picked from commit b8d1f8e56a135943175384e9719e7bfb59733dbb)

commit 33188c35bd3d870649abc84d81d3a77e69ca5b02
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Use New 4.8 Host Toolchain from Google
    
    * While we are fixing SM Host Toolchains let's use the latest Google.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3885177ff3cdcc3374944be6d9fe984e5d999291)
    
    (cherry picked from commit 3885177ff3cdcc3374944be6d9fe984e5d999291)

commit c32af1da2cfe94a592b726bfb360d8702926757c
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Add graphite flags
    
    Change-Id: I90bd416e800936b2130b82246fe0fd047774d466
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit f604a52efdb79fca5506fcd3e9c4c80799bdbb33)
    
    (cherry picked from commit f604a52efdb79fca5506fcd3e9c4c80799bdbb33)

commit cbf1ba804dba8af6f23395293431df7b32c25a92
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 17:12:51 2015 -0700

    Remove 2nd cpu nonsense
    
    * Not like I'll ever use it
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b5b4b58f4596c83e1f40b7d8a2e060c90f1dc7e3)
    
    (cherry picked from commit b5b4b58f4596c83e1f40b7d8a2e060c90f1dc7e3)

commit 9ca5fa0192f7812586869849fbf9854fd0e3d0bc
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

commit d6a38b747c1bf10ae575441ae0743f439b171265
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Dec 13 09:37:17 2014 -0500

    Cleanup armv7a neon
    
    * Why don't we have cortex-a9 option and why is the fix cortex a8 being applied to all?
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 6a513af74a4a3bb8f94ab9d8d1987b94fb7e86e0)
    
    (cherry picked from commit 6a513af74a4a3bb8f94ab9d8d1987b94fb7e86e0)

commit d10519e16dd647ee7dd1ea5fb1a848313114dfc3
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Mon Dec 15 23:08:47 2014 -0700

    Update modular:  add strict-aliasing and make flags default instead of using a string
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 8ced76a5bdd6cd38ce6845a8bf303986cfa4a9fd)
    
    (cherry picked from commit 8ced76a5bdd6cd38ce6845a8bf303986cfa4a9fd)

commit 39cf04e4ac3d07e786d2a0e5f60e878076fcbbb0
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Dec 24 09:44:17 2014 -0500

    Update Graphite and Strict Aliasing
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 15a343e2ef029a83ca8feebad9c5a42952a0621a)
    
    (cherry picked from commit 15a343e2ef029a83ca8feebad9c5a42952a0621a)

commit 0308e1e8965614099dc8ff9ebad120ec34399e99
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 24 12:59:31 2014 -0500

    Initial Disable Strict Option
    
    * Still will need lots of work.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit a1430dba729cd13e6e7a04d2b00c60d929979bd0)
    
    (cherry picked from commit a1430dba729cd13e6e7a04d2b00c60d929979bd0)

commit 9f1baa13a22bf27272cedb6246fd58422f593411
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 24 16:45:55 2014 -0500

    Updates/Fixes for modular graphite/strict implementation
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 0d5703ef3aa4632ff8a638b42da053055b14f475)
    
    (cherry picked from commit 0d5703ef3aa4632ff8a638b42da053055b14f475)

commit 0a1811484652da3fc0ea343a977bc645941d9f2a
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 18:28:43 2014 -0500

    Use Universal True instead of Yes
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 64d3fe317204e1ba769c4ac39eda93ea613f0d58)
    
    (cherry picked from commit 64d3fe317204e1ba769c4ac39eda93ea613f0d58)

commit 31796902300116b8d6441dfd87d6ac43b6c5fd06
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 19:14:21 2014 -0500

    Introduce USE_HOST_4_8 Flag
    
    * This will enable Host 4.6 by default for devices that can't handle Host 4.8
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    True not yes
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 659f1389ba8500794324fd705fb2c8a7b8847533)
    
    (cherry picked from commit 659f1389ba8500794324fd705fb2c8a7b8847533)

commit 010eee810d0ab2f06661459d6c1121b52c8d24f0
Author: Anthony King <anthonydking@gmail.com>
Date:   Thu Nov 6 20:34:13 2014 +0000

    WIP: clang supports cortex-a15 now
    
    Change-Id: I9872db2237c513f135df32c5147e47edf6eba49f
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 442dbe42044641f457b45930230c342ce1728281)
    
    (cherry picked from commit 442dbe42044641f457b45930230c342ce1728281)

commit f0ef0a3a21d7957e8ac64e62195def12dcfecd1a
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 26 19:44:02 2014 -0500

    Update Strict.mk with more violations
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit f0f90132858e72ae4ffa2f24c9fade2748c85797)
    
    (cherry picked from commit f0f90132858e72ae4ffa2f24c9fade2748c85797)

commit 79bffe3680e091a329b965c2e52e3da180418127
Author: Jake Weinstein <xboxfanj@msn.com>
Date:   Mon Dec 22 13:01:03 2014 -0500

    build: clang: use swift and VFP4 flags for krait
    
    Change-Id: I4c22d6d7d8d2dcf5de26ba3061bba58c74eaf93c
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 860fcc499f91a9644cccfb3de7b3b37570bad379)
    
    (cherry picked from commit 860fcc499f91a9644cccfb3de7b3b37570bad379)

commit fad7fc98f7c0c7b598ca4b7b72167f46530d8354
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Dec 27 02:20:48 2014 -0500

    TWRP Strict Aliasing Violations
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b1ec348c6d50c8652002cc896fccc02477313be7)
    
    (cherry picked from commit b1ec348c6d50c8652002cc896fccc02477313be7)

commit 17b92ede1ef6889a7e10504f503586607d750191
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Dec 27 03:21:14 2014 -0700

    strict-aliasing: Fix warning levels for clang or not clang
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit ff049aa0fb7b40556ad48618eadd01663cbb76af)
    
    (cherry picked from commit ff049aa0fb7b40556ad48618eadd01663cbb76af)

commit cac4c979df46b4466cb6534a109dc5d2b806e9b7
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Dec 27 18:15:49 2014 -0700

    strict-aliasing:  update module list
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 00ba0c7d0e09258eb4026a58f90721d641a9c450)
    
    (cherry picked from commit 00ba0c7d0e09258eb4026a58f90721d641a9c450)

commit 08f2dfc2ce7b006dc736dc70bc76fc71c7a0dfa9
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

commit 2b7917356a03d8932f8c5d4fd6a2c32f6faf0013
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 16:46:13 2014 -0500

    Attempt to tune for Krait Modularly
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit ce30849f0c936fa9606062334bbc79eb627b4185)
    
    (cherry picked from commit ce30849f0c936fa9606062334bbc79eb627b4185)

commit 4c21001765dbe8af66fd02d44906526a1585033c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:39:14 2014 -0500

    Return some GCCONLY flags used in Kitkat
    
    * and keep them away from clang too!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3fe59b017364f110fdf226e02f1790fc2772d0ea)
    
    (cherry picked from commit 3fe59b017364f110fdf226e02f1790fc2772d0ea)

commit cfcdad7aa3aeed10cba3615aa6d8f64820ab2263
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:52:16 2014 -0500

    Keep Krait Tunings off the Host Modules
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 0e2c474b8d599ca911f6d8ce2f04ca3933bfa2fb)
    
    (cherry picked from commit 0e2c474b8d599ca911f6d8ce2f04ca3933bfa2fb)

commit d99ddeeeda45f629917b722ed138d78957bc2d7c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:55:05 2014 -0500

    -mvectorize-with-neon-quad not supported by clang
    
    * Will move to GCCONLY
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit dc4fcef6055be0b532b468c997c20c68044606e5)
    
    (cherry picked from commit dc4fcef6055be0b532b468c997c20c68044606e5)

commit 1bc70c805d8c651a2af7723aa2f7f5a2157cb444
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Dec 30 23:56:23 2014 -0500

    GCCONLY: Add -mvectorize-with-neon-quad
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit b72cdd79ea283f4f5accc296add6677277ef0031)
    
    (cherry picked from commit b72cdd79ea283f4f5accc296add6677277ef0031)

commit 2660d082df10af4efef63168a4d5d795dc9402ff
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 01:43:49 2014 -0500

    Update the Krait Ignore List
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 72b10173b9b3810f8d039cafe2754e66b90eaf39)
    
    (cherry picked from commit 72b10173b9b3810f8d039cafe2754e66b90eaf39)

commit 9fb18469b5451b3dda0d0eeb7054661e027f8255
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 08:34:23 2014 -0500

    Bluetooth: The Most poorly written code in Android
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit df207552867bbeae8f31618ec36738851d27f371)
    
    (cherry picked from commit df207552867bbeae8f31618ec36738851d27f371)

commit 3b2e9801ac86817fcefa3f6addacf28beb0bfd2f
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 13:10:43 2014 -0500

    armv7-a-neon: Apply Correct mfpu and mfloat tunings per arch
    
    * Before everything was neon and soft float.  Now let's allow for per cortex tuning. Benchmarks should go up.  See here for better references https://github.com/CyanogenMod/android_build/commit/8907b775376211e73a566e8c9ef65e5b76cba1af
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit e63fba92b06f8833a4d57ef52c00dfa7ffcadc32)
    
    (cherry picked from commit e63fba92b06f8833a4d57ef52c00dfa7ffcadc32)

commit df6fa73753e781a25fe22965fe1b229ec627c8f2
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 2 21:57:00 2015 -0500

    Remove webview related files from -O3 and GCC Only Optimizations
    
    This causes FCs on some applications.  I haven't experienced it but it makes no sense to really make these files larger anyways.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit a28f8e66579ec22528a578d1df844da2b489792e)
    
    (cherry picked from commit a28f8e66579ec22528a578d1df844da2b489792e)

commit 285f036103d59d61e2e33432794f910f33ec470c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Dec 31 13:45:17 2014 -0500

    Clang doesn't support -mfpu=neon-vfpv4
    
    * Which is unfortunate.  I would be much better if I didn't have to hack this crap
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 6ee82e88fa5b7302d2b9984bc93168aca1749b90)
    
    (cherry picked from commit 6ee82e88fa5b7302d2b9984bc93168aca1749b90)

commit e6c11f5e4038908db15a8ce703b75be7a8752705
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sat Jan 3 00:01:31 2015 -0500

    libwebviewchromium: Haters Gonna Hate
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 48eb1ecbb5d1d97c508eb7e285e375bbb8824fcb)
    
    (cherry picked from commit 48eb1ecbb5d1d97c508eb7e285e375bbb8824fcb)

commit a5ef1240a17d3ee00777136b5def8a30fde0564e
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Jan 14 18:45:00 2015 -0500

    Order Matters
    
    Put Graphite last since it will help optimize code size after -O3 and all of the other stuff.  Credits @pbeeler.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 29d6c5d482fc27c81d0184a93795d6706a97cf0f)
    
    (cherry picked from commit 29d6c5d482fc27c81d0184a93795d6706a97cf0f)

commit 13e8542bf93c45dc996e9d06822347d91de02eae
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Jan 14 18:49:14 2015 -0500

    Update Copyright Year to 2015
    
    * New year!!!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 9e39753fd61c1d9f0d2a73186a8bb1d475425629)
    
    (cherry picked from commit 9e39753fd61c1d9f0d2a73186a8bb1d475425629)

commit 951244b682496faa9176f50ad697a2ea68d36e6c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 13:49:30 2015 -0500

    Missing Separator
    
    * Must have missed it in rebase... :/
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c42a61a5edd6d9adebb5ed25471c8ff50c33d954)
    
    (cherry picked from commit c42a61a5edd6d9adebb5ed25471c8ff50c33d954)

commit 2b0119cd96fdf801ea0470ac02f61bf517b09c1b
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 14:10:29 2015 -0500

    O3: Ignore Annoying warnings that crop up with -O3
    
    * These are warnings, not errors! Please don't stop my build!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c89528ad587b3eefddb1656623c4e1c95ca8167e)
    
    (cherry picked from commit c89528ad587b3eefddb1656623c4e1c95ca8167e)

commit 3b61645241e208d671f4a635b184d97b04fb9965
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 16 20:23:13 2015 -0500

    Update graphite again
    
    Seems the order change in the binary file caused a two more graphite errors which we fix here
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 878e16fce0084d7a4239d8cbc1482d7f09a9b9dc)
    
    (cherry picked from commit 878e16fce0084d7a4239d8cbc1482d7f09a9b9dc)

commit 89bfe0b187368909335b51835bccc3503b1f65d9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Jan 18 07:15:52 2015 -0500

    Introduce Modular TARGET_USE_PIPE
    
    * Allow for -pipe to be used. This flag actually has no effect on the generated code, but it makes the compilation process faster. It tells the compiler to use pipes instead of temporary files during the different stages of compilation, which uses more memory. On systems with low memory, GCC might get killed. In that case, do not use this flag.
    
    * From my personal experience, compilation time was ~5 minutes less using pipes on a "make -j8" build on my personal computer.  Times may improvement more when doing like a make -j16 or -j24 on a build server with lots of RAM. Also note that this may not speed things up on a SSD hard drive due to the faster write speeds, I only tested this on a regular hard drive.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit c5e99ee9ca8edcfa0055c66cb5f3a22c8220fe4c)
    
    (cherry picked from commit c5e99ee9ca8edcfa0055c66cb5f3a22c8220fe4c)

commit 12ddd63ba1534bf44d6f69da1a3a4fa4fd578840
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 17:40:33 2015 -0700

    Shrink the codes

commit 477599413928550204d659c3dd68edbca101b954
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

commit e28f4d6a43bdc1e243f4a3b6c57c5cbdbdff7734
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 18:22:07 2015 -0700

    build: show info of all Optimization features being used

commit 980e063001d5fcf538734f8d523daaf2fa490191
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 18:47:52 2015 -0700

    dumpvar: fixed sabermod kernel version

commit e9de012daaa58cdec3989639c2d0e5b804fad12a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 19:19:34 2015 -0700

    strict : disabled more module for cmRemiX Rom

commit f41fb071084e7fb48a5a6dbacc9773b48db778a2
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 20:08:40 2015 -0700

    graphite: one more module for new SM 1-14-2015

commit abdc0283deb7e013d116ce5bc5201590f0a90299
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 18 20:17:17 2015 -0700

    Introduce Modular Link Time Optimization
    This is the codes from @MWisbest, Get the idea to
    for modular from Chet Kener & Pbeeler

commit a9112d55560fad9a412149561bbb9c92bbaa5faa
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Mon Jan 19 11:50:28 2015 -0500

    Introduce FLOOP_NEST_OPTIMIZE
    
    For more info with regards to how this works see http://en.wikipedia.org/wiki/Loop_nest_optimization
    
    It's highly aggressive so you'll notice I had to disable several dozen modules.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 548561d867e8bc8b1dc70be0c1144050f968c09b
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Jan 19 12:01:40 2015 -0700

    dumpvar: add FLOOP_NEST_OPTIMIZE info

commit 4319470d8477b309e493c9cb2758f1a2077cd18a
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

commit fd0a966af64777e1def365290d00141cde2802c2
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Jan 24 01:40:34 2015 -0700

    various fixed and update

commit c3cfa89ed2d8d4d9e8345d05e9c6898aaa09a96a
Author: johnnyslt <ionut.darescu@gmail.com>
Date:   Sat Jan 24 20:53:54 2015 -0700

    Add changelog generator (2/2)
    
    How to use :
    
    two methods
    
    1.- export CMREMIX_CHANGELOG=true
    
    2.- add flag CMREMIX_CHANGELOG=true in BoardConfig.mk or BoardConfigCommon.mk
    
    Ported by @cristianomatos and verified by @alviteri
    
    (cherry picked from commit 1785e3196939a468b61431bc4c67b31673bef30b)

commit 1e77c6eaf5bce150af8d0dca0902970acdb12996
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

commit 168bc8ba542ecab7fe337d8752eff1cc56d31188
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:17:28 2015 -0700

    Move flags and disable modules lists out of build (1/2)
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    (cherry picked from commit 6f45ca92e1fa15e39eee76a1c35aa7e6863c4fb7)
    
    Conflicts:
    	core/O3.mk
    	core/graphite.mk

commit 781cfb8b6fbafb3585177753b377bbeae6590077
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:17:28 2015 -0700

    Have -O3 skip when thumb is used to reduce code size. (1/2)
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 3617505a97f07888ed3698b1880d7b8854669169)
    
    (cherry picked from commit 3617505a97f07888ed3698b1880d7b8854669169)

commit 6c585e66749daeec4e03b8a633ba56b11998b4d8
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:20:06 2015 -0700

    arm neon:  Pass arch variant cflags to the kernel.
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    (cherry picked from commit 05a3f4d9446a759f21f482f4bb101eda0f18bf95)
    
    Conflicts:
    	core/combo/arch/arm/armv7-a-neon.mk

commit d3d1b5fc17bab7b8283343bda20f7ca9dc5b69d7
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 25 17:20:06 2015 -0700

    O3: Only filter arm: Only arm uses thumb.
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit f12f0fb482656e892add0b03e1d5248dcbf4db34)
    
    (cherry picked from commit f12f0fb482656e892add0b03e1d5248dcbf4db34)

commit ab43d82db3bea8cfb6e02e2edb6c411a25875f4b
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 25 18:03:25 2015 -0700

    Move Strict flags and disable modules lists out of build (1/2)

commit a0ae4d3bc25c72b4568a528a2430d531913a5164
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Jan 25 22:59:14 2015 -0700

    add and removed various optimzization settings

commit ddb00a01b058d82865d651260d86b96f71231b5a
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Jan 26 22:52:13 2015 -0700

    kernel: Add custom toolchain for kernel build again after rebase
    
    example: TARGET_GCC_VERSION_ARM := 4.9

commit 95c13339840d1188ac8e15f292165fb8d9c90963
Author: SferaDev <sferadev@gmail.com>
Date:   Mon Jan 26 22:52:13 2015 -0700

    Don't stop if JDK version doesn't match
    
    Change-Id: I5e77c70724c7d81544673715ed09e0a53ce32730
    
    (cherry picked from commit 1cbdadbfeae0321b1cd9859cd2ed2572b5fdc39b)

commit 12d39baf30135271382ea7e8a6feb6c241c824a1
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    build: change O3 OPTIMIZATIONS

commit 2b6101e5af77f4cc8cb6b20ea498768d23abcc2e
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    Fix annoying issue with clang not understanding -mfpu=neon-vfpv4
    
    Credits to @Cl3Kener
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 5b4267469a9d4c2e183c07157928b4bcf203a72a)
    
    (cherry picked from commit 5b4267469a9d4c2e183c07157928b4bcf203a72a)
    
    (cherry picked from commit 235ff9aa3b0302d04aab3e4d52248e91e21a16a3)
    
    (cherry picked from commit 235ff9aa3b0302d04aab3e4d52248e91e21a16a3)

commit 9da37f36471c7346a8309aad3f8d88313e8e732c
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

commit 580722e38e965fd1196b1d08a2acb2da359c21a3
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 01:15:58 2015 -0700

    arm neon: denver:
    
    use -march=armv8-a instead of -mcpu=cortex-a15
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit 01ca9fac721f54ab5634ac643c817c18103e19b8)
    
    (cherry picked from commit 01ca9fac721f54ab5634ac643c817c18103e19b8)
    
    (cherry picked from commit 67af787a69fb429704f3fca6cc0f8e41f4cfb933)
    
    (cherry picked from commit 67af787a69fb429704f3fca6cc0f8e41f4cfb933)

commit c92fc504cb8ccfd03db66d5b3a271d6b09867459
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Jan 27 03:06:04 2015 -0700

    arm neon: unbreak
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Unbreak #2
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    (cherry picked from commit ce439710eddfd2c5130f117380afd3d4a5aa93de)
    
    (cherry picked from commit ce439710eddfd2c5130f117380afd3d4a5aa93de)

commit 35b0dcb031663f23b4867909ca643ba56a23a987
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Jan 28 00:12:50 2015 -0700

    build: instroduce GNU11 Modular (Pbeeler) and fixed LTO

commit 401dbbe076eb008974f6a46660200b2f91a58a89
Author: David Viteri <davidteri91@gmail.com>
Date:   Wed Feb 4 22:37:39 2015 -0700

    Build: Changelog (3/3)
    
    Thanks David (crDroid Andrroid)
    Conflicts:
    	core/Makefile

commit 835c76f7cba86be9e910ab0797e2014c1b3eb776
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

commit 602270f5243b7a85ea5b41d88781c1501612cc88
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

commit 977ce36a34e75dbbe56934ffb3abd373ad062d09
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Feb 4 23:06:14 2015 -0500

    gcconly: Change -floop-nest-optimize to enable by module
    
    * This optimization is super aggressive and causes play store crashes.  I want to focus on the most important modules first (bionic/art) and see if I can at least get those without breaking anything (like the Play store crashes we were experiencing before)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 85976f03db36776c2a591d8bb54cf3fdfa45db29)
    
    (cherry picked from commit 85976f03db36776c2a591d8bb54cf3fdfa45db29)
    
    (cherry picked from commit 2223c25aba286615b130a297836491061334808f)
    
    (cherry picked from commit 2223c25aba286615b130a297836491061334808f)

commit 535bc11b63d5d2b148565e9c446193b41ed1c12b
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Feb 4 23:19:45 2015 -0500

    List Art Modules in nest optimization
    
    * Let's try art first
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 29a1852c15d96d58ff52a25ad673523d5fd58e25)
    
    (cherry picked from commit 29a1852c15d96d58ff52a25ad673523d5fd58e25)
    
    (cherry picked from commit e66e53b1b7ee0411174677bedcb1ef50f019f738)
    
    (cherry picked from commit e66e53b1b7ee0411174677bedcb1ef50f019f738)

commit 21512ba10e054dc9339027cb5d3c6b85b3325d59
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Feb 5 00:53:13 2015 -0500

    Add Bionic to Nest Optimization List
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 9b44f2bed6782c82ff4979c629e146602cd17876)
    
    (cherry picked from commit 9b44f2bed6782c82ff4979c629e146602cd17876)
    
    (cherry picked from commit 5b46ee4212fdfb4a870f57b5aa89090b8bb3eb18)
    
    (cherry picked from commit 5b46ee4212fdfb4a870f57b5aa89090b8bb3eb18)

commit 4b0b506227e21c080052f7bd0a3ac07cc62e6f4b
Author: arter97 <qkrwngud825@gmail.com>
Date:   Fri Feb 6 19:30:35 2015 -0700

    arm: add support for BoardConfig to append CFLAG
    Defining BOARD_GLOBAL_CFLAGS from BoardConfig will add a global CFLAG to be used with the entire ROM compilation
    
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit a05769a8fda53c27b20399187f4fa35b053d00b6
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Feb 7 20:52:54 2015 -0700

    no need this settings

commit d07135b108831b39a5d6aff9b5da63ea8e00ac4a
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 12 21:01:29 2015 -0700

    Revert: Do not use mkf2fsuserimg.sh if we have two fs in fstab, for example:
    
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          ext4    noatime,nosuid,nodev,barrier=1,data=ordered                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/cache        /cache          f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2                     wait,check
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           ext4    noatime,nosuid,nodev,barrier=1,data=ordered,noauto_da_alloc     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt
    /dev/block/platform/msm_sdcc.1/by-name/userdata     /data           f2fs    flush_merge,noatime,background_gc=off,inline_xattr,active_logs=2     wait,check,encryptable=/dev/block/platform/msm_sdcc.1/by-name/encrypt (reverted from commit 232b0c465eb098e47bdf16bc48fd9cb7a570bb6d)

commit 220790aba30a70e6878ac59730b8bd54a6f56957
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Fri Feb 20 13:13:37 2015 -0800

    Revert "build: Handle custom boot images properly"
    
    We don't want to force this since we need to be able to
    re-sign boot images with proper keys, which requires rebuilding
    of the images.
    
    This also has an error in it from merging (dropped _MK).
    
    This reverts commit 22913dea82299eac7e1a5e754102b89af4796a0d.
    
    Change-Id: Id1353e9883c3f24bbc10e685f43bede779430025

commit 92b88ee03cdf13455150f208f90c3c7cd6706174
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Mon Feb 23 00:38:24 2015 +0000

    Revert "Revert "build: Handle custom boot images properly""
    
    This is still needed, per this discussion here:
    http://review.cyanogenmod.org/#/c/76919/
    
    This reverts commit 78d216bc157021e111a31a6606622cef4b9d383d.
    
    Change-Id: If494c2c6468185bc0e10cdb92847a9f8429b79c4

commit a20b772154516b9c3c25c1747711c8e98df1ab98
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

commit 47fde8f8a9d1a604461316b6b303770c6e1f8a95
Author: kantjer <kantjer@gmail.com>
Date:   Mon Feb 23 00:43:04 2015 -0700

    Add ro.cmremix.model for OTA purposes
    
    Change-Id: I5d4baf0548e098d629e900580758a6d582d3cc2b
    
    Conflicts:
    	tools/buildinfo.sh

commit fd97499bd0d1f1e4a5b84e68662dc09dbd0eb606
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Sat Dec 6 12:44:40 2014 +0100

    updater-script: Format system before installing ROM
    
    Change-Id: Ib266d6c1bde64a028a4d06bca40c5c1a1431edd0

commit 99a717a3e358a301812463bea9028fe8c56a5e32
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

commit 60afa6d83dce599a246a2d5a63ff4d11f6b5ca4b
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Feb 25 02:00:33 2015 -0700

    Add Global posix thread aka pthread Support (1/2)
    
    this flag enables multithread support much like what I did in kitkat.
    
    https://github.com/SaberMod/android_build-OLD/commit/93d376380dffae1ec96eeb0ef00a7e663d107ca4
    
    Change-Id: Id5559ec460b2ba84ed9cfe7a47b0ac59544e1d61
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 44279661e64f622f0e292d68e79aa5c8e39a67cd
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Feb 25 02:16:32 2015 -0700

    build: add pthread to dumvar build info

commit 5a831c65c745e0438477bff584d53185fcbc5987
Author: fattire <f4ttire@gmail.com>
Date:   Mon Feb 16 01:19:08 2015 -0500

    repopick: Always expand paths to the repo executable.
    
    Change-Id: I4e89a530f98e3a28973c57adaf9046e9c21f1290

commit 19f9daa58b87f379bcc6b5e08554479ad3d5c017
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 11:22:32 2015 -0500

    Mock Location should be off!
    
    * Unless you don't want people to know your exact location.  Users can try it then if they like
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit b198e7c8034cc0ebff085e6d445a216618ab65ef
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:32:21 2015 -0500

    Do Not Odex Eng Builds
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 4a3cdfd0305b45a158a128fc514fbe9a42f0384b
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:40:46 2015 -0500

    Do not build test stuff for eng builds
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 0277627e4e5b7dcd5ff0e9b7725482e2bdb29b9c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 10:42:26 2015 -0500

    Remove Debug from Eng
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit c375907bd54daaf9a8d6dec360e63686a4d0a7a7
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 11:16:04 2015 -0500

    Remove ro.kernel.android.checkjni
    
    * JNI, the Java Native Interface, provides a way for code written in the Java programming language interact with native (C/C++) code. The extended JNI checks will cause the system to run more slowly, but they can spot a variety of nasty bugs before they have a chance to cause problems.
    
    * Forget the bugs I don't ever want to see OptiPop run slowly
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 4c86cf4ea63dd4aac66e6eb9fd984fa51bd896af
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Jan 23 12:34:14 2015 -0500

    Eng: Include in user build filter
    
    * Let's make eng builds similar to user builds.  (but with some of the eng build perks as well)
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 5c5394dbc0e8b565c31fbcfaf3c16fc587881af9
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Feb 26 11:27:41 2015 -0700

    armv7-a: More Specific Tunings per CPU
    
    * Also add some substitutions and ignores for clang.
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Conflicts:
    	core/clang/arm.mk
    	core/combo/arch/arm/armv7-a-neon.mk

commit 81826b11ce21d1f92fdee716b65fb78312127bf8
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Sun Nov 16 17:52:59 2014 -0500

    Do Not Build Recovery Or Use it
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 515b15fb5429bde5fdf341cbaa78ca70d29cf8e5
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Nov 12 22:34:31 2014 -0500

    Lollipop Audio Only
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Hangover Derp
    
    * You should try it sometime
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 693de6308aa6093638bbaf3ef1f90e7f4184f86b
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 23:07:28 2014 -0500

    Remove Annoying Goldfish Stuff
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit ecc14c4c3674526a51e9ebfe418b3f066c7acfbd
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:34:10 2014 -0500

    Build Stk and CellBroadcastReceiver
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 961df10a8b25465b1a92d298250074a5c826b5f4
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:33:02 2014 -0500

    Build Launcher3 instead of 2
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 254ff04933a363fe33e0fec09651a7bddd31a151
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:27:57 2014 -0500

    Allow Prebuilt APKs
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit b8672bffd2aaed89a3675d193af8de016cf7c1ca
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:25:00 2014 -0500

    Do Not Build QuickSearchBox
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 7ac26163a0ed642760212c095a5a0a16dfe4f87f
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Tue Nov 4 21:28:48 2014 -0500

    Unsecure
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 0082877d10f7b8a93822f2f462d1e4bbe24a3409
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Thu Nov 6 07:45:15 2014 -0500

    Remove Default Combos
    
    * I never use these
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit e82b3270d95e7ebdf959caa291136203eb49d601
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

commit 4ac5db90261157bc2ab509bf64251ce677b256fd
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:46:02 2014 -0500

    Makefile: OTA File by Date
    
    * This will keep things from getting confusing
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 95be98a32e1276e6160a9ae69014c9b6e6a87eac
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:50:24 2014 -0500

    Remove MOAR Bloat
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit cba6cf66605adb4ee11970fc977c687cc2255b6f
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 26 11:44:11 2015 -0700

    Kill Bloat with Fire!
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 6415a77fecffaa7636fdc1b8a7521d2368f61642
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Feb 26 20:48:11 2015 -0700

    Build: cmRemiX up sounds and update (2/2)
    
    Base on Build: slim up sounds and update (2/2)
    reference on sdk and full base builds to slims make file.
    As well remove both copy command in sdk build. This is handled already on slims
    make file.
    
    Change-Id: I9b0146df1a43cfc5282288012fc59509e0badedf

commit 2663804bf1667596a60d02478035393fcc654224
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Feb 28 02:00:33 2015 -0700

    build slim launcher again for more testing

commit 6a5abdda3f04b2a1f046c0d30287e649f6e70ac3
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

commit 41a12854105d02ca8fd3db86841c8aab7b706b4b
Author: JoseGalRe <josegalre@gmail.com>
Date:   Tue Mar 3 14:36:10 2015 -0700

    build: optimizations for devices with low-RAM [1/2]
    
    Change-Id: I339042fc3d5b072297e4748be71ad6770367917d
    
    Conflicts:
    	envsetup.sh

commit bfca5dbfd76f863709f532052b08921aeae3f641
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 9 17:59:28 2015 -0700

    build: update clang qcom optimization & removed fastmath keep -O3
    
    Change-Id: Ia629fcabf627b5bccdf5d3bce18596dd64c8d2b2

commit abcab1b040dd3716aee51523eb28fb708c747e03
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

commit d08da9ef8b1aa0f30de3b96c0762d4dc2a1ed27c
Author: MaDc0w <MaDc0w@pac-rom.com>
Date:   Fri Mar 20 00:29:11 2015 -0700

    build: Rainbow unicorn puke [1/2]
    
    Change-Id: I393dd013194d73b293b361a42d42fa171ceee837
    
    Conflicts:
    	core/Makefile
    	envsetup.sh

commit 00d1719e11b56fbc1c05af6bc892be0d5d0e3741
Author: JoseGalRe <josegalre@gmail.com>
Date:   Fri Mar 20 00:31:49 2015 -0700

    build: move chromium call...
    
    Change-Id: Ia91e750470f4af67487bf3e52d208bedc3a585dd
    
    Conflicts:
    	core/Makefile

commit 71036401db061408085451c48648b44192857805
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Sun Mar 8 16:29:37 2015 -0400

    build: Prebuilt Chromium files check
    
    Change-Id: Ic12f1d2559417f74af787e635d1ab882d07d9d00
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit b8bcd846c333d97579f7a1d49c24ecf996cff1ba
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 14:16:59 2015 -0700

    build: removed gnu11++ optimization and fix SM version info
    
    Change-Id: I5dcd750856a7d7ef38dd8c0e339c8755724043f5

commit 10cdabc5fc922ea5f803a80e2d13224dc051abd0
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 24 00:04:48 2015 -0700

    build: -Wno-error=maybe-uninitialized
    
    Change-Id: I322f0d1951b461e44f3ebf913dab3afbb43bcb47

project cmRemiX/
commit 2938cf2fd65a1298f1b356181b120c708908c64a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 22 18:51:50 2015 -0700

    update to qcom snapdragon clang v3.6

commit c26bcfab0b9eea23b4f7873651de7ad9475534fd
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 22 18:55:03 2015 -0700

    derp

commit a156338d9ff96ecc02c60e2c23e4dd191167bc85
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 22 20:07:50 2015 -0700

    add back qcom clang v3.5

commit 78c5c2271c99554bc62718ef4b43a9540f864623
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 14:33:21 2015 -0700

    revert compile_rt

commit 3f2093da9b3d93d025b2ee8ebc3532458f277165
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:19:07 2015 -0700

    track SM arm-linux-androideabi-4.9

project device/samsung/trlte-common/
commit 50768ea4ea5558130f59dfaa20a88bff4cefaac1
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 17:53:33 2015 -0700

    DONT_DEXPREOPT_PREBUILTS

project frameworks/av/
commit 5a728307f0e82a813bb181d2f80501817ea2623e
Author: nadlabak <pavel@doshaska.net>
Date:   Mon Mar 23 23:48:52 2015 +0100

    audiopolicy: Fix call recording for legacy qcom HAL
    
    Change-Id: I774f75b493c47386ca1eaf004d663432f1041a66

commit c29fb05f433e919815083a14445185ac8173597f
Author: Weiyin Jiang <wjiang@codeaurora.org>
Date:   Wed Mar 11 16:51:38 2015 +0800

    audioflinger: refresh fast track underrun state upon start
    
    False underrun is detected when starting recycled fast tracks, which
    leads to continuous fatal assertion failures and even AP reboot.
    
    Track's last mObservedUnderruns isn't updated one at previous stop()
    call. Hence, when we start the same track again, we should synchronize
    it to the latest state instead of relying on stale one.
    
    Change-Id: Ia003a49c6896dba965798c062c98b8c367ef8369
    CRs-Fixed: 803389

commit b2de0c19b11c8b83873510eb6c629cf4cfd62b1e
Merge: cf8c5de c29fb05
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:24:13 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

project frameworks/base/
commit c17bf2d040e53ac50a0d2017bfb318c2498a852b
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 10:01:45 2015 -0700

    Revert: RAM bar (1/2)

commit f859af0f3676b69dc2eba71cc42157414067e1b5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:25 2015 +0200

    Automatic translation import
    
    Change-Id: I460224ba9600de61f44fb9950ca1d80ed7a12d4e

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

project frameworks/opt/net/wifi/
commit 67d21c2ce1ce492fb798dbdbef09c99be0422f8c
Author: Hu Wang <huw@codeaurora.org>
Date:   Wed Feb 4 19:57:10 2015 +0800

    Softap: update WifiContoller state on start softap failure
    
    If start SoftAp fails due to tethering timeout or improper
    ssid config, WifiStateMachine would transition to InitialState,
    but WifiController is left stuck in ApEnabledState, which
    in turn fails to turn on WLAN again.
    
    Register WifiService to receive WIFI_AP_STATE_CHANGED_ACTION
    intent from WifiStateMachine, and if wifiApState is failed,
    inform WifiController to transtion to ApStaDisabledState.
    
    Change-Id: Ic54716745a4d8b4e0d6984251260390d452ab889
    CRs-Fixed: 781404

commit edbc0d618f2f47640c8ecc8d65f4b2b01b28cd5f
Merge: 5a16c4c 67d21c2
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:27:21 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

project frameworks/opt/telephony/
commit d683d69fa307189b9a280bb9a31a64eb24688482
Author: Rakesh Pallerla <rakesh@codeaurora.org>
Date:   Thu Dec 18 13:32:35 2014 +0530

    Abort Cross mapping process if SubInfo List is null
    
    Abort cross mapping process if the SubInfo List is null
    and notify Stack is ready for other processes to continue.
    
    Change-Id: I836484b06c29b63f86d1c264d3c7bd386b6c580e
    CRs-Fixed: 767026

commit d77b4cde527370f9ba68413aba581b13b9dbe830
Author: Sukanya Rajkhowa <srajkh@codeaurora.org>
Date:   Wed Dec 10 15:21:38 2014 -0800

    Telephony: Handle PS DETACH failure during DDS SWITCH
    
    In DSDS, PS DETACH can fail if there is an ongoing voice call on the same sub.
    This scenario is triggered when sub1 is DDS and is in a voice call. At this time
    there is an MMS on sub2. DdsScheduler goes into DdsSwitchState and initiates an
    on demand DDS switch from sub1 to sub2. This involves doing a PS DETACH on sub 1
    followed by PS ATTACH on sub2.
    If PS DETACH itself does not go through, data connection on sub1 will not be torn
    down. As a result, DdsScheduler will be stuck in DdsSwitch state unable to process
    further DDS switch requests.
    Handle this by introducing PS DETACH retries for 6 times and notifying DdsScheduler
    of the failure so that it goes back to IdleState to process further requests
    
    CRs-Fixed: 759265
    Change-Id: Ia426a51167be007847b1edde444eb154bb536e5a

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

project hardware/qcom/wlan/
commit df34a8d9881e386cd077b4629707056aad13e18a
Author: Ethan Chen <intervigil@gmail.com>
Date:   Tue Mar 24 18:37:33 2015 -0700

    Revert "Further Availability Map Structure change"
    
    This reverts commit f624f39421073a0851749a8a72248442055c43cb.
    
    Change-Id: Ibe2a4b622550534df120032d8a818d098d81cb1e

commit 325fb2e06b5a18b6b732b74da06225b91df80439
Author: Ethan Chen <intervigil@gmail.com>
Date:   Tue Mar 24 18:37:47 2015 -0700

    Revert "Adding support for passing userdata in nan_register_handler"
    
    This reverts commit 50ed1c836c1253a26ba9256f5eb04f3a96889c97.
    
    Change-Id: Ia31e7f2110ab01c4ae1f751144ab7d7cb33efe4e

project packages/apps/CMFileManager/
commit 96e8aa29d876ec15688b9941ff40ff4ff75a8900
Author: Zyg0te <edvard.holst@gmail.com>
Date:   Sun Mar 22 14:37:33 2015 +0100

    CMFileManager: Nitpicking on strings
    
    Secure Storage password reset is probably better described as a password
    change, as you have to submit both the old and new password to perform
    the change.
    
    Syntax Highlighting sounds better than just Syntax Highlight, doesnt it?
    Change-Id: Ibf28d93c3cf38e4c706687eddd78fa4aebc2038a

commit 1e3be7d23d1a69d6d10c3bbe1cada878ebde6ea8
Author: Zyg0te <edvard.holst@gmail.com>
Date:   Mon Mar 23 21:15:37 2015 +0100

    CMFileManager: Removed copyright portion of about_summary
    
    Change-Id: If794766a6b55a3a289bec5c3a96b9c3cea15588c

commit 72869df54dc7d62d8c9a34a8afea47937c0c61f0
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Mar 23 22:17:01 2015 +0100

    cmfm: update changelog
    
    Change-Id: I29dda23c3e30da28288733fb8bb93ba20730ca42
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit f8a8d15371d11b691a919a90880dc10f096cc952
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Mar 23 23:58:13 2015 +0100

    cmfm: fix typo in xml drawable
    
    Change-Id: I414a67eb4fbc022b72eaa6c41b173a12a66a11e8
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 79d00ace1b886c4eb487661720e2493953027f8d
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Tue Mar 24 00:13:55 2015 +0100

    cmfm: reduce banner size and adjust ratio to fit the banner view bounds
    
    Change-Id: I46df6cb1c167fac8d7fe5a7b83f572634cfb44f4
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit b96748d2ea7edf747d2eaae5e3ee2f89e6e69aaf
Author: Zyg0te <edvard.holst@gmail.com>
Date:   Tue Mar 24 23:53:45 2015 +0100

    CMFileManager: Changed status string to something more descriptive
    
    Currently the status switch doesnt really communicate what its
    indicating the status for. If it's supposed to be indicating whether the
    partition is mounted or not, the status string should indicate as much.
    
    Change-Id: Ia3a89bb7ef4c603c596777e9cc0f6cae613b990f

commit 1288edb9bc0b752d157af7f17d00de52bcf61652
Author: Zyg0te <edvard.holst@gmail.com>
Date:   Wed Mar 25 00:06:14 2015 +0100

    CMFileManager: Fixed string typo
    
    Change-Id: Ied59603a11be19f10eb11d1ef8b9d3a043f110cc

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

project packages/apps/Calculator/
commit 207cff207bdd76defb4754a5818c17e62e92a832
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 23 09:46:06 2015 -0700

    Calculator: remove cbrt option in floating calculator advanced window
    
    The lexer can't seem to parse the function, and it doesn't exist as a
    function in the full app.
    
    Change-Id: I3dd2d9c8834d9178ee8ab8e37af3a3e45390f21f

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

project packages/apps/Camera2/
commit 40d8dce70728e2970675df8b04a47db66d8a634d
Merge: 982bcc1 7a11a41
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:30:20 2015 -0700

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

project packages/apps/ContactsCommon/
commit 33e8f4228b4b3fa76b23d0006800e56e1d7f304b
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 19 14:46:10 2015 +0100

    contactscommon: ensure preferences are loaded before reload data
    
    SIM state event can arrive early than the preferences were loaded. Just ensure that preferences are loaded
    in that event too.
    JIRA: NIGHTLIES-884
    
    Change-Id: I9909c3a2302b9aa83f41365514cea622ab568a05
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

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

project packages/apps/Email/
commit 8ee3601a81b4107c4ccd7fe1f3032f18af7cba79
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 27 00:57:30 2015 +0200

    Update strings for crowdin
    
    Change-Id: Ib59198e1321db5b3c6889432c842d42dd040cea4

project packages/apps/Gallery2/
commit 6de816c631ebed08bb50ab23e51318ba81f16de5
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

project packages/apps/Mms/
commit 62461530f0e62d7ae47c7198e2acec3e47a4286c
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Mon Mar 23 16:08:47 2015 +0100

    Backup: fix crash when listing backups
    
      * importing a backup extracts the backup zip
      * when an import gets aborted (the device reboots, low ram condition, the
        user or any application kills it, ...) the import does not clean up the
        extracted files
      * if the user now goes back to the importing screen, where a backup to import
        can be choosen, the adapter tries to parse the extracted files and it crashes
        with a number format exception
    
    Solution:
      * use a filename filter to only accept zip files
    
    Change-Id: I6fe1ec2f6f011677a983c3cb8152ca6d52b49690
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

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

project packages/apps/Settings/
commit 8238a8ea6f3042c1f64d58f10f2c30cbdfc126f2
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 10:05:52 2015 -0700

    Revert: RAM bar (2/2)

commit 89bc1a5bb9d3d450788cbd2abf2c3c7954a8a0b4
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:24 2015 +0200

    Automatic translation import
    
    Change-Id: I3df9393551ebf117cc6461f799e778ad3d660116

commit 9b57bd56d5592419a9ea4ec477972032fd281269
Author: Tamás Tóth <syman@babulus.hu>
Date:   Mon Mar 23 10:16:21 2015 +0100

    Settings: Set untraslatable
    
    Change-Id: If13991f0daf9a02cd3e3c25ff512a956ed9720c7

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

project packages/apps/UnifiedEmail/
commit 1011e62ae812ef733b8e285aa4f22b4e608986c5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 27 02:24:15 2015 +0200

    Improve strings
    
    Change-Id: I5bd562779fcd3a85a3e03a0432ea0413d26f52a5

project packages/services/Telecomm/
commit 2e18c0609c827738171709a3e40f92eff69df1dd
Merge: 1952939 e556309
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:33:05 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/services/Telephony/
commit 50451ca01742026cc56da68c60301df1ee100584
Author: Lin Ma <lma@cyngn.com>
Date:   Tue Mar 24 21:09:27 2015 -0700

    TeleService: Set mode to 2g on other sim(DSDS) prior to change
    
    * Fix a bug where other SIM slot gets changed when
    user wants to change the preferred network type.
    original commit 69efa99f1cd4afdaeec4554475594bc6a2900338
    
    Change-Id: I69fde842b1c27601752cd3a1078664eb26d86fe1

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

project prebuilts/clang/linux-x86/host/llvm-Snapdragon_LLVM_for_Android_3.6/
commit dae3881361a67bd81f775c0282dd87ff179ad3b4
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 22 18:07:18 2015 -0700

    initial commit for llvm-Snapdragon_LLVM_for_Android_3.6

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
commit a4f3e9a213f97e0381eca9b82856618a011db20c
Author: Tamás Tóth <syman@babulus.hu>
Date:   Mon Mar 23 22:09:16 2015 +0100

    Update Telekom (T-Mobile) HU APN
    
    Change-Id: I003a14519b17ea0f7a3d72ee16fb97eeb763eb3e

commit 75271cfdf9ad92eefa82d7347cc2cf411cb276b6
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Tue Mar 24 14:37:37 2015 -0700

    Airtel MMS - Add authtype=1 for PAP
    
    Change-Id: Ic41d403221351b5bec67c306d8ded2915e0cf45b

commit 2ca5d3999b35d328f0969a264009bffe0faf889d
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 27 11:42:11 2015 -0700

    vendor: add sepolicy entry for killswitch service
    
    Change-Id: Ib3c44c50138f5715d92addbf8df7ed591785b550
    Signed-off-by: Roman Birg <roman@cyngn.com>

project vendor/cmremix/
commit 36df53c28bb3f491f8f2f21237e05028e141d501
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Mar 22 23:20:22 2015 -0700

    Saberize v4 (1/2)
    This includes all the current sabermod changes plus
    
    some new defaults for gcc versions.
    
    Change-Id: I29d53fdc190a368b7dc20f211cd3e0d8c1008c7f
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Update sm.mk:
    
    Include -mthumb-interwork to LOCAL_DISABLE_O3_FLAGS
    Update disable graphite modules for omni-rom
    
    Change-Id: I6a57d6d0dd15f079c1704ad1bcc509d756c29ec5
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Add list to disable -mthumb-interwork
    
    Change-Id: Id0aec04f0713f5c1ceb7c799c2a5bb433346dfb9
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    sm.mk: Cleanup -O3
    
    Change-Id: I9bbf6cbb9ebf0229c7b31be50b1d78c6747e72c9
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    sabermod config:  include pthread in build flag options.
    
    Change-Id: I2fa9ed41a4865d01920691ce3e1923b875a0dcf2
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    update LOCAL_DISABLE_GRAPHITE list
    
    Change-Id: I1c1e8c5dd2f4dc3dec0d3068e85400c04cc6999a
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Update warning message for new rom changes
    
    Change-Id: I87fd97e5eac7cc24fa497fe6e2e24b077158e060
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    SaberMod config:  Move graphite flags to where they "should" be.
    
    Change-Id: I9eee0e97f896a64ebff3bfb3fcf9f5c0a2b4b3c7
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Update for new sabermod toolchain naming style
    
    Change-Id: I184f605be1b5db4b2983774d521bf68ef7dcfc6a
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    opps
    
    Change-Id: I0e703f474e8124d66febe287f6e931ef443fe16e
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Add TARGET_LIB_VERSOIN (2/2)
    
    Still getting hit with missing cloog lib errors.  Sometimes
    TARGET_SM_AND can be set different than the actual gcc version itself
    
    Change-Id: I8f5b51f221f26a3c9e7e521dda230353161f9e2f
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    hammerhead: include sabermod device configuration
    
    Change-Id: I7302ba9fa2e841da7116bafdcb57a1411117cde2
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Update sm.mk
    
    Change-Id: I0243c464c92061d9fab83b3a2360a3505b3934df
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Include TARGET_SM_KERNEL and MAYBE_UNINITIALIZED
    
    Change-Id: I7fb086763652c91d4f97672b81194c27c092d9b2
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    hammerhead: target lib version 4.8
    
    Change-Id: I5d99032af36cea79e2988e0e30fb35e5074a820d
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    sm.mk: update warnings with a more generic description for all ROMs
    
    Change-Id: Iee484ad6b65144f0b81f844e9f69bc7e4caa6861
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit be497c7666a9e97e36902d15b27c4bace14d61c4
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 23 17:11:42 2015 -0700

    vendor: update flags

commit cb410679dc0c9871af9e003e9487d9d7d205f4ba
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 24 16:31:42 2015 -0700

    C M R

commit 013558da4e65ec19301223da4815c114cfcb4d82
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 11:49:47 2015 -0700

    vendor: update sabermod.mk

project vendor/samsung/
commit b6dca7f1d874296d6b88307aa81e1d445a19fd7f
Merge: c36d013 51ea1bf
Author: ciwrl <ciwrl05@gmail.com>
Date:   Mon Mar 23 15:58:38 2015 -0700

    Merge pull request #600 from solk2/cm-12.0
    
    ks01lte blob updates

commit 0f74675cc514245a67036424b96ae7b7f6484b57
Merge: b6dca7f 850fda5
Author: Ethan Chen <intervigil@gmail.com>
Date:   Mon Mar 23 22:41:33 2015 -0700

    Merge pull request #556 from Alberto96/cm-12.0
    
    i9500: update proprietaries for L

commit 714323b48cc7df0aa82c29edbbccbd0741319c75
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Sun Dec 21 12:49:29 2014 -0600

    msm8960-common: update adreno blobs and d2 camera
    
    * From: I535VRUDNE1
    
    Change-Id: Id073c52c7646cd5d18791685b3da324d662f3a8a

commit 7f1b2ea8d3e2ff951ccc0e691e50cede4dc61e03
Author: sbrissen <sbrissen@hotmail.com>
Date:   Tue Mar 24 14:54:10 2015 -0400

    t0lte: KK ril blobs

commit 9024b3036e6f56339017997458077ccdcf479b28
Author: sbrissen <sbrissen@hotmail.com>
Date:   Tue Mar 24 14:56:17 2015 -0400

    p4notelte: update KK ril blobs

commit cb8d668fe5996b49dc7035f652821b67f789201b
Merge: 714323b 64e7efe
Author: Ethan Chen <intervigil@gmail.com>
Date:   Wed Mar 25 08:52:33 2015 -0700

    Merge pull request #601 from JoseGalRe/cm-12.0
    
    jf-common: fix path for locationservice

commit e9fb886f2f23701c9e3e0b55343fc3da1c66ac7e
Merge: cb8d668 9024b30
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Fri Mar 27 08:44:39 2015 -0500

    Merge pull request #602 from sbrissen/cm-12.0
    
    KK ril update for p4notelte and t0lte
