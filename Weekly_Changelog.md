project CMRemix/
commit 58d8d95dd87a0c589ee02da39905519c865e693a
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 15:12:01 2015 -0700

    track codeaurora Caf Repo

commit 07b93cc12cdb1895507737c128793198d83459c2
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 13:59:19 2015 -0700

    add back cmremix various repo

commit 4247df28cfdf36d7baaabbfc87b436698432f9ef
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 09:26:25 2015 -0700

    remove duplicates

commit 4c58cb642647e361ca40be2d4fffe0f8e9c630a5
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 15:21:49 2015 -0700

    removed cm MediaProvider

commit 43f9d6b6c0eecbcc67d5da8bac26c1f6d8266d4f
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 00:27:47 2015 -0700

    track frameworks av & native

commit 6fd3aedcd727dfa44166ac62ae4b3bc866dd8302
Author: Tony Layher <layhertony@gmail.com>
Date:   Tue Apr 7 17:48:48 2015 -0400

    manifest: Track our own chromium/v8
    
    Change-Id: Ic69f29266388545154d78f60b0ba126127929aa2

commit 384b3f5f56d36b690365dea8fd7b870e363d3c41
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Wed Apr 8 22:26:27 2015 -0700

    Track our own external/libvpx
    
    For x86
    
    Change-Id: Id44c119d52b39aacd9dfd353baf340fff189283b

commit 19b9a70cd61e6666f45e1e2bf9fc2dd7149f7822
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 03:11:56 2015 -0700

    track MusterMaxMueller's clanglibs qcom 3.6

commit 071c72fde27c7306478a660d0d64be5769bf469f
Merge: 19b9a70 384b3f5
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 03:15:00 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 71cee1b9428c26ddb62c74dc0af12bbffe900a7e
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 23:14:29 2015 -0700

    track all needed apps from cm-12.0

commit 8a1754ac8178991fc807ecbe4451d041d0b0e26c
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 10 07:58:55 2015 -0700

    remove opt/hardware duplicate

commit 0ac2075d36d809801bafb625fce60da9c8e887b5
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 10 08:19:48 2015 -0700

    update manifest

commit 81fbf082ab8f2df3e2cbb1913dc495f1757201f1
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 10 08:20:00 2015 -0700

    track MusterMaxMueller's clanglibs qcom 3.6 (reverted from commit 19b9a70cd61e6666f45e1e2bf9fc2dd7149f7822)

commit 9ed0ac6b48671fb4a779a40522749789dd0db1fb
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 10 08:22:16 2015 -0700

    remove more dup

project bootable/recovery/
commit 75496c1b274ab3b3050151b8ea2e4738b8de0891
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Wed Apr 8 03:22:42 2015 -0400

    Don't disable including TARGET_RECOVERY_UI_LIB if exists
    
    This is needed for fugu (Nexus Player) as it has one button on the
    bottom.
    
    Change-Id: Ic9f1f546abd90ff9bb6f983bc57628bcb45d641c

project bootable/recovery-twrp/
commit 2252d24c964df89189143e8d09626e9455e0f580
Author: that <github@that.at>
Date:   Fri Apr 3 22:33:04 2015 +0200

    twrpTar: fix segfault after encrypted backups
    
    also use unsigned int for core_count instead of unsigned long long.
    I'll change it back when 4-billion-core devices are common.
    
    PS2
    - cast return value via intptr_t (may be important for 64 bit platforms)
    - output errors from TWFunc::Wait_For_Child to console
    
    Change-Id: I04158daa0b64e44d68e179d626a83d81cf5d49f7

project build/
commit 3d6ba53e5f1e145e49c7e3c0b74db395c29910d4
Author: Rashed Abdel-Tawab <rashed@linux.com>
Date:   Tue Feb 24 23:00:38 2015 -0500

    qcom_utils: Add msm8992 and msm8994
    
     * The Snapdragon 808 will be releasing as the msm8992 so
       reference it as such.
     * The Snapdragon 810 is already released and used, so build the
       qcom utilities for devices using msm8994.
    
    Change-Id: I564cb68295099a73fefd24d43e19ca371968ef44

commit dce67d2009b89db15f0d21d390af159425a479b7
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 13:57:23 2015 -0700

    Revert: Build: cmRemiX up sounds and update (2/2)
    
    Base on Build: slim up sounds and update (2/2)
    reference on sdk and full base builds to slims make file.
    As well remove both copy command in sdk build. This is handled already on slims
    make file.
    
    Change-Id: I9b0146df1a43cfc5282288012fc59509e0badedf (reverted from commit 6621c1436f9a12190177cd0f2195671269bd2a4b)

commit 318309bde024891cd8751ffdf9fe9e84601ddcc8
Merge: dce67d2 2e6c7c4
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 15:45:15 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project device/qcom/common/
commit 08c7e809674b2092526e6a30f5513b049e5fb266
Author: Arun Kumar K.R <akumarkr@codeaurora.org>
Date:   Tue Jun 24 13:17:55 2014 -0700

    init: Add MSM-specific init extension library for 8994
    
    - Implements MSM-specific initialization during bootup
    - Sets the lcd density at the bootup
    
    Change-Id: I2bbc3e724682b8b11329b87c26aca1e4faf8d357

commit 49446fd5753d540a00f4db9474c01f98696a264a
Author: Ilia Lin <ilialin@codeaurora.org>
Date:   Tue Oct 21 14:01:57 2014 +0300

    init: qcom: Set LCD density for Dragonboard APQ8094
    
    Set proper LCD dencity for the FWVGA display on the
    Dragonboard APQ8094.
    
    Change-Id: I6bd657ee90a21ed8a13e6456b05feaf79b5c5c95

commit 87416cf91ea703d405ec69f2e48f9f86772ab83c
Author: Jeykumar Sankaran <jsanka@codeaurora.org>
Date:   Mon Dec 8 13:52:20 2014 -0800

    init: Add MSM-specific init extension library for 8992
    
    - Implements MSM-specific initialization during bootup
    - Sets the lcd density to 480
    
    Change-Id: I2997e902c3bdafefda0bb98b8d8b3c1279c7b5dc

commit b0eb8ec264243d41855923b57ea7916a9a83f90c
Author: Dilip Gudlur <dgudlur@codeaurora.org>
Date:   Wed Jan 28 15:17:45 2015 -0800

    power: introduce 8992-specific handling
    
    Creates framework for handling special cases like
    display off, video encode differently for 8992.
    
    Change-Id: I195a96f0787c0d2dc2696c75a6f281774e2345cb

commit 202720576073847dfd260bde7aac8539583fb944
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 4 10:23:16 2015 -0400

    power: Updates for 8916/8939
    
    Change-Id: Iaf5f6b726e7e171a077bb326b05266d1c8a8f107

project device/samsung/trlte-common/
commit f3894cc7985de84e4e1fef2902fc890d54cd7840
Merge: 50768ea 56654b5
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 16:49:42 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.1' into cm-12.1

project external/bluetooth/bluedroid/
commit 19517c6c8fc4a9137c52e359c20a221e8017e284
Author: arter97 <qkrwngud825@gmail.com>
Date:   Sun Sep 21 00:07:06 2014 +0900

    Enable -Os back to bluedroid
    
    Using plain -O3 causes bluetooth to not work properly.
    Fix this by adding -Os to the CFLAGS.
    
    Change-Id: I61cd3aa25a80c73a5e5647b064f77f9731e00f48
    Signed-off-by: Park Ju Hyung <qkrwngud825@gmail.com>

project external/chromium_org/
commit c9d88d668f85f20b0db2ce846746685451b0fef5
Author: Tony Layher <layhertony@gmail.com>
Date:   Sun Apr 5 12:24:13 2015 -0400

    Fix build for MacOSX 10.10.X and CLI Tools 6.1.1
    
    Change-Id: I36d3bca779d96a0cf6f90f9ba9a2ac94052a4ccf

project external/chromium_org/v8/
commit eba9304aedaf5734919f0936f7ff1876cad04200
Author: Tony Layher <layhertony@gmail.com>
Date:   Sun Apr 5 12:24:44 2015 -0400

    Fix build for MacOSX 10.10.X and CLI Tools 6.1.1
    
    Change-Id: Ic2052cd54e8c07f595ea273673322dace81ce760

project external/ffmpeg/
commit 97ebddcc2efa7301fa96f047be6741543f842388
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 7 01:14:12 2015 -0400

    x86: Use yasm from prebuilts and don't depend on host install
    
    Change-Id: I88016039ba8727eba72eabc49c90379211f77dd2

project external/libnfc-nci/
commit f1c4f2f8191f9d451a6368015490de8138f73abc
Author: Rashed Abdel-Tawab <rashed@linux.com>
Date:   Tue Feb 24 22:50:39 2015 -0500

    libnfc-nci: Change to LOCAL_MODULE_RELATIVE_PATH
    
     * Fix warning when compiling multiarch HAL
    
    Change-Id: Ie7f50d0a78eb43260a44a7d5cf69073b72e1c568

commit 25190cbecf840f5583449a9537a858a01eac4439
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 4 23:57:04 2015 -0400

    nfc-nci: Unbreak NFC for the planet
    
     * LOCAL_MODULE_RELATIVE_PATH should not have a path.
    
    Change-Id: I77a184f437069a04c67a2f94c608c4cdcbfda4e2

project external/libvpx/
commit 3bead6224f8abd081a9db85d098aab999f0b787a
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Wed Apr 8 23:26:31 2015 -0400

    Use the prebuilts version of yasm to avoid host install
    
    For some reason YASM is getting redifined after being set in
    build/core/config.mk, so lets just make sure it's set again here.
    
    Change-Id: Iab42e048964289928e58a929a093f52aa6c4924f

project external/sepolicy/
commit 79ff523ac99b339914ccaa754e068072d64da542
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Apr 5 16:19:57 2015 -0400

    sepolicy: Deduplicate the final policy union
    
     * In our current setup, if the product makefiles attempt to be tricky
       and re-read the BoardConfig (in order to get the SoC type), we end
       up with duplicates in this list. This causes the build to fail. Let's
       just tolerate it until a better solution is created to the board vs.
       product setup problem.
    
    Change-Id: Ia6d16da4424b3e354cae3f78c3ee8a9ef565046c

commit 7e7f5f45c449fcf12fb8f56f7e46c67480ab4d97
Author: Ethan Yonker <dees_troy@teamw.in>
Date:   Tue Dec 16 14:23:00 2014 -0600

    Make recovery domain permissive so we can set SELinux permissive
    
    This change makes the recovery domain permissive so that we can
    use the recovery selabel in the init.rc to set SELinux permissive
    in recovery.
    
    Change-Id: Ib371ff9f0a0b2c5a0a97183afaf1fe89c5a90dc1

commit c89e40a7d6de9fcea9e7574f2ba420e4f8979036
Author: Ethan Yonker <dees_troy@teamw.in>
Date:   Mon Dec 15 11:32:05 2014 -0600

    Allow init to setenforce to set SELinux permissive
    
    Allow init to change SELinux to permissive, mostly for TWRP
    purposes.
    
    Change-Id: I0985c3bcde8cf96a1219024571ee0a19e7af5d24

commit 947754944032a36152efd8ebc6b64935646c3882
Author: maxwen <max.weninger@gmail.com>
Date:   Fri Jan 2 17:33:43 2015 +0100

    sepolicy: changes for lvm support
    
    PS2:
        allow lvm device:chr_file { read write open };
        allow lvm block_device:blk_file { read open };
        allow lvm lvm:capability { mknod };
    
    PS3:
        allow lvm labeledfs:filesystem { mount };
        allow lvm lvm:capability { sys_rawio };
    
    PS4:
        move lvm-placeholder attribute to attributes file.
        fix build for non lvm devices.
    
    PS5,6:
        fix code style and commit message.
    
    Signed-off-by: Humberto Borba <humberos@gmail.com>
    Change-Id: Ia237e70f7f74cd12406b722ad2b9b673475f3a28

commit d2a9e973cd087b936df9ac2592f1e01468bbbec4
Author: Ruben Brunk <rubenbrunk@google.com>
Date:   Wed Jan 28 18:15:01 2015 -0800

    Add security policy for ProcessInfoService.
    
    Bug: 19186859
    
    Change-Id: Ic08858f346d6b66e7bfc9da6faa2c6e38d9b2e82

commit 307ef54608c9f484181851ad2b14187f2fa083a4
Merge: 9477549 d2a9e97
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 15:49:45 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project external/sqlite/
commit d57ae734d0a9a05c226f680da4dc034cb8228b22
Author: arter97 <qkrwngud825@gmail.com>
Date:   Fri Dec 12 22:12:19 2014 +0900

    Upgrade to SQLite 3.8.7.4
    
    Downloaded from http://www.sqlite.org/2014/sqlite-amalgamation-3080704.zip
    
    Change-Id: Ib22c3156fb37a1cd0f06497508424f89dfba98d4
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit d88e35ccf9d8ee15ecfe6eaac66e607955dbfd18
Author: arter97 <qkrwngud825@gmail.com>
Date:   Thu Jan 22 00:08:15 2015 +0900

    Upgrade to SQLite 3.8.8.1
    
    Downloaded from http://www.sqlite.org/2015/sqlite-amalgamation-3080801.zip
    
    Change-Id: I32ec7d945e6cdb3495c9621a68926a8d5e32fdec
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit cf55ddb159d594ed378dbbc3d998da8f224b3009
Author: arter97 <qkrwngud825@gmail.com>
Date:   Fri Mar 13 17:44:38 2015 +0900

    Upgrade to SQLite 3.8.8.3
    
    Downloaded from http://www.sqlite.org/2015/sqlite-amalgamation-3080803.zip
    
    Change-Id: I48989910d22b7feee57bf9e8b4c3cc9692207b88
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit 4623ad4ec136adc1fbf60771ec9ebccaedbb0694
Author: Kiran Kumar H N <hurlisal@codeaurora.org>
Date:   Fri Feb 11 10:45:48 2011 -0800

    SQLite: Enable fdatasync for SQLite
    
    SQLite library recommends usage of fdatasync when available.
    Since it is available for linux, enable it. This gives better
    performance compared to fsync.
    
    Change-Id: I47d5fb9cb1e8331729b54d77f10f7499e028269d

commit 39f8b22d88690adc61807010a5f9f5892ce7488d
Author: David Ng <dave@codeaurora.org>
Date:   Tue Jul 5 10:53:34 2011 -0700

    Add hooks for database open and pragma handling
    
    Change-Id: I0c1843a1c17e6cb7786ea5c66d229282b1fa0d32
    
    SQLite: Updated hooks for database open and close.
    
    Change-Id: I38135eaed3b5e66ef302eb0337f1bf3ba9f184d7
    
    Leave out magic perf code unless requested
    
    Change-Id: I154e288e440abd70dd4eec590150be1e800efac9

commit e4476b08906ab6cf728ec3ff112ec4758123d13c
Author: Steve Kondik <shade@chemlab.org>
Date:   Tue Dec 3 05:57:43 2013 -0800

    Additional guard around perf enablement
    
    Change-Id: I37aaa73110b5d91aae7a35cb8fecf4eade088661

commit 3a5e813623adf1491c39e27a82e03a660f0462b7
Author: Koushik Dutta <koushd@gmail.com>
Date:   Thu Dec 5 11:30:15 2013 -0800

    Do not pass QC_PERF into host build of sqlite3.
    
    Change-Id: I1ea8c434e2996ae5b5197c5dafb5f868aa485d87

commit 4f6a20dd3cec6e0114ac23b08cd72fa75a01a63f
Author: Steve Kondik <shade@chemlab.org>
Date:   Sun Sep 14 19:21:44 2014 -0700

    sqlite: Rename perf flag
    
    Change-Id: Id5bfb5901a56fb4ab5a077e4275ee3693db2f706

project frameworks/av/
commit 7e1c0f2bb721f12b067fd88dbe53618e22d6c0a9
Author: nadlabak <pavel@doshaska.net>
Date:   Mon Mar 23 23:48:52 2015 +0100

    audiopolicy: Fix call recording for legacy qcom HAL
    
    Change-Id: I774f75b493c47386ca1eaf004d663432f1041a66

project frameworks/base/
commit e7fbe8c6cd36a6012a83f405a996c9a067b85cc0
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Dec 14 11:54:32 2014 +0100

    CommandQueue: showCustomIntentAfterKeyguard ensure that it gets syncronized
    
    Change-Id: I86be91a09277bfa8b1522fb0088541ac865eb23b

commit c1e829c7cd64456eff9fdbc3ab8c32f3cff65bdf
Author: faust93 <monumentum@gmail.com>
Date:   Fri Apr 3 13:08:03 2015 -0700

    Wakelock Blocker [1/2]
    
    Change-Id: I4197ef96e9f05f78cf72b69281ba3109a9e8f0f7
    (cherry picked from commit 6d162d0b99b290a374b25cb117798f49458735fd)
    
    (cherry picked from commit ffb36324022faab0629ae82eebe705ea295aafa7)
    
    Conflicts:
    	core/java/android/os/IPowerManager.aidl
    	core/java/android/provider/Settings.java

commit 859aec770b0686f6740ea64e40afe34c079f7a84
Author: dankoman <dankoman30@gmail.com>
Date:   Tue Dec 9 20:25:37 2014 +0100

    Frameworks: icon materialization
    
    These are the first few. There are still 23 more shortcut image
            resources that need to be done, and these will come
            sometime next week probably.
    
    Change-Id: Ie10d154914d2e4cfe2e7960791cff6240a1a2765
    
    (cherry picked from commit c2bc7b80066f14b4763c9f904dcaca85f2da71e0)
    
    (cherry picked from commit d26fdf5ffc55addf95a989d03a29818aa3008c68)

commit 42b5686f30e0ed26245e5fc3ec51894cfcb39ae7
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Fri Apr 3 13:11:19 2015 -0700

    Frameworks: Keyguard - Add user configurable shortcuts
    
    Change-Id: I55620f3835775792282ef8b9468ed0dd626c0beb

commit a8ae8ddd481e4278b1449804c92a765392f8274d
Author: Kyle Repinski <repinski23@gmail.com>
Date:   Wed Dec 10 15:40:37 2014 -0600

    Fix strict aliasing violations.
    
    (cherry picked from commit 6d19195845b6c81a6507e4a23d26746bb2c9f0f6)
    
    Change-Id: I8c76d6e49bfe389c54325bf3ccb1503af81e357d

commit 4625507764ffc6698fad1aa833df3ffebe435ba0
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:07:08 2014 -0500

    Speed up Statusbar
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 3e15ac607851022be4cbd2ad994486a2cc0ae4f1)
    
    Change-Id: Ifd431336587812d2f0f3e4967f2ee0b209b00008
    
    (cherry picked from commit 9ff517b705b7878b5cdf9b5097118d899e098357)

commit 6a1cbaf4e1f0a33c4a35201f625bc2ef14289fee
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 12:01:14 2014 -0500

    Speed Up Recents Menu
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 8f5e45b66c56223e6cadac2cbc834ddf789cc2dc)
    
    Change-Id: I9ad9b0ca889221d97dd38aca0b703c43203ad6cb
    
    (cherry picked from commit 8eafc4aa6791dee6fc9aabb448ecf26cd8ad18fd)

commit 4a8e537edd7e62e4e076cda14bdada2059f775e1
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 11:58:29 2014 -0500

    Speed Up Long Press Timeout
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    (cherry picked from commit 95bde085987003486497e79f630ea9fa3c6868b5)
    
    Change-Id: I04be54afb7c99ada543c5a023dc340f6231fbdbe
    
    (cherry picked from commit 30a5d5b56f1fd9534c810de51f04d2f848a646be)

commit 6fd75cb2426cb7c535ea2d7034cd79eedf0df815
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Dec 12 01:20:48 2014 -0500

    Disable Lots of Debugging
    
    Revert "Debugging: Enable All Debugging until GPS bug is Squashed"
    
    This reverts commit a7e2e0bfc70c866645c2f45df2ab06030c7e1131.
    
    Conflicts:
    
    	policy/src/com/android/internal/policy/impl/keyguard/KeyguardServiceDelegate.java
    	telephony/java/android/telephony/SubscriptionManager.java
    
    Change-Id: Ife6bc042b8db2143a3005421230f6f2563aa8320

commit 1e31fbc9d341910f1216ddb0292c912e298232ea
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Apr 3 16:24:19 2015 -0700

    [Base] Nav bar tweaks
    
        - Toggle on/off (CyanogenMod alredy did but only for hw keys devices). crDroid allow all devices to do that for those using PIE apps.
        - Nav bar dimensions (height and width)
        - Here we also automatically reverts CyanogenMod navbar toggle: https://github.com/crdroidandroid/android_frameworks_base/commit/b70cda7d0d9b5142f54d390275b5e2ffa64ae9b4
    
        PS: THIS COMMIT IS A SQUASHED PORTED FROM crDroid KK and 99% od the codes are from SlimRoms. I want to say a HUGE thanks to @kufikugel
    
    Conflicts:
    
    	core/java/android/provider/Settings.java
    	packages/SettingsProvider/res/values/defaults.xml
    	packages/SettingsProvider/src/com/android/providers/settings/DatabaseHelper.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    	services/core/java/com/android/server/wm/WindowManagerService.java
    
    Change-Id: I16fd5700695d1e4730590d9ef026ad5c858c8c3b

commit 034fa2c64864c92f9c3f5eb8ef123ccc00806515
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Apr 3 14:22:01 2015 -0700

    [Base] HW keys tweaks
    
    PS: to enable this feature you need to set to true <bool name="config_hwKeysPref">true</bool> in device overlay. Of course this is for devices with hardware and capacitive keys ;)
    
    Want to say thanks here for @Temasek, CyanogenMod Team and OmniRom Team
    
    The hole inital idea of this commit is from Temasek with codes initially based on HW keys features from crDroid KK. 3-dots overflow button codes was ported from CM KK and some really useful ideas was taken from Omnirom sources.
    
    Conflicts:
    	core/res/res/values/cr_config.xml
    	core/res/res/values/cr_symbols.xml
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    	services/core/java/com/android/server/wm/WindowManagerService.java
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Change-Id: I917953f6dadf7234038777e8dd803961e5918813

commit ad605c2769a5e30e7f6035744c57772a82b7f26c
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Apr 3 16:33:40 2015 -0700

    [base] long press back to kill configurable timeout (1/2)
    
    Forward ported from crDroid kk
    
    Conflicts:
    
    	core/res/res/values/config.xml
    	core/res/res/values/symbols.xml
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Change-Id: Ie600f7ced186dceb3836bea3fc4288d2cd03f8f6

commit b0657a7337bfac0ab2ae68c1d5fa2f724b97039d
Author: nuclearmistake <nuclearmistake@gmail.com>
Date:   Fri Apr 11 19:04:15 2014 -0400

    Show package names during dexopt
    
    ps2: Attempt to determine localized package label, and print that.
         If unavailable, print packageName
    
    Change-Id: If9ca78fe312acd674bdcee160f914b4445d5c85f
    
    (cherry picked from commit b49c6bd2d90305bb095ce40c54a16e0bff5a99f0)
    
    (cherry picked from commit 26ce8ac33ae1e4235e89bb01b552b1c6c5156c82)
    
    (cherry picked from commit 1656dc9c63b99101c1bc59a4352978e32c67c511)

commit cb867914fe488d63adcd228630886ba651a32c9a
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 11:01:25 2015 -0700

    [SQUASHED] [1/2] FB: Status bar Network traffic
    
    This codes are not mine an here i'm giving the proper credits
    
    Commits inside and they authors:
    @htchoi1995: omnirom/android_frameworks_base@4268d2d
    @Haus1: omnirom/android_frameworks_base@12daeeb
    @Haus1: omnirom/android_frameworks_base@017c56c
    @cristianomatos: https://github.com/crdroidandroid/android_frameworks_base/commit/6504ad84f7bb0db10543d938f24412e2d082e43e
    
    @alviteri: Added SeekBar from KK for autohide
    
    Change-Id: Iec9ff5ecb23a3cabbe11621c5a856a19c2efc148

commit 4e10b978a0962ef2e6e5222063ef0929d8b3d5fe
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sat Apr 4 11:06:01 2015 -0700

    FWB: Network traffic supercharged (1/2)
    
    Bring back AICP kk traffic
    
    Change-Id: Ide3ac899da7632dd1fb3a0615ab9560a4ae6cfd0
    (cherry picked from commit 271b5c8f1e4e843a362526a7d9e25a4fde05e001)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/NetworkTraffic.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit cff89311a5c8477597052b918b83ba30776b9755
Author: 0xD34D <clark@scheffsblend.com>
Date:   Sun Apr 5 13:33:20 2015 -0700

    FWB: Gesture Anywhere - bring it back [1/2]
    
    AICPfy lp5.0:
    - Lollipopify LOL
    - By request from doc
    - Added TriggerOverlayView from AppSidebar
    - some lines from Locskcreen gestures to get
      it compiled and working
    
    Change-Id: I04acb9a88fe0011921a1bafdc1919d76ce57aedf
    (cherry picked from commit ccca76f5b82a7d6485128e2fb894fa5284c551b5)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit b37a4289bdc126407a40c9370cdd7aab5dddabaf
Author: blk_jack <jcorcoran+github@gmail.com>
Date:   Sat Apr 4 11:38:27 2015 -0700

    MediaScanner behavior on boot (1/3)
    
    Lets you enable/disable/ask (with a notification) media scanning on boot.
    Can speed up boot and reduce initial boot lag from MediaScanner
    
    Change-Id: I634ae96b1dcb493b966b4653589cd97523b63da7
    (cherry picked from commit 44e913eb5b1890ab5d009530a6b79d21b562742a)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 48207d0bb1988ce77135e0fbb3aa39221d1d7857
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 12:16:56 2015 -0700

    Revert "systemui: animate clear recents button on exit animation"
    
    Change-Id: Iaed877955a955ac918c1390ded0d14c3435728f3

commit cc0b20735f44e3834cd0a9f6e58333e924e3de56
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Wed Nov 26 12:04:44 2014 -0200

    [Base]: recents panel clear all button tweaks
    
    - Show or hide recents button
    - Place the button in top right or left
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/recents/views/RecentsView.java
    
    Change-Id: Ic50e62191bb033de3364c0bc0f314a64ee5d2f0c

commit b9b6e8ae9f25b586b24db8c7d71a68dc935c6648
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Apr 5 13:55:18 2015 -0700

    SystemUI: replace recents clear all button with a fab button
    
    * this allows us to have it any corner
    * added bottom right/left options
    
    Signed-off-by: Altaf-Mahdi <altaf.mahdi@gmail.com>
    
    Change-Id: I1016cae52d22d815e0a8fe4d83dda60e05a9cf51
    (cherry picked from commit 3ffdd9ce0b5942492fa434b046904ef42e3a08db)
    
    Conflicts:
    	packages/SystemUI/res/values/cr_colors.xml
    	packages/SystemUI/res/values/cr_dimens.xml
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/recents/RecentsActivity.java
    	packages/SystemUI/src/com/android/systemui/recents/views/RecentsView.java

commit 34dfec43ef72cd797104f7e5a4756b0b2528498f
Author: westcripp <korukaltan@gmail.com>
Date:   Sun Jan 4 02:36:23 2015 -0700

    add floating button center option & change clear all button
    
    Change-Id: I0e87e046569dadf9007536e9dd69587bb1568760

commit 28349edd31a94bade942a7f0037a88808fc7df2c
Author: westcripp <korukaltan@gmail.com>
Date:   Sun Jan 4 02:48:09 2015 -0700

    Recents: Update & add top center
    
    Credit: westcripp
    (cherry picked from commit e0ec77300e3e2d8240953463860bf2870e709e3e)
    
    Conflicts:
    	packages/SystemUI/res/values/cr_colors.xml
    	packages/SystemUI/res/values/cr_dimens.xml
    
    Change-Id: I417d1aa5c3e8bb5242dfdfc9e58c8cb0ac40cd24

commit ccf90f8609d513d29bf09fa36e6c77b111caad42
Author: maxwen <max.weninger@gmail.com>
Date:   Sun Apr 5 14:58:27 2015 -0700

    FWB: omniswitch as default recents (squash) (1/2)
    
    AICPfy and bring to lollipop
    PS5: G2G
    
    Change-Id: I866806ee3601ac69eb877f10c10bb881a70b1013
    (cherry picked from commit ffaabdffa5de3f294a8bb7e47ff75a6200dff96a)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit c43780dfdb82ad8fbc0f526e62d90d088a29d16a
Author: Janson Kang <temasek71@gmail.com>
Date:   Sat Nov 29 17:30:39 2014 +0800

    Remove unnecessary videos
    
    Change-Id: Ie8e312b582be06415d7d79ac31f38078da4ba613

commit af20693f80290a12e90360d150a266ffc942ba8c
Author: muzbit.kim <muzbit.kim@lge.com>
Date:   Tue Mar 11 16:19:57 2014 +0900

    Change SQL to improve performance.
    
    To know the number of images, use "COUNT(*)" instead of "_id" in SQL.
    Using "_id" gets all result set. and when getCount() is called, CursorWindow is filled.
    But using "COUNT(*)" gets just 1by1 data.
    So using "COUNT(*)" is more faster than now.
    And this SQL is called everytime per a file during a file transfer in MTP
    The better way is by using "EXIST".
    But if using "EXIST", modify MediaProvider.call() method.
    So i applied just a "COUNT(*)"
    
    Change-Id: Ic5882af0fad2304f836b7b7043a4746359391609
    Signed-off-by: muzbit.kim <muzbit.kim@lge.com>

commit 9156cfeede30e0d29e7ea2e1c355aa64c71b27be
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 12:18:51 2015 -0700

    Revert "Speed up a few animations"
    
    This reverts commit 01ac82090b2795c1a03808e7b586e883bb59c8dd.
    
    Change-Id: I0e009d32b56048926a86759b32d6fa37ca2c143f

commit fd210e7f778e31da80cc961bfe9d2ac0ebc20f4c
Author: Janson Kang <temasek71@gmail.com>
Date:   Thu Oct 31 07:33:49 2013 +0800

    Frameworks: Speed up orientation rotation
    
    Change-Id: Ic3de867e9e66f602d5ea565068c560d18678a8d4

commit af55d266dd3e1ca39523d86f2aeb03033e32098d
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Nov 5 17:51:11 2014 -0500

    Speed Up Windows Orientation
    
    Change-Id: Icbcb669147c5440ff185b6515bdf9c9be4e0edef
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 4e07557407b4b8c81dce0b35310282e94f569295
Author: rascarlo <rascarlo@gmail.com>
Date:   Fri Jul 26 10:57:37 2013 +0200

    use a solid black not a gradient as background
    
    Change-Id: I2ce84c370fa6277002f13c6c40374d70e5166c1a

commit a6d44a5ef40ee0f52b666da061412576969264c5
Author: zweif <gurkensindgruen@gmail.com>
Date:   Wed Nov 12 13:45:10 2014 +0100

    Fix lockscreen selection view in landscape mode.
    
    Added a dimen-value for selector in landscape-layout to fit screen. Issue is described here:
    https://github.com/LegacyXperia/local_manifests/issues/677
    
    Change-Id: I9501c91fed2660e947f1eae617f9a31d95766ed8

commit 31838b03ff4fc748ad55b5ff64410de2e9c2268b
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Wed Dec 25 03:04:18 2013 +0100

    Forward Port: Smoother Upload and Download Animation
    
    Change-Id: I6e6409cc85ad951019dbac10156d4aed92f4c5bc

commit 1485820e65463bf21218090e9969438c316d88e0
Author: willl03 <wgangers@gmail.com>
Date:   Mon Dec 8 11:13:28 2014 -0500

    Only go HOME if screen is fully awake
    
    Avoid going home when hardware home button is used to wake the device on an insecure keyguard
    
    Change-Id: I5d5d8c4fff76967c29e70251f7b165205005ba11

commit f4d276fea79a15bec66f1caef14cef5df97a532a
Author: dankoman <dankoman30@gmail.com>
Date:   Thu Dec 11 21:27:28 2014 +0100

    SystemUI: redraw navbar icons, add custom navbar icons back
    
    Patchset: add sw600dp versions
    
    Patchset: finish up the rest of the custom icons
    
    Change-Id: I0925fe7a348a8914757caaca6c97d85fb7337f7b
    
    Conflicts:
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search_land.png
    
    Conflicts:
    
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_recent_land.png

commit de50074e297b976ab0f5b820354ebc5991357343
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Jun 23 13:11:50 2013 +0200

    Fix ANDROID_LOOP=true for ArgoNavis and Perseus ringtones
    
    Change-Id: I2fd05e73d68758867a17d2c3369cfeefc203ac9a
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 62c754b913fb921f9e3aab61442af339b30db048
Author: Amit Pundir <amit.pundir@linaro.org>
Date:   Sat Jul 27 01:44:32 2013 +0530

    frameworks/base: Fix build in ISO C++11 mode
    
    Change-Id: I5d3ba44cc9faa5826a5a0a6b37c8f0eb2872e1ac
    Signed-off-by: Amit Pundir <amit.pundir@linaro.org>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 0c0009995a7fa07888987b30486900d67097622c
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Fri Nov 21 13:30:44 2014 -0500

    core:jni: Disable Strict Aliasing
    
    Change-Id: Icd7b0047af4d27cc0b8458efe18306aab3fae7d9
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 3c4a9ffd6c831838e7ab7165928339a6d634d991
Author: Chet Kener <Cl3Kener@gmail.com>
Date:   Wed Nov 5 17:56:09 2014 -0500

    Enable Non Market Apps/Disable Package Verifier
    
    Change-Id: I6a63b357af3535fbab41ab9128b771f2d8b97af0
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit be2f79fb08d406c6d39d840248d33c85a3e748ce
Author: Li Li <lli5@nvidia.com>
Date:   Thu Dec 19 14:57:36 2013 -0800

    bless python versions newer than 2.6
    
    Change-Id: Ic4bfb857586f1fd4aa9cfddf5984341a89b0cd4a
    Signed-off-by: Li Li <lli5@nvidia.com>
    Reviewed-on: http://git-master/r/347711
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Peter Zu <pzu@nvidia.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit efd93515cf34ff47cbb15fcc24eb31700e747a98
Author: Craig Gomez <craigacgomez@gmail.com>
Date:   Sun Nov 16 20:57:18 2014 -0800

    Enable Dessert Cake dream
    
    Change-Id: I987154631bab920698ee1d1c3e1d04d80b397ad7
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 0a7ba1dc626fc88f95f2cacad55b75aa5992b2f0
Author: tiger_huang <tiger_huang@htc.com>
Date:   Thu Oct 23 20:24:19 2014 +0800

    Prevent wrong system ui visibility callback after the user swipe
    
    If we return vis without clearing clearable flags, it will be set to
    IStatusBarService in updateSystemUiVisibilityLw(), and then be
    callbacked to WMS via statusBarVisibilityChanged(), and then be
    dispatched to the client; which is wrong because WMS should dispatch
    the new value to the client, not the old one.
    
    https://code.google.com/p/android/issues/detail?id=79991
    
    Change-Id: I2a06d1fbe66e854e639d86a39784f8c6a3303674

commit e83ec31a8ab8d6fc69e5438f22ff9ad8ae79b2a0
Author: dankoman <dankoman30@gmail.com>
Date:   Sat Apr 4 14:10:57 2015 -0700

    Frameworks: add shortcut action icons
    
    Change-Id: Ib4b70241675e65e9f080f193da4523ca5be670b7
    
    Conflicts:
    	core/res/res/values/cr_symbols.xml

commit 19dd63526738b309f2f438744ed1919f597dedd5
Author: Elliott Hughes <enh@google.com>
Date:   Wed Dec 17 16:17:19 2014 -0800

    Remove a bitrotted test.
    
    Change-Id: I4c44f2da0544dbfde8e340f7f477191725c5fb8b

commit 781a94d799a7e276095f4234b40a854c881d682f
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Thu Nov 13 22:46:12 2014 +0100

    SystemUI: Tiny expanding improvement
    
    Change-Id: Id58d12bfb71b8e1de4fabd5bde8b1e71e6373d76
    Signed-off-by: BigBrother1984 <carlosavignano@aospa.co>

commit ddb9d260b4fb3acb9624e263bfe930e3ef553b18
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Mon Dec 22 21:40:21 2014 +0100

    SystemUI: This TODO can be solved actually
    
    Signed-off-by: BigBrother1984 <carlosavignano@aospa.co>
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Change-Id: Ic7357eaa38f6917f26b92a36b5fd8b283d8ebf4b

commit 0b9b6d05553f1b9e220d363ede3323b298073202
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Sun Apr 5 19:34:16 2015 -0700

    [1/2] Base: implement App circle sidebar
    
    add whitelist app to include into circle view
    rebased
    make standalone patch
    
    PS.15 : rebased
    PS.16 : cleanup
    
    Change-Id: I08d2a3a7e0f8df20e801e585d4cac8547a740a3e
    
    Conflicts:
    
    	packages/SystemUI/res/values-land/cr_dimens.xml
    	packages/SystemUI/res/values/cr_dimens.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/values/cr_styles.xml

commit a882930f60f3df28915b3e71fe315cc63c3f17ec
Author: zeetherocker <zeetherocker@gmail.com>
Date:   Sun Apr 5 19:46:49 2015 -0700

    Support for Configurable Trigger Region
    
    Change-Id: Ib89a98e607f48108b1a1fb54f00335a3bc4ff2e7
    
    Conflicts:
    	packages/SystemUI/res/drawable/ic_livedisplay_outdoor.xml
    	packages/SystemUI/res/drawable/trigger_region.xml
    	packages/SystemUI/src/com/android/systemui/appcirclesidebar/AppCircleSidebar.java

commit f389d3da8d01af1835d879eb902137d54e1c4ccf
Author: Stevespear426 <stephen.k.spear@gmail.com>
Date:   Sun Apr 5 19:49:30 2015 -0700

    Base: All in One Animation Control [1/2]
    
    Allow configure System, ListView, Scroll, and Keyboard Animation
    
    * System from
      AOKP Animation Control https://github.com/AOKP/frameworks_base/commit/015c9cf00a8e49aea22d70b57b0af87c9134be73
      thanks to Steve Spear <stephen.k.spear@gmail.com>
    
    * ListView Animation https://gerrit.omnirom.org/#/c/2863/
      thanks to jkl5616<jkl5616@gmail.com>
    
    * Keyboard Animation https://github.com/zst123/XuiMod/commit/975cd531a9a847769b2af306495643a55ec44aaa
      thanks to zst123 for patches
    
    * with slight modification to OmniRom
    
    * Scrolling Animation https://github.com/zst123/XuiMod/commit/48c180cfa762617f59b4ceb3da50a6c28befe24f
      thanks to zst123 for patches
    
    * add toast animations
    
    * add separate option for them
    
    Change-Id: I89d880250867c41aecbb4cbe3ba1d473e780ebb4
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/java/android/view/ViewConfiguration.java
    	core/res/res/values/pac_symbols.xml
    	packages/SystemUI/res/drawable/ic_navigation_ring_vibrate.xml
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 06c069b46b47c3bede1d2c56181d564bc55ce552
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sat Apr 4 18:46:02 2015 -0700

    AOKP animations: Add an entry for TRANSIT_TASK_OPEN_BEHIND [1/2]
    
    Change-Id: I38247e34d82a3156b2f03845fdd9a9e39d9b0236
    
    Conflicts:
    	services/core/java/com/android/server/wm/AppTransition.java

commit f33f2cfad46ba3ee514c21cfbf09b3705f35e254
Author: BytecodeMe <hiasant@gmail.com>
Date:   Sat Apr 4 18:48:10 2015 -0700

    base: make animations faster by default
    
    *Why multiply the animation duradtion, which is 0, by 15 to get the actual animation
    duration which is still 0.
    *Just set mAnimationDuration to equal the AOKP.ANIMATION_CONTROLS_DURATION
    
    Much efficency. Wow. Very Zero Product Property.
    
    Signed-off-by: Andrew Warfield <hiasant@gmail.com>
    Change-Id: Ic33d80421285f2901429a0afb6d23e07741d65c2
    
    Conflicts:
    	services/core/java/com/android/server/wm/AppTransition.java

commit 456d4b41457d8d9cbc0a1121ade5a892c8a0e4dc
Author: Dirk Rettschlag (MarcLandis) <dirk.rettschlag@gmail.com>
Date:   Sat Apr 4 18:50:05 2015 -0700

    bring animation back from traveling in hyperspace
    
    Change-Id: I920f5e38ccf6bedb1fc242c7adbe9304798268d4
    Signed-off-by: Dirk Rettschlag <dirk.rettschlag@gmail.com>
    
    Conflicts:
    	services/core/java/com/android/server/wm/AppTransition.java

commit 65709164b6d513a34d6e9754753a5dff468410db
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 27 15:04:02 2015 -0700

    Themes: Create data/cm/ for CM specific test data
    
    Change-Id: I523845be1bf2cbe1c2f01fc1cb0e7d2a9d8ef1e1

commit c0a175844c248ba81c373eee01bfd48c85c9b46a
Author: d34d <clark@cyngn.com>
Date:   Tue Mar 31 14:46:46 2015 -0700

    VolumeUI: Call mContext.recreateTheme() on theme change
    
    This resolves an issue where the theme object is holding on to
    themed resources that no longer exist.
    
    See http://review.cyanogenmod.org/91826 for more details.
    
    Change-Id: I6a6fd560791de42cf2f89807800ea158f4c591af

commit ac54fa7236d177cfe403e4b5ec180101fa4b5dde
Author: d34d <clark@cyngn.com>
Date:   Wed Apr 1 16:02:41 2015 -0700

    Themes: Remove unnecessary query in updateWallpaper
    
    Not sure why this is here but it's not necessary since the returned
    cursor was never used besides calling moveTofirst()
    
    Change-Id: I95b579d89f3a77e2187cea498a4a22d67e6a3486

commit 5331338a5282aa620d1687913cd486fd9950b5d4
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Thu Apr 2 09:34:10 2015 -0700

    SystemUi: Nuke secondaryIcon.
    
      bb4a702e6 introduced a secondary icon that would allow
      for the manipulation of the ringer stream during specific
      active stream types.
    
      This duplicates functionality with our expandable volume panel
      and is not as effective as a utility, so kill it with fire.
    
    Change-Id: Ia74fc95a3886f4c57b8e632b7b26f7ade4247e41

commit 58cd82d62fe36f4953d939d5c381d51db9df7388
Author: Ethan Chen <intervigil@gmail.com>
Date:   Mon Feb 16 22:50:19 2015 -0800

    bootanimation: Set CPU boost hint
    
    Change-Id: Idaefc6fa5044afb3ca6b40e70e81cf01307adb51

commit e8818a5d6a64c9d401ee4530150d2c3240ca9669
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Fri Apr 3 16:11:06 2015 +0100

    Revert "SystemUI: fix nav button ripple getting stuck"
    
    This reverts commit 19040260713a8367a00d1d679843a2cf7f353098.
    
    Change-Id: I839c3cbbcbbe6bef11e099c62e6e5cc60320c41d

commit 7242c67a08f44bab6faf40ad84128bbb0a90b7e2
Author: Hamster Tian <haotia@gmail.com>
Date:   Sat Apr 4 16:21:09 2015 +0800

    SystemUI: remove redundant ic_qs_signal_hp.PNG
    
    We have vector images now. This png will lead to blurry H+
    in QuickSetting panel.
    
    Change-Id: I52e58f093e9bfe1c223e9b1df90edfa340ec287b

commit 2065070f0c1a949a27011ab554029871b936f123
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Dec 15 15:16:42 2014 +0100

    Frameworks: add ability to change the color in battery saver mode (1/2)
    
    User complain about the ugly orange....give the user the ability to change the
    color in status and navigation bar if battery saver mode is activated.
    
    Especially for you Tylog :D
    
    PS
    - move it into the observer...method is called to often to call every time
      the settings value for it.
    
    Change-Id: I48ed2e85c462a2e94770b2bc1ad75b1ca40f2304
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/BarTransitions.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit dcb26406df64b6937abccf705d9336cb3df9748d
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Feb 8 22:06:56 2015 +0000

    SystemUI: rework battery saver bar color feature
    
    Since we only want to enable/disable this the previous implementation didnt make sense,
    now checkBarMode will only change the mode to MODE_WARNING when this option is enabled,
    this also fixes bars resetting to orange when device is rotated.
    
    Change-Id: I15a61c49a2cb9874a6d9f5936e75e4930531da40
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 0103247e291076395bcc0e25b7f51b0ff3fc473d
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 23:38:25 2015 -0700

    fix build appcirclesidebar
    
    Change-Id: Iae06e574c3fd41a2cfb9cc5389fbb11863990c4a

commit 05e7e2650eb166768e0959d482bbfce72e62e3be
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Mon Dec 29 16:02:17 2014 -0200

    providers/Settings: getBoolean and putBoolean methods
    
    - We'll use them in AOKP custom animation and may use in other features
    
    Change-Id: Ie0edf6645ce8abef91a17b57203bf4c8bd2487f1

commit 470a5752549bb69b4688f6db3dede3bad0fd53cf
Author: jangwon.lee <jangwon.lee@lge.com>
Date:   Thu Feb 6 11:13:24 2014 +0900

    Correct a mistyped word "MSG_SET_CLEINT" to "MSG_SET_CLIENT"
    
    "MSG_SET_CLEINT" is mistyped, so correct it.
    
    Change-Id: Ib5eeaf7071e95db8b2375ca09d10420a5a445543

commit 1be3ee75bc26ce109396a7647c24249f0cb4098a
Author: justinmuller <justin.muller@acm.org>
Date:   Wed Oct 16 22:06:55 2013 -0600

    Fixed grammar in the comment that introduces the Debug.MemoryInfo class.
    
    Change-Id: Ic021e689b7a8c55367277875b321358535c04e6a
    Signed-off-by: justinmuller <justin.muller@acm.org>

commit 870aaaa6d6730a90ebf958cbaf72a40fcb538e49
Author: Seonggoo Kang <seonggoo.kang@lge.com>
Date:   Wed Dec 24 13:55:50 2014 +0900

    Prevent duplicated registration of OnComputeInternalInsetsListener
    
    OnComputeInternalInsetsListener is added when initViews is called,
    and initViews is called by onCreate and onConfigurationChanged.
    But it is removed only by onDestroy.
    Therefore listeners are accumulated and it results performance issue.
    So before adding, remove mInsetListener that was previously added.
    
    Change-Id: I494d3f1875613d73d3f9b8e2af286b5800f03196

commit b9c2b3358a0cc3e661a132688dd903a4a311b30d
Author: maxwen <max.weninger@gmail.com>
Date:   Wed Dec 3 21:31:17 2014 +0100

    base: fix battery stats wakelock crazyness
    
    Until someone explains to me why google has killed the
    since unplug stats for partitial and kernel wakelocks
    change them from beeing screen off based to unplug based
    
    Change-Id: Id727d5d9e237eecb7e86d7dee3285f18a57f9723

commit 1c4b9fdc7dc10941022a7b655405223d56020673
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Wed Dec 31 02:15:43 2014 +0100

    Status bar notification: Use Material icons for missed calls
    
    Change-Id: Ib6ccaaa87b90655be721d479cc2a9f03c63df866

commit 493e303efde9428a556d5c2597332010ca0ba8c4
Author: dankoman <dankoman30@gmail.com>
Date:   Sun Jan 4 02:46:02 2015 +0100

    SystemUI: add materialized navring drawables
    
    Change-Id: I222dfb420b660da1c45dd822d7e7398108b0932b

commit f5d829179cd3c21f9959edec2507a66e6166bd4a
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Sun Jan 4 03:07:39 2015 +0100

    Activity: Add an helper to get its handler instance
    
    Change-Id: I9cd0cf53ae74f52f924c7a2885cb4332532e1faf
    Signed-off-by: @BigBrother1984 <carlosavignano@aospa.co>

commit f81d25ce8218b6d2066ca48d5cfedc35d8a35e76
Author: David96 <davidlepplaweber@aospa.co>
Date:   Mon Jan 5 00:27:56 2015 +0100

    QS: fix tiles not being refreshed on overscrolling
    
    This fixes https://code.google.com/p/android-developer-preview/issues/detail?id=1860 I will later submit that to AOSP as well.
    
    PS2: better approach without exposing private method
    
    Change-Id: I53fa9cd9244d690f317da61bd4de89aa07915a56

commit 7374a1f1901d0dcc1d30ba706a6139083b301bb9
Author: Srikanth Chintala <srikchin@codeaurora.org>
Date:   Sun Oct 21 02:20:06 2012 -0700

    Telephony: Initialize GsmCellLocation class members properly
    
    Default values for class members mLac, mCid, mPsc would be 0.
    Initialize these variables with -1 as 0 is considered as valid value.
    
    CRs-Fixed: 406479
    Change-Id: Idb3d1737c7101b97a90eab3dc7436ee1806d0bc4

commit 9f49bdd46e764a55c20e365d5252ee9477530da3
Author: Carlo Savignano <carlosavignano@aospa.co>
Date:   Sun Nov 9 07:58:32 2014 +0100

    SystemUI: Underp AndroidManifest indenting
    
    Change-Id: Iffd2985e69ec07620095d149a360038f2ced22e3
    Signed-off-by: Carlo Savignano <carlosavignano@aospa.co>

commit 89aee78cc502e65d9c7c56577af5eb0b22e539ec
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Jan 8 00:57:02 2015 +0100

    Status bar: Update notification count icons:
    
    - Redraw all icons:
      - Use 18dp icons, (+ 1px for the nine-patch frame)
      - Update border color, (cc808080)
      - Fix xxhdpi icon size, (was xxxhdpi)
    
    Conflicts:
    
    	packages/SystemUI/res/drawable-xxhdpi/ic_notification_overlay.9.png
    
    Change-Id: Ic3c80d6cbebe1294debdb9a276eab34f2baad01d

commit 970357c14d20401add4781e231b450fa932dd652
Author: MartinRo <martin@rodemann.org>
Date:   Sun Jan 4 13:08:24 2015 +0100

    Policy: Fixed key action for launching camera
    
    Change-Id: Idf76d638c52382fc5e67ed77ded25e0477e7a008

commit 454db1433399d96fd585867b80d926eaaa51933c
Author: chad <guochongscut@gmail.com>
Date:   Sun Dec 21 15:43:01 2014 +0800

    bindService can't start up service process
    
    Issue 85758 https://code.google.com/p/android/issues/detail?id=85758
    
    Change-Id: I28645445ee5c46b2ab4cf78189f143ea97df63dd
    Signed-off-by: chad <guochongscut@gmail.com>

commit a3ede70cd6e48b209ab981d84d36e769ec25568f
Author: xplodwild <me@xplod.fr>
Date:   Mon Nov 11 02:07:32 2013 +0100

    DocumentsUI: Add a standalone File Manager
    
    This commit adds a standalone mode to the DocumentsUI, to let
    it act as a file manager/explorer.
    You can browse your storage contents, open files, and delete them,
    as well as do everything that the DocumentsUI can do (ie. sort
    by name/size/type, list and grid view, recents, search, ...).
    
    This gives us a consistent file browsing UX accross all apps
    that uses the new documents API.
    
    Change-Id: If73a3c100f010bdb766c843976d4fd3573ea805c
    
    Conflicts:
    
    	packages/DocumentsUI/src/com/android/documentsui/DocumentsActivity.java

commit 99fc61fa2b0c1752a7c19d4812d4fd451f6c12f1
Author: Alex <mazdarider23@gmail.com>
Date:   Sun Dec 29 00:34:10 2013 -0600

    Fix Icon size in DocumentsUI
    
    For XXHDPI devices if you go into Settings/Display and Notification light and select a custom value (application) you will see a GIANT icon.
    
    Before - http://i.imgur.com/DRkua3T.png
    
    After - http://i.imgur.com/f7xW4tY.png
    
    Change-Id: Ia355bddc515906134c8b3b4e67d381aaacceec78

commit f8d5a7d205f6cc4d2fbaebe495d8e9e2d6fc8113
Author: Yamil Ghazi <yghazi@gmail.com>
Date:   Tue Apr 15 10:19:29 2014 +0000

    DocumentsUI: Allow open files instead of URIs
    
    Check files' real path and mime type to open them only in standalone mode.
    This allows, for example, installing apks.
    
    Change-Id: I4501c694db84b8595cd3928752254a8914539972

commit fc7889c686e89a07ba02e57cf0a2e13d88d9efb4
Author: Felix Ableitner <me@nutomic.com>
Date:   Mon Apr 21 22:18:34 2014 +0200

    Replaced custom strings with Android defaults
    
    PS2: also replaced menu_cut/copy/paste with strings from android.R.string
    
    Change-Id: I7695b283faa66c6997fad372b31de2c678d222d0

commit 08e18f9e975b8b0b7266f58933ed24ab81836800
Author: Felix Ableitner <me@nutomic.com>
Date:   Sun May 4 16:20:11 2014 +0200

    DocumentsUI: Remove catch-all statements
    
    This removes several "catch (Exception)" statements which violates the Android code
    style guidelines and hides problems.
    
    I left some catch-all statements in, as they seem to be intended like this (grep for
    "catch (Exception").
    
    I suggest we do not merge this before we are sure that we fixed any problems. One problem
    is a crash when deleting items (I'm currently working to fix that).
    
    PS 2: Add exception to log.
    Change-Id: I483c320c7ee256acd993dd2a509c031fa5e3f09e

commit 734cff7d1d0ddc079eff5655f0681c7eee3f351b
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Jun 5 21:45:55 2014 +0200

    base: DocumentUI: fix a few issues handling remote content
    
    http://jira.omnirom.org/browse/OMNI-956
    http://jira.omnirom.org/browse/OMNI-950
    
    Change-Id: I8d50d71a9c91486dfc9e5da01538c6b5a626f054

commit 5b80a77200f4ee866b0c06e20bb7b8c67f3a7fe8
Author: maxwen <max.weninger@gmail.com>
Date:   Sun Jul 20 16:23:50 2014 +0200

    DocumentsUI: catch berserk apps on building recents
    
    We should not crash Documents app because of that
    
    Change-Id: Ie89a10c5005aef7f3e75a4f5a17f018e0fbc0814

commit 03f6d4ddbb2d8d79de83ddc3d0f55875b10814d6
Author: maxwen <max.weninger@gmail.com>
Date:   Tue Jul 29 02:10:00 2014 +0200

    DocumentsUI: fix recursive delete
    
    Create one DirectoryLoader in UI thread to use for delete
    
    Change-Id: I83a5811f152090f7812ad58ff4ee3bc13748d158

commit ee3fac074f0dfa83891898b64eda8863bd8c8e6b
Author: iceandfire <arhamjamal@gmail.com>
Date:   Thu Jan 8 23:44:39 2015 +0530

    DocumentsUI: Fix build and API changes for lollipop
    
    Change-Id: Ib4a2d70384985940de28c9d5864370080838ce19
    Signed-off-by: iceandfire <arhamjamal@gmail.com>

commit 83771d86cb7bcf46291508ac9661cc61e3a4f47b
Author: maxwen <max.weninger@gmail.com>
Date:   Mon Jan 5 22:27:21 2015 +0100

    base: DocumentsUI: catch NPE
    
    01-04 17:51:10.317 E/AndroidRuntime( 5924): java.lang.NullPointerException: Attempt to invoke interface method 'int java.lang.CharSequence.length()' on a null object reference
    01-04 17:51:10.317 E/AndroidRuntime( 5924): at android.text.SpannableStringBuilder.replace(SpannableStringBuilder.java:454)
    01-04 17:51:10.317 E/AndroidRuntime( 5924): at android.text.TextUtils.expandTemplate(TextUtils.java:912)
    01-04 17:51:10.317 E/AndroidRuntime( 5924): at com.android.documentsui.PickFragment.setPickTarget(PickFragment.java:85)
    01-04 17:51:10.317 E/AndroidRuntime( 5924): at com.android.documentsui.DocumentsActivity.onCurrentDirectoryChanged(DocumentsActivity.java:882)
    
    Change-Id: Iee201a8f5af7a58e4f8324e8c1847e091d45dc02

commit cc019a25ad96e52194610e4c47c48be02ca17549
Author: Tom Marshall <tdm.code@gmail.com>
Date:   Thu Nov 21 19:03:26 2013 +0000

    Allow custom density setting
    
    Use system property persist.sys.lcd_density to set custom density.  The
    custom setting affects the entire UI.  It is independent of
    ro.sf.lcd_density and has no effect on play store compatibility.
    
    Code distilled from PA project via PAC project.
    
    Change-Id: I8d26405d5d33bdf2890a0e9f67f113a4dc3e763b

commit 8e4a98d41b03a15fe734d8cfd0e531a357181b1e
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Thu Jan 15 00:26:28 2015 -0800

    Keyguard: Create lockscreen weather, move weatherimpl to utils.
    
    Change-Id: Ibf3fb8c877470ae152b778c9dc7bbf9aa6ae5f10
    
    Conflicts:
    	packages/Keyguard/src/com/android/keyguard/KeyguardStatusView.java

commit 4668940a320ab66e552afd32a57b96ab98c3f72b
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Mon Jan 19 19:25:16 2015 -0800

    SystemUI: Remove redundant and broken setText on temperture view.
    
    Change-Id: Iacb8a566a90bfb8cd13e10e70aeee818e7577b0b

commit 65575c2c982c26012fd0ce2093c87ee6515b588e
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Jan 18 23:09:08 2015 -0700

    core/jni: remove spacer at end of LOCAL_SHARED_LIBRARIES
    
    Change-Id: I0b04503d15e784643c18d81e83d88f25d4a665b5

commit 4c5dfdb08e4d0ef7fabb4bde8f239bf891655de0
Author: Valter Strods <valters.strods@gmail.com>
Date:   Fri Jul 4 15:10:19 2014 +0300

    Fix possible NPE in SyncHandler.onBootCompleted()
    
    If onBootCompleted() was called a second time, it would have throw a
    NullPointerException since the queue object would have already been
    set to null by the previous call. This commit just makes such an
    object behave as an empty queue instead of throwing the exception.
    
    Change-Id: I4472ff89a2a8dc93c3064210d2a49e0063f6efc0

commit 747e7090a244880636d6257d536498515b9ff5d7
Author: Sangkyu Lee <sk82.lee@lge.com>
Date:   Mon Jan 12 09:51:53 2015 +0900

    Fix ANR caused by hwuiTask thread
    
    If hwuiTask thread is exited while HWUI renders something,
    some tasks can remain unfinished forever.
    This can make ANR problem if RenderThread waits this kind of tasks.
    
    According to the current implementation, hwuiTask threads are
    exited when HWUI receives trimMemory() callback with level >= 20
    and some applications such as SystemUI can receive trimMemory()
    with level >= 20 even though they renders something yet.
    (For instance, when RecentsActivity in SystemUI is finished,
    HWUI receives trimMemory() callback with level >= 20
    but SystemUI should still render the status bar and navigation bar.)
    
    This patch prevents the tasks from remaining unfinished and
    make the tasks executed immediately if they cannot be added
    to their TaskProcessors.
    
    Change-Id: I5bd26439aa5f183b1a7c1ce466362e27554b4d16

commit 6bfc2cfbca5ac659803f992407be8bc1c67b84c1
Author: Henrik Baard <henrik.baard@sonymobile.com>
Date:   Tue Feb 3 09:25:28 2015 +0100

    Remove fall through for KEYCODE_VOICE_ASSIST
    
    Removing unintentional fallthrough for the case
    KEYCODE_VOICE_ASSIST.
    
    The code works today since KEYCODE_VOICE_ASSIST is the
    last case in the switch statement, however it is bad
    practice. If somone adds another case statement the
    code will break.
    
    Change-Id: Iee6234807bbe176bd94e2584de288105d6c6a7cb

commit b4746721e212e4ff84f9cef745a6a4225b7e51d7
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 00:00:35 2015 -0700

    SystemUI: Add permissions for reboot/recovery
    
    Conflicts:
    
    	packages/SystemUI/AndroidManifest.xml
    
    Change-Id: I3de20909725be91199e7375502b1d1621d96aaad

commit cc1240402429cdeaae7c64fe9c94d45259b4a38a
Author: Neil Fuller <nfuller@google.com>
Date:   Wed Feb 11 15:49:47 2015 +0000

    Remove usages of FloatMath
    
    Bug: https://code.google.com/p/android/issues/detail?id=36199
    Change-Id: Iec8fb663ed54eb967050f6ff25a36ba534204c4d

commit f45442e2db55edc283e7695759d1df944db26dec
Author: Pirama Arumuga Nainar <pirama@google.com>
Date:   Tue Feb 10 12:41:42 2015 -0800

    Store compiled code in Context.getCodeCacheDir()
    
    bug 16345623
    
    Use Context.getCodeCacheDir for EGL shader cache and RenderScript
    compiled code.
    
    Change-Id: I54c4e43674bd1f9342ae13059cb8899f4a3f4734

commit accd5753f1041b7cbc515525dca6a8fa317bca86
Author: Mikael Gullstrand <mikael.gullstrand@sonymobile.com>
Date:   Tue Nov 25 12:41:53 2014 +0100

    Call startInput on return from sleep mode
    
    One manifestation of the problem was that input string disappeared when
    returning from sleep mode. When editing a TextView with an IME in
    landscape orientation, the text would disappear when returning from
    sleep mode. The InputMethodManager would be deactivated when the screen
    was put into sleep mode as well as the input connection. However when
    returning from sleep mode the InputMethodManager was activated, but the
    input connection would not be activated again.
    
    The solution is to check focus of the InputMethodManager
    which will create a new active input connection to use.
    
    The change is however not specific to this one problem but fundamentally
    addresses the issue of lack of startInput on return from sleep mode.
    
    Change-Id: I95d05110bc1cf310fad23ea1bcbc5890f642d1fc

commit c58562693b4ba1c8af31b76fe4c83c72ce9055f7
Author: Neil Fuller <nfuller@google.com>
Date:   Wed Oct 1 11:55:10 2014 +0100

    Switch from FloatMath -> Math and Math.hypot where possible
    
    The motivation is an API change: FloatMath is going to be
    deprecated and/or removed. Performance is not the goal of
    this change.
    
    That said...
    
    Math is faster than FloatMath with AOT compilation.
    
    While making the change, occurances of:
    
    {Float}Math.sqrt(x * x + y * y) and
    {Float}Math.sqrt({Float}Math.pow(x, 2) + {Float}Math.pow(y, 2))
    
    have been replaced with:
    
    {(float)} Math.hypot(x, y)
    
    Right now there is no runtime intrinsic for hypot so is not faster
    in all cases for AOT compilation:
    
    Math.sqrt(x * x + y * y) is faster than Math.hypot(x, y) with
    AOT, but all other combinations of FloatMath, use of pow() etc.
    are slower than hypot().
    
    hypot() has the advantage of being self documenting and
    could be optimized in future. None of the behavior differences
    around NaN and rounding appear to be important for the cases
    looked at: they all assume results and arguments are in range
    and usually the results are cast to float.
    
    Different implementations measured on hammerhead / L:
    
    AOT compiled:
    
    [FloatMath.hypot(x, y)]
    benchmark=Hypot_FloatMathHypot} 633.85 ns; σ=0.32 ns @ 3 trials
    
    [FloatMath.sqrt(x*x + y*y)]
    benchmark=Hypot_FloatMathSqrtMult} 684.17 ns; σ=4.83 ns @ 3 trials
    
    [FloatMath.sqrt(FloatMath.pow(x, 2) + FloatMath.pow(y, 2))]
    benchmark=Hypot_FloatMathSqrtPow} 1270.65 ns; σ=12.20 ns @ 6 trials
    
    [(float) Math.hypot(x, y)]
    benchmark=Hypot_MathHypot} 96.80 ns; σ=0.05 ns @ 3 trials
    
    [(float) Math.sqrt(x*x + y*y)]
    benchmark=Hypot_MathSqrtMult} 23.97 ns; σ=0.01 ns @ 3 trials
    
    [(float) Math.sqrt(Math.pow(x, 2) + Math.pow(y, 2))]
    benchmark=Hypot_MathSqrtPow} 156.19 ns; σ=0.12 ns @ 3 trials
    
    Interpreter:
    
    benchmark=Hypot_FloatMathHypot} 1180.54 ns; σ=5.13 ns @ 3 trials
    benchmark=Hypot_FloatMathSqrtMult} 1121.05 ns; σ=3.80 ns @ 3 trials
    benchmark=Hypot_FloatMathSqrtPow} 3327.14 ns; σ=7.33 ns @ 3 trials
    benchmark=Hypot_MathHypot} 856.57 ns; σ=1.41 ns @ 3 trials
    benchmark=Hypot_MathSqrtMult} 1028.92 ns; σ=9.11 ns @ 3 trials
    benchmark=Hypot_MathSqrtPow} 2539.47 ns; σ=24.44 ns @ 3 trials
    
    Bug: https://code.google.com/p/android/issues/detail?id=36199
    Change-Id: I06c91f682095e627cb547d60d936ef87941be692
    
    Conflicts:
    	media/tests/MediaFrameworkTest/src/com/android/mediaframeworktest/functional/camera/CameraFunctionalTest.java
    	media/tests/MediaFrameworkTest/src/com/android/mediaframeworktest/functional/camera/CameraPairwiseTest.java
    
    Conflicts:
    
    	tools/layoutlib/create/src/com/android/tools/layoutlib/create/CreateInfo.java

commit 1d244f4ee5c8ce0c398d8540a61808bac3daccd2
Author: Neil Fuller <nfuller@google.com>
Date:   Fri Oct 3 09:38:24 2014 +0100

    Removing some more FloatMath references
    
    See frameworks/base commit 33253a4baa6279f81a73425b49dfb6abe5f5416e
    for details.
    
    Bug: https://code.google.com/p/android/issues/detail?id=36199
    Change-Id: I46d4ee4c4be7972e3bcc6782fb50f024b6fff1ee

commit f4a853459a83f49f8e72535c7c886ebd1ecbc023
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Feb 11 20:47:17 2015 +0000

    SystemUI: fix lock screen phone shortcut showing when target is set to none
    
    This issue only occurs on tablets
    
    Change-Id: I012e4e01844e2799a45c831749e832538a4b4e7b

commit dae72c4381e402f1ec6c234d420809d5f81cbf30
Author: Andreas Gampe <agampe@google.com>
Date:   Wed Mar 4 17:14:10 2015 -0800

    Frameworks/base: Add removeAll for ArraySet
    
    Add a simple ArraySet.removeAll(ArraySet) method. This avoids two
    allocations, a MapCollections helper and an Iterator object, over
    the removeAll(Collection) code.
    
    KeySetManagerService heavily calls removeAll during boot (about 9K
    times in AOSP). This reduces GC stress and optimizes the removal
    (about half the time the removed collection has only one element).
    The removal method in KeySetManagerService is also done under a lock,
    so that it gates parallelization efforts in PackageManagerService.
    
    Bug: 19498314
    Change-Id: Ib0e483adfd09831cd66ab19a820ebf6544a2b66f

commit 3315f8cfdd847591371aa692281ed4f79e6cc3ae
Author: Andreas Gampe <agampe@google.com>
Date:   Thu Mar 5 13:13:55 2015 -0800

    Frameworks/base: Use ArraySet more explicitly
    
    In KeySetManagerService, use ArraySet more explicitly. Avoid for-each
    loops.
    
    Collections API methods on ArraySet are not very efficient. Iterators
    incur two object allocations: a helper and the actual iterator object.
    During boot, about 4.5K such calls are made. Using the ArraySet more
    explicitly like an ArrayList/array avoids the overhead.
    
    Bug: 19617481
    Change-Id: I25df334fa1d4be3210667fb1404e3c43f2585049

commit 0780bcb7d4463613a901c99c855cb8a9c713b878
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Wed Mar 4 17:27:05 2015 +0800

    [ActivityManager] Skip receiver precisely.
    
    Symptom:
    Report broadcast ANR on a dead process.
    
    Detail and sample:
    http://code.google.com/p/android/issues/detail?id=158329
    
    Root cause:
    app.curReceiver can only remember the last running.
    If an application is both receiving FG and BG broadcast,
    only one of queue can discard, the remain one will still
    count as timeout.
    
    Solution:
    Select the skip-tartget-receiver by comparing the skipping app
    to the first record of mOrderedBroadcasts of each broadcast queues.
    
    Change-Id: Ic68d56f21b417a34f2d30d64ecfbed09c5e1764d

commit b2ea6b3a6eded477916601c0cc414caec87129a6
Author: Andreas Gampe <agampe@google.com>
Date:   Fri Mar 6 15:29:06 2015 -0800

    Frameworks/base: Remove unnecessary Pattern instance
    
    Using a static Pattern in ActivityThread prevents compile-time
    initialization of ActivityThread and GestureDetector, which depends
    on the former.
    
    It is also not efficient, as String.split has a fast path for simple
    splits.
    
    Bug: 19542228
    
    Change-Id: I5bb843c08c81e0d259bb8afafa87a8467bb1730e

commit 0ed2287f245fcb14bb377b74d1b6789dcf059646
Author: Andreas Gampe <agampe@google.com>
Date:   Fri Mar 6 15:53:06 2015 -0800

    Frameworks/base: Remove unnecessary Pattern instance
    
    Using a static Pattern in UriMatcher prevents compile-time
    initialization.
    
    It is also not efficient, as String.split has a fast path for simple
    splits.
    
    Bug: 19542228
    
    Change-Id: Ie9e5bfe6da04c6d05ec10b1426d0cd136ef46ef2

commit 9b62393b2b498c24fca94804b8c5f133c0b66b15
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Wed Mar 11 17:09:50 2015 +0800

    [ActivityManager] Fix index OOB when resetting removed task
    
    Assume task T has an activity X lives in process P.
    When P is died and before death recipient being called,
    start activity with flag RESET_TASK_IF_NEEDED to bring the
    existed task T.
    
    Then scheduleResumeActivity IPC will fail and trigger start
    a new process that removes task T.
    
    That results resetTaskIfNeededLocked cannot find the task
    when continuing the start flow.
    
    Detail:
    https://code.google.com/p/android/issues/detail?id=159558
    
    Change-Id: Icc400c7a6c481a3f78657e9fb83cf0c3a17dde68

commit 45c3af0aab86b3d2f66235fddc3c7434b49060f4
Author: ferro_chang <ferro_chang@htc.com>
Date:   Mon Mar 9 18:03:36 2015 +0800

    To call TypedArray.recycle() when we are done with the array.
    
    Change-Id: I6d672ce6c4e6521d82ef873ce69076b1f1cded56

commit 00a335536afd44321da6d8361c56b845b32859c0
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:10:23 2015 -0700

    Frameworks/base: Fix missing cast
    
    Without a cast, the division is integer division.
    
    Change-Id: I050e53778de8b1591a0be16ebbee8eed70eb1528

commit 8db8cd6959960115f02f2f3c96ae46446a90bfbf
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:19:43 2015 -0700

    Frameworks/base: Fix always-false equals
    
    Rect != Insets.
    
    Change-Id: I3d4ff890608e446b51f09a1b633af742f0c069d4

commit 0d168132784a63de2e6fa3da105b917c0ff85ca4
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:38:59 2015 -0700

    Frameworks/base: Fix a hashCode implementation
    
    Equals uses Arrays.equals. That means two responses are equal if
    the content of the data arrays is equal. By convention, the hash
    code of those objects should agree. In that case one cannot use
    hashCode on the array (which is the identity hash code).
    
    Change-Id: Icce8e2e71e9142421f5dac8a0ee8a211623fb704

commit de107ba47b15cfcc445b337b8fea6758d9fa117d
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:07:19 2015 -0700

    Frameworks/base: Fix null-pointer check
    
    Change-Id: I715a21c313e909ae654e0c1aa67bdf7bcd89de76

commit 284431ccce40b8a1f51acd0034c77c1181f57527
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:39:21 2015 -0700

    Frameworks/base: Use equals for Integer comparison
    
    Integer == is dangerous, as equal objects may not be identical
    objects. In fact, MediaFormat.setInteger was creating a new object
    every time.
    
    Change MediaFormat.setInteger and setLong to use valueOf, which
    may reuse returned objects.
    
    Change-Id: Iedcc6003adbf05c0c870aa4b3ada7f181a5b870e

commit a9b1aa6b28a2501ba9c601401e172b20d7e1aa3b
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:57:30 2015 -0700

    Frameworks/base: Check before foreach in Script
    
    According to the if below, ains == null is potentially valid. But
    the foreach loop would throw a NullPointerException.
    
    Change-Id: I4460fb1357eaa3abfe0ab9a21effb608f474ab51
    
    Conflicts:
    	rs/java/android/renderscript/Script.java

commit d19b1d1fcc2ee6fb780b10ebdefde598704a16ba
Author: jinchul.kim <jinchul.kim@lge.com>
Date:   Fri Mar 13 15:27:42 2015 +0900

    keep mDefaultDisplayMetrics from concurrent modification.
    
    getDisplayMetricsLocked can be invoked concurrently, it can cause
    concurrent issues like ArrayIndexOutOfBoundsException.
    
    Change-Id: I816eb4b276e7872c8a1964b6389a6f1238f51e48
    Signed-off-by: Jinchul Kim <jinchul.kim@lge.com>

commit 50289be5843216e074d2a221c0fbf408391e0742
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 20:17:07 2015 -0700

    Frameworks/base: Force long computation
    
    Ensure that an int-based computation is carried out as long.
    
    Change-Id: I23b10a95600674e8a5a65c0ea349afdc6aa152ae

commit 7d29a410f59f87a13744ae6cd8d0fd2b015b0522
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 18:04:41 2015 -0700

    Frameworks/base: Fix a comparison
    
    Change-Id: I80d62869920e77110c95f20369ec2631c75f6ed4

commit 2da6ed36885c3392638b7a335aee34ca9a5c7276
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:21:25 2015 -0700

    Frameworks/base: Fix trivial equals implementation
    
    The comparator's equal implementation doesn't satisfy the constraints
    of an equals method, namely being reflexive. Use the standard Object
    implementation instead.
    
    Bug: 19797138
    Change-Id: I74f888e99533e1945aab7ab10fe8ee3ded6388f4

commit 7483119e77dbbe38962590433f39a8530fd1e9c6
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 20:32:22 2015 -0700

    Frameworks/base: Use || instead of |
    
    Nothing wrong with | in this case, but || is canonical.
    
    Bug: 19797138
    Change-Id: I5f145736a5470f7cde06efce9a217d86eda2135f

commit 1d2c4a85512c0291ddcc197fcd1b5bea8b1808f6
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 13:59:50 2015 -0700

    Frameworks/base: Fix precedence bug
    
    Explicit cast has higher precedence than shift.
    
    Bug: 19797138
    Change-Id: Ifcf569bf774fbf65ee50c078f736ad167bcc6b8c

commit 8e0e3f8cee5fb1d754024e7923dae1cf0a1295bc
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:43:31 2015 -0700

    Frameworks/base: Fix format string in Camera
    
    One cannot print a boolean with %d. That will result in an exception.
    
    Bug: 19797138
    Change-Id: I86c42ea834cebebaecff8463637cc9de14d1fc88

commit 4f9bdf16a11d26b8046f4bad3fad0d5ccb8b2759
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 18:55:33 2015 -0700

    Frameworks/base: Make IDENTITY_MATRIX final
    
    Bug: 19797138
    Change-Id: I127f24b7060a0c4dab401ce8e3057d362c6d6b06

commit fc2c3d4680e456aa541c5e5a22e7e0f071f632a7
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:49:15 2015 -0700

    Frameworks/base: Fix format string in Geofence
    
    %p is not a valid conversion in format strings. It is also superfluous,
    as it is already known that location is null.
    
    Bug: 19797138
    Change-Id: I5784e28b05b4ca9aac57e0fc9da4a7f01d9b3247

commit f3cdb563d963803a2e4b41c985cd30804d2e360c
Author: Jason Sams <jsams@google.com>
Date:   Tue Mar 17 16:36:55 2015 -0700

    Avoid duplicate surface creation.
    
    Change-Id: I43104c8b48dd26681735940e6b2e1ba902af2020

commit 83d664d086648604a69dbdd934319764aac5b793
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 16:08:43 2015 -0700

    Frameworks/base: Fix visibility flag in Editor
    
    Fix double check.
    
    Bug: 19797138
    Change-Id: I95e694f384f1f25d6cf3b6a1669052940385e41d

commit 65d652230e5c6df4ea79399b0d6ac976b5109769
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 19:10:14 2015 -0700

    Frameworks/base: Remove duplicate check in Mesh
    
    Bug: 19797138
    Change-Id: I0b11c4ff63a8031d5e58a06ac13f91ae0bbac5dc

commit 5822eaccad5903f64a6154db7cb5d7f7840b294f
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:07:21 2015 -0700

    Frameworks/base: Fix potential NPE in InputMethod
    
    Don't read the size of an unchecked list.
    
    Bug: 19797138
    Change-Id: I9d8c087aff7bc9cc1e8aae9a0b489e23b5442765

commit 4dfef19f8456480d9d1267e16fcaaf9c35f43a0b
Author: longyu.huang <longyu.huang2014@gmail.com>
Date:   Fri Mar 20 00:35:41 2015 -0700

    third part apps can unlock the phone without password even if the phone has setted the password
    
    [Preconditions]
    set password or patten lockscreen
    
    [operating steps]
    1.install the app (eg QQBrowser) and connected wifi
    2.wait a while,the weather notification will shown on statusbar
    3.turn off screen,the weather notification will shown on lockscreen too.
    4.click the search bar in weather notification,it will disable lockscreen.
    5.press HOME button or kill QQBrowser in Recent apps,you can operate the phone
    
    Change-Id: I42689772b8a25c25b5dc0e4cca4c560e0d546ddc

commit 9c57ed7a65b8635c7440f05993474f4eb42fb2c9
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

commit dc4e39d5229bc9a65554b23097239253fad4cfd2
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

commit 488474d4484d6d2cb2fc0d08c33430664bdcc370
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 19:03:29 2015 -0700

    Frameworks/base: Don't allocate another identity matrix
    
    There is already an identity matrix in Matrix. Don't allocate another
    one for VectorDrawable.
    
    Change-Id: I51735f262d6680e043b0009707ec42acb2d0d1ad

commit 607030dfe6da32fdb4ea597fd1d51a55fe29b86a
Author: Raju Yadav <raju.yadav@sonymobile.com>
Date:   Mon Dec 22 14:54:13 2014 +0100

    systemui: Handle case when network has been lost
    
    If the network is immediately lost after becoming
    available the onAvailable callback may not yet
    have finished and is working with a lost network.
    In this case networkCapabilities may be null, so
    handle that.
    
    Change-Id: I588586ae0e844667cca4e2fd992d9694432a2198

commit eeef1c65a398a7edac139462d2ad991d532890f1
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

commit f00a4c9b5621662be128ba034b61eed354495986
Author: Mathias Jeppsson <mathias.jeppsson@sonymobile.com>
Date:   Mon Mar 23 09:00:30 2015 +0100

    Sort Bluetooth devices in quick settings by name
    
    To avoid Bluetooth devices moving randomly in list, sorting by name.
    
    Change-Id: I4f8e9f98fa29f9670678a3bb6051a6fcf7ae0b9d

commit aa85b77708a19df8d30cbac86cc78132d8924602
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon Mar 30 07:50:31 2015 +0800

    Revert "Make forward/reverse lookup default overlay"
    
    This reverts commit 66ef0e3abc8ed9c59553a1ae905e308118a679cd.
    
    Change-Id: I8c2e2b369b896e1409d20743982c758e12193543

commit 0d84c626550fd97d7a7d5a5033b0483417bd6efc
Author: Jason Sams <jsams@google.com>
Date:   Thu Mar 26 14:47:17 2015 -0700

    Fix potential npe
    
    bug 19805515
    
    Change-Id: Id36b145d3ce1c81311e88f5cdd2441880e98f737

commit 0eaaca3ab18734605d45335796f71ebe4998efda
Author: Jason Sams <jsams@google.com>
Date:   Thu Mar 26 15:29:56 2015 -0700

    Catch errors for unknown object types.
    
    bug 19805334
    
    Change-Id: I71e172b8123076896737d352403f8ddefca544b6

commit 28c07d9a568938058c60db533bb70ecaf711d24e
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:22:49 2015 -0700

    Frameworks/base: Fix request removal in VoiceInteractionSession
    
    Fix and simplify removeRequest.
    
    Bug: 19797138
    Change-Id: I0eca877e3109c9f39cebd4c888f166ce334fcc0e

commit 570b0381398ec5bf8e3c15d7110a42febfa933c8
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:47:42 2015 -0700

    Frameworks/base: Change String == to equals in Preference
    
    Bug: 19797138
    Change-Id: I496b12c425da45ee098db12e72ad843c22444ba3

commit 2867ab7c440fe21a4b099ce0f4a2d57852dd7685
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Nov 25 23:27:09 2014 -0700

    CPU temp (if available)
    for every core governor + online + freq
    
    PS3:
    increased font size
    
    PS4:
    whitespace cleanup
    
    PS5:
    more of that :(
    
    Change-Id: I8e2fd81edd8499eea2b1a6de8c042938387b33ef

commit 439350079048dd8d725a3fd98f0dbcc560e822f8
Author: kantjer <kantjer@gmail.com>
Date:   Wed Jul 23 10:45:21 2014 +0200

    StopSwitchDelay - Remove 5s Delay To Open Apps After Pressing Home Button
    
    Conflicts:
    	services/java/com/android/server/am/ActivityManagerService.java
    
    Change-Id: I86b882244dc5e240a2e94d651fa5366c43919dee
    
    (cherry picked from commit 6b51aa63f416cf5d1269055be010fee912824501)
    
    (cherry picked from commit 22edad0fdf92733b3e94965cc39be89123d878a7)
    
    (cherry picked from commit 83ef509cde02f62953858ed61611c22df7fe4d46)
    
    (cherry picked from commit 36483f62ca220c01012b69f125c84c46f470b289)
    
    (cherry picked from commit d8e7d48fefc5daaaf0cfeeb8a20acf74002b5865)

commit 0b9e39b79cc6facafff3c478241ff59c0cb97dcf
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 08:29:22 2015 -0700

     fb: less notifications sound (1/2)
    
    add back the 4.3 feature like it was.
    User can setup how often notification sound
    for an app comes trough so that
    it does not annoy to much
    
    (cherry picked from commit c9febc715df1f93e1bf5a80b36775f37ff000dde)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	services/core/java/com/android/server/notification/NotificationManagerService.java
    
    Change-Id: I6f30f180daf4483a11732f20fc9b98addec07558

commit 6d8f346eb2779a5d24f8c5990a16e8575c4a6225
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 13:53:41 2015 -0700

    Framework: safe headset volume option (1 of 2)
    
    thanks DvTonder
    
    Change-Id: I5355820a24d48c1d8f54ea17a7022d891ad07857
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit ea05603e5d4cdaf0816aee3354964964f9ea0715
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 13:57:09 2015 -0700

    Option to use volume keys to control media volume anytime [1/2]
    
    The volume keys control the Media volume rather than the Ringer
    hence removing the issue of accidentaly changing the Ringer volume.
    
    Credits: Pawitp
    
    Change-Id: I789e05bdb0bb7c968f71e4e10f4a759b3dbd0b59
    
    (cherry picked from commit ee22615ca993f369728f7b56cd135140b8892741)
    
    (cherry picked from commit d0e1e4608d3903981c884f49cb92edb054ea6c2d)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit ab00b27137bcf7f498dbda5edc2bfc1a26b5d5e7
Author: Meticulus <theonejohnnyd@gmail.com>
Date:   Mon Apr 6 16:48:28 2015 -0700

    volume steps: lollipop implementation [1/2]
    
    PS2: Rebase
    PS3: Move settings to PAC
    PS4: Never mind
    PS5: Move to PAC settings table
    
    Change-Id: Iad99653c8dc472370e88a829f5e86462f981efa1

commit 2823b897e797c1118e28534e39fa70cad2d93608
Author: KhasMek <Boushh@gmail.com>
Date:   Sun Nov 9 18:20:18 2014 +0100

    Lockscreen: Add timeout and instant lock option to slide lock (2/2)
    
    This adds AOSP's new timeout and instant lock options to the
    slide (aka chooser) style lockscreen.
    
    AICPfy:
    brought from kitkat
    
    Change-Id: I64b5f53a4e6c4098640b2c0cb3af2a56d6df019f
    
    (cherry picked from commit 1435c8be893eea29fb32033ced1fd48cc3cc01f3)

commit 4717621be97123c8689421edcaac7c5b89152734
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon Dec 15 19:57:37 2014 +0800

    Frameworks: Option to enable/disable scrolling cache
    
    (cherry picked from commit 101ae03becf4b8f4492aa60dfa2acf1e4d762ac4)
    
    Change-Id: I7404cea5af9ed3d1703947bcbcc087c4b02f8242
    
    (cherry picked from commit d09a0e55034cd849bad84df0e0b7264b1f28d767)

commit d5347c187895bb07ff182ac64e1d31fc74dcb66a
Author: Matt Filetto <matt.filetto@gmail.com>
Date:   Sat Apr 4 23:26:32 2015 -0700

    policy: don't allow app switch/recents key to be pressed on lockscreen
    
    Change-Id: I25223fef03896b86a4c56ec8abfbfc3b4591eaea
    
    Patchset: 4
    http://review.cyanogenmod.org/#/c/93464/
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 833a6c4e7f613e33142991ee1216f8984fb9a915
Author: tristan202 <tristan202@gmail.com>
Date:   Mon Apr 6 08:50:55 2015 -0700

    SystemUI: add back status bar date options (1/2)
    
    * Date style
    * Date format
    
    Signed-off-by: Altaf-Mahdi <altaf.mahdi@gmail.com>
    
    Change-Id: I03f70aa9f0c632727b4f1465842bb75839d0de46
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/Clock.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit baf28dc387a87d11af76c7c2a5a5a5ca588ce986
Author: tristan202 <tristan202@gmail.com>
Date:   Sun Feb 22 03:29:45 2015 +0000

    SystemUI: add back date style option (1/2)
    
    * 0 - Regular style
    * 1 - Lowercase
    * 2 - Uppercase
    
    Change-Id: Ia7773b9754f8c2cb843b9377e4f8dd25f68d7a69
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/Clock.java

commit 74bc5c34a8a74301e603653c33536f349706ed43
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 14:14:39 2015 -0700

    [1/1] enabled advance reboot default
    
    Change-Id: I391f2e9929998db15910e3a3addf37b8e5f4123b

commit 146cc7f1d5fd6c9b6ab252fc00d4df2aa94f8a25
Author: 0xD34D <clark@scheffsblend.com>
Date:   Mon Apr 6 14:16:09 2015 -0700

    [1/2] Screen Recorder
    
    http://forum.xda-developers.com/showthread.php?t=2547196
    
    Change-Id: I5bb81f909a44183fd8e011318f50a1b1e42c94e5
    
    Conflicts:
    
    	core/res/AndroidManifest.xml
    	core/res/res/values/cm_strings.xml
    	policy/src/com/android/internal/policy/impl/GlobalActions.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/res/res/values/cmr_strings.xml
    	core/res/res/values/cr_config.xml
    	core/res/res/values/cr_symbols.xml
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 8e1572d476029e26c1f17e0792cf58e73b5b40fa
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Tue Dec 30 20:53:43 2014 +0100

    ScreenRecorder: Update icons
    
    Thanks to @kantjer
    
    Change-Id: Id7a752a2a1edc7aa384addd19691981f52b1cf5f

commit fa6f2e02ceecf85502bb14621f725228f60a5aa7
Author: Janson Kang <temasek71@gmail.com>
Date:   Thu Jan 8 16:49:57 2015 +0800

    Screen Recorder: Catch NullPointerException
    
    Change-Id: I316de00ba7761fa627071e53964412d653830c32

commit 38c63104261b9ba6833c357339ae8592dbf8e931
Author: maxwen <max.weninger@gmail.com>
Date:   Mon Apr 6 14:25:33 2015 -0700

    [1/2] base: storage notification enhancement
    
    -allow hiding storage removed notification
    this notification can be pretty anyoing e.g. for
    usb otg storage devices
    
    -ongoing mount notifications for removable
    storage devices
    
    -to prevent unnice resizing when using progress in
    the notification change the notification layout height
    of the progress bar to be the same as the text line
    
    Adapted from
    https://github.com/TeamBliss-LP/android_frameworks_base/commit/34acc0e8a191c41e430aba2e7883cb1d8729c208
    
    - AICP'fied by merging with existing logic.
    
    PS2: Commit message updated
    
    Change-Id: If6401cca67155fe14d4db01eadac81ca3b55e8cf
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/values/strings_aicp.xml

commit 04e776db864fc6e1dec86cad655aa99466052b6b
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Mon Apr 6 16:01:02 2015 -0700

    [1/2] Base: Configurable overflow menu button
    
    Forward port from SlimBean. It was part of the hardware key custom rebinding.
    
    Change-Id: I9c6307041a4580ae85c27e3f979721c96a7ae219
    
    Revert "Always show overflow buttons on action bars"
    
    This reverts commit ea04f3cfc6e245fb415fd352ed0048cd940a46fe.
    
    [1/2] Base: Extended configurable overflow menu button
    
    Change-Id: Id33c2f83af24affa7cee3e1d552d76b368dba2d0
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/java/android/view/ViewConfiguration.java
    
    (cherry picked from commit e768d13d3c333e7ff117c0c377f2b63740685115)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    (cherry picked from commit 7f567e8cfefd2efea7cc1674b1cbc1d755c4e2e1)
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit eecb2c2100b78344479929d582065c7ffa873547
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Sun Mar 31 16:26:31 2013 +0200

    Forward Port: Add Camera sound toggle [1/3]
    
    Change-Id: I9e90f606d528eea08a41c35e75cd189e765c5d97
    
    (cherry picked from commit 44dbdef0b7d91b508bf833667ce79d3f5ac89cbf)
    
    (cherry picked from commit f4d1d70a3e993efb6f21c42ed2c2433ba00aeadd)

commit 89d7695d82c2ea3b4c3d3a50cc46d0d01593339f
Author: Owain94 <jerrywsullivan@gmail.com>
Date:   Mon Apr 6 17:01:29 2015 -0700

    Fix custom volume steps setup
    
    Change-Id: Ie282b6d055e2044759a6311d0fe2f6e653b5a29d
    
    Conflicts:
    	media/java/android/media/AudioService.java

commit b1991c4fcda52e87e2645ff7712de86fc3939db3
Author: Owain van Brakel <owain.vanbrakel@gmail.com>
Date:   Fri Jan 2 22:02:05 2015 +0100

    Fix volume step scaling
    
    Change-Id: I6e5bd767b7e122284257a770161bfb13ccb0f1e2

commit 6446ab20d635b0401e912561425baff4006f7eb3
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 17:05:18 2015 -0700

    Frameworks: Disable Quick Settings on secure Lockscreen (1/2)
    
        We have a lot security guys as user due of using the phones as business phones...that
        said a lot complains go into the direction of google how it is possible to have
        access to quick settings on a secure lockscreen which is absolutely understandable
        due that you are able to control Wifi BT AirplaneMode data etc.
    
        This patch takes care on this problem and adds an option to control this behaviour.
    
        ATTENTION: Due that this is really an UX derp for an average user this feature is
        enabled by default now. User need to disable it explicit in settings to get on secure
        locksreen the original android behaviour back.
    
        PS2:
        - fix derp
    
    credit: @kufikugel @Nick0703
    Change-Id: I2056bfd6c6f369b6ba9269c44bd232dfa8e8254e
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/NotificationPanelView.java

commit 3b7edeb81c0383bc916e3e052e7758de32436a7a
Author: LuK1337 <priv.luk@gmail.com>
Date:   Sun Apr 5 13:19:08 2015 +0200

    Fix FC after starting screen recording
    
    mDialog seems to be null in some cases so it crashes everytime you start screen recording.
    log: http://pastebin.com/UCdSumAD
    
    Change-Id: I8dfc006311aeebb881d54f36bfadf78b2e841026

commit 3b4f84a262cc081d9a6e1b4958e695308d0e35c0
Author: Ajay Kumar <ajayku@codeaurora.org>
Date:   Tue Mar 17 16:48:02 2015 +0530

    Bluetooth: Handling Null profile references before connect
    
    Handling the Null references of profiles before connecting.
    
    Change-Id: I52a991eedd4c25381c67eec570a774a94fe0d6b7

commit 1562fe82ff94b93c6192f7211b1591af7b0e9d3f
Author: Preeti Ahuja <preetia@codeaurora.org>
Date:   Fri Mar 13 16:00:58 2015 -0700

    Handle NPE in TelephonyManager
    
    ITelphony service instance could be null at boot up
    when device activation is taking place.
    
    Change-Id: If72622a2d22a20b1ce909134ce4c6446b132dffe

commit d5a8ab17c484f67d1b97a1e5055a3ad04ca4ddb4
Author: tsubus <tsubus@ilwt.org>
Date:   Mon Apr 6 23:18:08 2015 -0700

     Base: Implement ad blocker [2/3]
    
    *Hosts File Manager
    *Picked from Dirty Unicorns
    *This uses two prebuilt hosts files and switches between them by symlinking
    
    Change-Id: I23a1d9f1dcca623a556defb5eaae94f4e9e3b21d

commit 04cab7b8a843d35bf3b138e245ef96d06f3f35ab
Author: Dragon <dragon7780@hotmail.nl>
Date:   Sun Jan 25 22:56:19 2015 +0100

    Allow disabling of FC dialogs [1/2]
    
    credit: jmztaylor
    
    Change-Id: I70631d8864fabe5a7b0f6c2dfde4389cdfd1c6f8
    Signed-off-by: Dragon <dragon7780@hotmail.nl>
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit a0a96d33be50d8d0156da93970115fdaeeeb309a
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Wed Jan 14 19:47:21 2015 +0000

    Privacy guard: option to disable notification (1/2)
    
    Conflicts:
    
    	core/java/android/provider/Settings.java
    
    Change-Id: I3f4ca92dc9f6a53f09d84e1deb86e0d88e68d68c

commit 7d73f541764930612e0945d218ba2bd14d340f3e
Author: Gianmarco Reverberi <gianmarco.reverberi@gmail.com>
Date:   Tue Jan 20 19:07:54 2015 +0100

    Wifi: add option to show quick settings detail view (1/2)
    
    Added a switch preference in notification drawer settings
    to enable detail view for Wi-Fi tile
    
    Change-Id: Ieb1ff1fe5d7c8af802677ddfb7c5788306fe0b62

commit d51049dad2e9c6f18bf23bbd2b86f71fc23d4099
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 14:31:04 2015 -0700

    Quick Settings: Auto collapse panel (1/2)
    
    Since we have some tiles which display detailed view like CellularTile I've
    added the call to the tiles which will use it instead of globally.
    
    Signed-off-by: Altaf-Mahdi <altaf.mahdi@gmail.com>
    
    Change-Id: I6d8ecbed72bacfe034f423d5aebf94baa17efff4
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 064101ab9733404727052e7a5bc20efcd8fa90c9
Author: dankoman <dankoman30@gmail.com>
Date:   Mon Dec 22 23:09:45 2014 +0100

    Frameworks: port SlimSeekBarPreference
    
    Patchset: materialize slider preference
    Change-Id: I84c16cee9162a3fd53c0b62398a2ca03415ce974
    
    Conflicts:
    
    	core/res/res/values/cmr_strings.xml

commit 880efd3a87cf2c714ef5c679b1673147bec1830c
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Mon Feb 2 17:08:41 2015 +0500

    Update API
    
    Change-Id: I5adfe0b2d58174824b5bc8156edf87b80e2a09dd

commit 1eafeb046b72d997022bbbf336099f03e28a5191
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Tue Apr 7 01:09:37 2015 -0700

    SlimSeekBarPreference: Fix broken link
    
    Change-Id: Ic01e36df9c8f818168fc3724b63b733eefb3c528

commit 0c0196898db3754e61cc4139923c1787e8f11767
Author: dankoman <dankoman30@gmail.com>
Date:   Mon Jan 26 00:05:08 2015 +0100

    SlimSeekBarPreference: clean up a wee bit
    
    Prevents FCs citing a null object reference.
    
    Change-Id: Ica22754a93d4b0701b5d120f11ddf8bf0b48240c
    
    Patchset: 3
    https://gerrit.slimroms.net/#/c/24054/

commit 8a31ed2b21f5b1f0cf074b2892cb83364975c9df
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 14:32:40 2015 -0700

    [1/2] Quick settings: Add Haptic Feedback to tiles
    
    Change-Id: I792a00a2689a572110963db00362f8e9d77b316
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/QSPanel.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit d5a87bb3044b29f85f03566c530ff19b9a3bc6a0
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Fri Jan 2 00:16:07 2015 +0000

    SystemUI: extend qs haptic feedback option to Status Bar Header
    
    also add it to detailed view toggle and buttons
    
    Change-Id: I7723d938adeede8a377bca0adaff70a106079041

commit ea33b29518de8a158ed1546f3f828c9165ff9e50
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Sat Jan 17 20:14:15 2015 +0500

    QS: Squashed from EuphoriaOS (1/2)
    
    Change-Id: I69b2932f71f9d0d5797a80397563fef9f9297148
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/qs/tiles/RotationLockTile.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/StatusBarHeaderView.java

commit f14f705d425489045d7e9d3220919fbe878a8983
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sat Jan 31 21:49:21 2015 +0000

    QS: add Screenshot tile (1/2)
    
    Change-Id: I5cefcd20391ffe8fb1bc40e92c522500e5315de7
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit e6c0730d92185c0acff3b00a7aa6537bf0199f11
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Feb 1 06:41:03 2015 +0000

    QS: Option to show four tiles per row (1/2)
    
    This also reduces the size of the ripple when using 4 tiles per row
    
    Change-Id: Id61d6f2b113feabda46f464d0eda51c811226dd8
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/qs/QSPanel.java

commit 3b8345bae06e76f7f34746c0c567c52958e4445e
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 14:07:52 2015 -0700

    QS: add Sync tile (1/2)
    
    Change-Id: I0c0bb51e736a01661566f1118f955e32eba96063
    
    Conflicts:
    	packages/SystemUI/AndroidManifest.xml
    
    Conflicts:
    	packages/SystemUI/AndroidManifest.xml

commit f7ead3f1d8fffae0eea7723907d370c50d8809f3
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 2 00:59:58 2015 +0000

    QS: reduce TILE_ASPECT when using 4 tiles per row
    
    This fixes the side padding issue and we dont need to adjust the ripple size
    anymore.
    
    Change-Id: I75d705567f2451b6c365b8abc6832ffd5ed52b96

commit 15a009cbb636f7c511e83d46cc5c940ac37e4e54
Author: Janson Kang <temasek71@gmail.com>
Date:   Tue Feb 3 22:39:53 2015 +0800

    SyncTile: Add quick collapse
    
    Change-Id: I8b8680459d1c0252c3501482248dab29e7652e43

commit 6919f0a5a321257c8b9ee5199546609c42112c93
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Feb 3 06:47:33 2015 +0000

    QS: don't resize dual tiles when using 4 per row
    
    let them use all the space
    
    Change-Id: I29dcc2ca910ab42ad81b236da736dc6e0636b4a7

commit ec52319effffabfe3c9ab9bf9a5bf5d8b9dd4c6b
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Fri Feb 6 10:34:47 2015 +0000

    QS: move all options into a SettingsObserver in QSPanel
    
    Since we have many options now in QSPanel it makes sense to use a SettingsObserver
    
    Change-Id: Ie72d5a476f24a7e590772031324af5b74a341a66
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/QSPanel.java

commit 622c32ecb15a4d70d8797a9fb4be681b88c2445e
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 9 13:32:00 2015 +0000

    QS: add Brightness tile
    
    * long press to toggle auto/manual brightness
    
    Drawables by Alexander Westphal <westphal.alex94@gmail.com>
    
    Change-Id: I173281dbaba5945f0f99071639ddccee6a6ca365

commit 9790b9d11c01784d95ffeb44642d64c34060aa32
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 9 13:39:52 2015 +0000

    QS: add Battery saver tile
    
    Drawables by Alexander Westphal <westphal.alex94@gmail.com>
    
    Change-Id: I7bb419ac5d135b27f9f35d4a7acdb452a197a68f
    
    Conflicts:
    	packages/SystemUI/res/values/custom_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit ac5643caa1cbf9bb319a7cba53588e18930a63c1
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 9 13:48:03 2015 +0000

    QS: add Screen off tile
    
    * Long press for power menu
    
    Drawables by Alexander Westphal <westphal.alex94@gmail.com>
    
    Change-Id: Ib40968ed38edeb26fa657c69106d446c6ebdb39e
    
    Conflicts:
    	packages/SystemUI/res/values/custom_strings.xml

commit 02482e1a1713eb8365565631d1238e3435b1635f
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 9 13:55:29 2015 +0000

    QS: add Expanded desktop tile
    
    Change-Id: Icb4ef73eea923acf9cde52f6c66750a26360f238
    
    Conflicts:
    	packages/SystemUI/res/values/custom_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit c1ea7bf030eec4e9afc6569087c298bafa7e8756
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Feb 9 16:02:34 2015 +0000

    QS: clean up tiles
    
    * fix Copyrights
    * add auto collapse to some tiles
    * add long click and secondary click to tiles that were missing it
    * change long/secondary clicks on cellular tile to go to DATA_ROAMING_SETTINGS
    
    Change-Id: Ifc27d5769aca70e9a93335b39c855a71c2e0a8dd
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/qs/tiles/AdbOverNetworkTile.java
    	packages/SystemUI/src/com/android/systemui/qs/tiles/LteTile.java
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/tiles/LteTile.java

commit 62b78e6be38cb81e9473d13afec91ff39c8b111e
Author: MrBaNkS <banksmi09@gmail.com>
Date:   Thu Feb 12 21:25:11 2015 -0600

    QsTiles : Brightness point to ic_qs_brightness_auto_on_alpha
    
    Change-Id: I217e44bc81eca28002ce7d99240b2f725bcdd461

commit 16e5d9497ecedf2dcc44accfea2f1e7c399106bd
Author: David Smit <dsmitty166@gmail.com>
Date:   Wed Jan 14 17:21:40 2015 -0600

    QuickSettings: Disable auto collapse panel by default
    
    Change-Id: Id374cbbd3a1942cd4a7d99d920972db27c821ca1

commit b884f474547827d43c0394fca8eab7bba4db8bbc
Author: Janson Kang <temasek71@gmail.com>
Date:   Sun Feb 22 11:20:28 2015 +0800

    Quick Collapse: Multi-user support
    
    Change-Id: I5ddcf4aa933084034533e05ad484e231fead6fa6

commit 13e9ce925685b0a7e08eaba66427386ac8436214
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Sat Feb 21 22:52:13 2015 +0100

    QSTile: Reboot/Recovery tile (1/2)
    
    Forward port from SlimKat
    
    Change-Id: Ia933ffd48c485a8a6ca72a3c60139b144ac80e90

commit b92729d5b8e77f0a37983dec55938ac807ae0445
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 7 15:12:24 2015 -0700

    base: remove duplicate Default string
    
    Change-Id: I91e11ae51042e06d9fd690dce786dd116da8119d

commit 1eb516c6706579374eee3a9715ef9110ccb28d87
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 7 15:41:21 2015 -0700

    base: QS fixed build
    
    Change-Id: I405b953129337e4041d31fe56d8e121574bf44f5
    credit: temasek
    LocationTile: Fix build after cm updates
    ProfilesTile: Remove duplicate longclick
    HotspotTile: Update secondaryclick intent

commit 13e589740c940ed7a08fa83c24ba7cb2c232a8b7
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Mon Feb 23 21:32:20 2015 +0100

    NotificationTile: Simple mode ring/vibrate/priority/silent
    
    Single press: Switch between ring/vibrate/priority/silent mode
    Long press: More detail
    
    Change-Id: I17c105be8d54339d23a31b40e82e8da049522272
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/qs/tiles/NotificationsTile.java

commit df8e89115c8427a4039798228e2553f606a68276
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Tue Apr 7 15:46:25 2015 -0700

    Quick settings customizations, (1/2):
    
    - Change accent color for SystemUI to deep teal 500, (ff009688)
    - Custom background color
    - Custom icon color
    - Custom text color,
      (this won`t change any text which is using the accent color)
    
    Change-Id: I8ccefddf5eb2d38297f385a7ea83752162a7c563
    
    Conflicts:
    
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/drawable/qs_background_primary.xml
    	packages/SystemUI/res/values/cr_colors.xml
    	packages/SystemUI/src/com/android/systemui/qs/QSDetailItems.java
    	packages/SystemUI/src/com/android/systemui/qs/QSPanel.java
    	packages/SystemUI/src/com/android/systemui/qs/QSTileView.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/NotificationPanelView.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/values/cr_colors.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/NotificationPanelView.java

commit c32564faf5a591cb4b0f4f04c814eab3505321b0
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Apr 7 15:50:12 2015 -0700

    QSColor: Improvements (1/2)
    
    Theme active visualizer tile icon
    Don't force transparent qs background
    Transparency switch
    
    Change-Id: I6c43e8838c1aa929cf0d77fd05527ea2df5f017b
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/tiles/VisualizerTile.java
    
    Conflicts:
    	packages/SystemUI/res/values/cr_colors.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/NotificationPanelView.java

commit 70ff22429eef9d6a57c0ec0816b024f0cf9b9038
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon Mar 2 19:23:06 2015 +0800

    QSPanel: Use getIntForUser
    
    Change-Id: Icb2d0025a2ebf3bf86589f7ab76afe9c8d91bbc6

commit 0fb22d433599dfbfa7984d303f11ac108cb0a11d
Author: rogersb11 <brettrogers11@gmail.com>
Date:   Sun Mar 1 16:20:26 2015 -0500

    Small update to qs colors from @XXMrHyde
    
    Pulled out of here https://github.com/XXMrHyde/android_frameworks_base/commit/0dcf2360f84c769f8c2a45ee1f669acbf41d5e22
    
    Change-Id: I20d61cd6eb9006b2656185c792390d34d70f10bf

commit bb119dc8cf7a7ea5d47d01d6ede97848096ee680
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Mar 2 20:18:52 2015 +0000

    QS: add a little delay when toggling expanded desktop
    
    gives the animation time to finish otherwise it stays on
    
    Change-Id: I6851c170029fd2f5ab73238ca8d03ccb6e9b4fc5

commit 801b00000269e0b38e21e077ee8739eafc29f139
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Apr 7 15:54:56 2015 -0700

    FWB: QS colors master switch (1/2) - VERY DIRTY
    
    Change-Id: I45156cdd94333343ea71a627d6964c511eec737e
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/QSDetailItems.java
    	packages/SystemUI/src/com/android/systemui/qs/QSTileView.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/NotificationPanelView.java

commit d6c9269c9f3639d490574c4364f9b5dc78a6e6f6
Author: linuxxxxx <io.nolinuxnoparty@gmail.com>
Date:   Tue Apr 7 20:17:07 2015 -0700

     Base: HeadsUp options [1/2]
    
    Includes:
    
    * Base: forward port Headsup options (1/2)
    
    -Global on/off
    -Blacklist and Do not disturb
    
    (by Adnan Begovic)
    
    * HeadsUp: fix settings not being applied after reboot
    
    blacklist and dnd setting were not being applied at boot
    clean up the SettingsObserver
    
    (by Altaf Patel)
    
    * My changes
    
    - Let user choose if headsup swype action hides or dimisses notification
    
    Change-Id: Idca8dd715b13838a8c59a31276bfe9445651d6f7
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/HeadsUpNotificationView.java

commit d89701cefeb8dae939c1de036bea5757359bf260
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Feb 2 07:41:44 2015 -0200

    Frameworks: Actually start to use HEADS_UP_REQUESTED extra
    
    Prepairing slim heads up feature, we do this here to allow apps to
    send a heads up notification no matter what.
    
    Google introduced this flag but is not using it in the actual API
    
    Take HEADS_UP_REQUESTED into account to indicate that this notification
    is a good heads up candidate.
    
    How to use it you can see in email or mms app
    
    Change-Id: I4a29404122ae12ab9b95e1d223911078a360b44e

commit 67ab9b7f6161369f0776835d8d24daf39a69a5bb
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Dec 25 06:36:14 2014 +0000

    HeadsUp: add timeout option (1/2)
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Change-Id: Ie1a85ad7b731b9fd102da1996b732e7fbaeb128f

commit 029af5441f031e188e70bc62fb3aeecec0681f55
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Dec 25 07:03:46 2014 +0000

    HeadsUp: do not show if notification drawer is visible
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    
    Change-Id: I07390c7164e000a53cb997f4ccaf6f0e59867b3e

commit 9bcea3a80ef73e98a2e8c80f38275a091e2d6944
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Thu Dec 25 16:56:57 2014 +0000

    HeadsUp: fix headsup for incoming calls
    
    Change-Id: Id993852db87caca9c4c241408a4517cde46ca8e1

commit 83ad3aa40ffa9dd874be86104f461bd50597d698
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Wed Jan 28 07:35:23 2015 +0000

    HeadsUp: check if headsup is attached and not null when adding view
    
    Change-Id: Ie906aaa78862a35c80695b54e2472e313ebd75cf

commit 65a3a80cbd178cbc1cc7de9648e86f950c590cda
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Wed Feb 4 21:01:34 2015 -0200

    [Heads up swipe] Disable by default
    
    Change-Id: I9b7ee37664ce99ef72f8c767b8cd077a9a621d86

commit 3ae02d917e9642aa8f86e2886fedce9fdf50340b
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Tue Apr 7 20:31:46 2015 -0700

    [Heads up] Add touch outside event
    
    - Codes to it was picked from here: https://github.com/AOSPA/android_frameworks_base/commit/b62eeedf6f99760f88ee62d6c163c92092f4294f
    
    All the thanks goes to @BigBrother1984
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/HeadsUpNotificationView.java

commit 129b32cf6cee138713dc15eb67d218bbbaf5605d
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Mon Feb 9 14:37:29 2015 -0700

    [Heads up] Touch outside to hide (1/2)
    
    Add an option for it
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Change-Id: I68edf125e9422a9a36a1ab9242a8bdd24e3b6b01

commit 8f412b3dd4e8ffdcdcd7a2a85c745049c9151a22
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Fri Feb 6 08:37:15 2015 -0200

    [Heads up] Don't show heads up while IME is showing
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    
    Change-Id: I1434ce426f0b2434f39ce77cea4c245220df56a5

commit f6afba10b6a8e5114cb52bb1a7a7fb38f6587336
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Fri Feb 6 08:41:10 2015 -0200

    HeadsUp: Don't reset Y coordinate and improve edge swipe readability
    
    * Resetting Y position seams to broke showing behaviour.
    
    Signed-off-by: @BigBrother1984 <carlosavignano@aospa.co>
    Change-Id: Ifcb6dfa33cc15436b3b90abe081468a43b188cf3

commit a4dffcc41cd8592dc486a7a1bf680fa3d3cf10ee
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Feb 6 18:11:46 2015 -0200

    Fix heads up dismiss not working
    
    The key was renamed here: https://github.com/crdroidandroid/android_packages_apps_Settings/commit/c3e36c077b0454ce56a64b5f9fa3b5fab50242b8
    
    Change-Id: Icb833efb5482e341fc60d885c19a669ab462e43c

commit 565ea48b6d5f54126a2025a68b5083d56ee8326f
Author: Janson Kang <temasek71@gmail.com>
Date:   Sun Apr 5 23:51:18 2015 +0800

    BaseStatusBar: Heads up fixes
    
    Change-Id: I2984d32105d1817242c18bd0d07638f3a5faa352

commit fe3a417899aaa5b0548e8cfe4a74e96e196de1d4
Author: dankoman <dankoman30@gmail.com>
Date:   Fri Jan 2 16:13:34 2015 +0100

    [1/3] Frameworks: Proximity speaker
    
    Change-Id: I8846e1d54b7f26f4322b91fc1ba20f3e5da465ec
    
    Patchset: 1
    https://gerrit.slimroms.net/#/c/22230/
    
    Conflicts:
    
    	core/java/android/provider/Settings.java
    
    (cherry picked from commit 8b3c5e19238e8c1f71dde36cd33fcc0061e494c8)

commit cefeb107f324f15666d0a104738633b667146ec7
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sat Jan 3 15:53:28 2015 +0000

    Base: don't kill an app if its currently pinned
    
    Change-Id: I893d58e5800b67d5f3b843b1e77681749936261a
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/83590/
    
    (cherry picked from commit 791c89ad18ec38e10ba35b0603bbbecc9fbea659)

commit 8e03b8e308c487d1d7611767ca83e78557c91bfb
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sun Jan 4 22:07:20 2015 -0200

    [Base] Add the ability to hide superuser status bar icon
    
    - Add a simple option to hide the su icon placed in status bar when a session is active
    
    coded by @cristianomatos
    
    (cherry picked from commit 2cd0d60cade56207940cb42fd69ec7997772f531)
    
    Change-Id: I69003ca47a0ba4489274c2eaa6661af361f600f3

commit a9233b3c9b793bbf7a551f743f79eefbc1b5c623
Author: lichti1901 <lichti190185@gmail.com>
Date:   Mon Feb 2 19:28:48 2015 +0100

    Navigation bar button color (1/2)
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/KeyButtonView.java
    
    Change-Id: I950d99f91f4700fe8da07d255b7fba05d59e36fc

commit af4da73e6a13a755f7b1779db698a727ba7fc3f7
Author: david <davidteri91@gmail.com>
Date:   Wed Jan 28 18:56:58 2015 +0100

    Base: add more drawables to Slim LockScreen Shortcuts (2/2)
    
    Chrome
    Github
    Paypal
    Youtube
    Whatsapp
    Messenger
    Office Suite
    Tapatalk
    
    Change-Id: I4788376cf8ebd4ac28ed43b355180c86a55069e8

commit 2a5573dfde1827d77cad20e3f76d0b69b970b3c5
Author: jukiewalsh <xxxwilsonxx@gmail.com>
Date:   Thu Jan 29 00:56:00 2015 -0500

    base: add snapchat icon [2/2]
    
    Change-Id: If532e03f19b60523dcfd1d243fbc85766eeba468

commit dd304587d350f05f74e5c63cfcb5c115b6d49c43
Author: David96 <davidlepplaweber@aospa.co>
Date:   Wed Feb 18 17:19:03 2015 +0100

    Themes: Fix bootloop when applying theme fonts
    
    Should probably be submitted to CM as well, but I didn't get to testing
    it on a CM build yet.
    
    Change-Id: Ife95ab4942e6b179c9ab823dc26d3b8ac4eb535d

commit ffd8c658c3de90943f4cee98be717f0ab1f6a99c
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 26 20:51:24 2015 -0700

    Frameworks: cmremix up sounds and update (1/2)
    
    Base on Frameworks: slim up sounds and update (1/2)
    Till now we modified always the aosp make files etc. Was complicated to maintain.
    Hence we add now an own slim folder and own AllAudioSlim.mk to mainatin it completely
    ourselves.
    
    As well reduce size etc etc
    
    Change-Id: I0d60a0abe0935f1000016bc5d69b4f4e36616941

commit 72239965903d6a21b735dc31cfdcc0f2031a46f3
Author: Libin.Tang@motorola.com <Libin.Tang@motorola.com>
Date:   Wed Dec 17 22:47:45 2014 -0600

    IMS: add the api to get IMS registration information
    
    Conflicts:
    	telephony/java/android/telephony/TelephonyManager.java
    
    Bug: 18668325
    Change-Id: Ie694c7f1cc12a573cbef2815199ae6c91cf8088e

commit 711a54066f44c2321a8b8973e2a5be84db53682e
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Apr 6 21:33:11 2015 +0200

    base: fix BluetoothControllerImpl formatting issues
    
    Change-Id: Ia61ce35ddda46997e07bcbc87fff992bdaef10ba
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit c6b751670a599733eec86eefd352710ed483a784
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Thu Apr 2 16:43:13 2015 +0800

    [ActivityManager] Avoid improper resume top activity.
    
    When there is a process died, only resume top if
    it contains visible activity.
    
    This can fix case 1 in
    https://android-review.googlesource.com/#/c/120901/
    
    Change-Id: I45584e76f9e863980d04bbb593d7d26a8900acd0

commit 2f889d34a154c2ce2b241c81e7a48d668e7b0ae2
Author: tiger_huang <tiger_huang@htc.com>
Date:   Tue Mar 31 22:09:49 2015 +0800

    Prevent infinite layout and wallpaper flashing
    
    The original logic would cause mTopFullscreenOpaqueWindowState to be
    hidden in PhoneWindowManager.finishPostLayoutPolicyLw(), and to be
    shown in WindowAnimator.updateWindowsLocked() continuously if there
    is a show-when-locked dialog.
    
    The wallpaper would be hidden after the original wallpaper target is
    hidden, before the new wallpaper target is shown.
    
    https://code.google.com/p/android/issues/detail?id=162495
    
    Change-Id: I918e0fa03eec38d9f0c07150c17013c6c21683cb

commit ea35bb2ba5c3f4518b32d749025ecfcbd545c54b
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Wed Apr 1 18:58:07 2015 +0800

    [ActivityManager] Reduce report wrong anr activity
    
    Symptom:
    Report ANR on wrong activity.
    
    Reproduce steps:
     (All launchMode, taskAffinity are default and
      without additional intent flag)
     Case 1:
      1.Launch activity A from launcher.
      2.Activity A starts B activity.
      3.Press home key.
      4.Launch activity A from launcher (B is top).
      5.Press back key twice to finish B and A,
        A sleep 10s in onResume.
      6.ANR will report on launcher.
    
     Case 2:
      1.Launch activity A from launcher.
      2.Press home key.
      3.Kill process of A.
      4.Launch activity A from launcher.
      5.A sleep 10s in onResume, press back key immediately.
      6.ANR will report on launcher.
    
    Possible root cause:
    Focused activity will not be updated every time when activity
    resumed. (the condition to call setFocusedActivityLocked)
    
    Case 1:
    Launcher was stopped and not waitingVisible due to launcher
    is not the previous one, then getWaitingHistoryRecordLocked
    has no chance to correct the real ANR activity.
    
    Case 2:
    Due to process of next activity is died, bring existed
    task will not set mResumedActivity (it will be set when its
    process is started), so when assigning waitingVisible from
    processStoppingActivitiesLocked, the return value of
    allResumedActivitiesVisible will be true even there is no
    mResumedActivity. That results set waitingVisible to false
    to previous activity (e.g. launcher), then also cannot
    correct ANR target as case 1.
    
    Change-Id: I0b24f46a8fab266382ebc6e2ed84ebeca9358768

commit 6aad3e2a7c2af3a5fc6293de4f5d53b08a62fafc
Author: louis_chang <louis_chang@htc.com>
Date:   Tue Mar 31 15:18:21 2015 +0800

    [ActivityManager] Examine bad process before clean up application
    record
    
    Symptom:
    Unable to launch activity
    
    Root cause:
    There are some cases that would start process while pid
    assigned or already running. So the previous application
    record will be clean up via handleAppDiedLocked(), but it
    won't be removed from ActivityManager.mProcessNames since
    the process is supposed to be restart later.
    
    However, if the process is started from a background
    operation and has named as a bad process, it silently fail
    the launch. Then, the process won't ever be request to
    start afterward. The process status is app.pid > 0 and
    app.thread is null.
    
    The application components are unable to launch since then.
    
    Solution:
    Examine bad process before clean up application record
    
    Change-Id: I53dc06e49254094abc06e460c8b8b33f36803601

commit 197955ab77b43968523459c73d128d902d1aaecc
Author: louis_chang <louis_chang@htc.com>
Date:   Thu Mar 26 13:31:14 2015 +0800

    [ActivityManager] Fix ServiceRecord leakage
    
    Symptom:
    The first step of cleaning up application services is
    to clear the app state from services (which set sr.app
    to null). Then it clean up the service connections.
    In some scenario, the Service might be removed during
    the connection cleanup (i.e. the Service is no longer
    needed). In that case, the Service will be removed from
    ServiceMap, but won't be removed from r.app.services in
    bringDownServiceLocked(line 1670) because the r.app is null.
    
    Solution:
    Remove the service connection first.
    
    Change-Id: I644d73af58fe0e7c1c4a6c9779fe6b5d747b880d

commit 4f29eb864a38cfc024b90e524bd3624c9f0292ab
Author: younghwan1.kim <younghwan1.kim@lge.com>
Date:   Thu Apr 2 19:15:11 2015 +0900

    [ActivityManager] Do not add service to reschedule after removing users.
    
    Some service which has persistent attribute has restarted again and
    again after removing users.
    but it dies right after launching because it is not valid in owner mode.
    
    This patch will check service's userId whether userId is alive or not.
    And then if userId is not alive, then service will bring down.
    
    Change-Id: Id99bf3c651b88e377f1fd6bec8aaad81318d7579

commit 15cb44c8570313d7f2a11b77eb5556fb4e5d8a13
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Tue Apr 7 11:30:09 2015 +0800

    [ActivityManager] Improve task order of getRunningTasks.
    
    Symptom:
    During switching task in same stack, the first result
    of getRunningTasks will be the behind stack's top task.
    e.g.
     App Task X is starting task Y, the first entry may be home.
    
    Root Cause:
    TaskRecord's lastActiveTime is updated when pausing
    or resuming. When X task launch a new task Y, Y is
    on the top of task history, before X complete pause,
    Y's lastActiveTime will be 0 because it is a new task.
    Then when comparing the front task with other stack,
    other stack will be regarded as the newer one.
    
    Solution:
    If the stack is focused stack, give the top task with the last time.
    
    Change-Id: I0adc07608e03d333e0120a0dbc52a0fbbbb12f34

commit 2166ca68bddd60ec697774ebe32ddbc0f1dbb9f9
Author: Ruben Brunk <rubenbrunk@google.com>
Date:   Wed Jan 28 15:04:16 2015 -0800

    Add ProcessInfoService to activity manager.
    
    - Adds a new AIDL interface for querying process
      information from activity manager.
    
    Bug: 19186859
    Change-Id: Ic08858f346d6b66e7bfc9da6faa2c6e38d9b2e82

commit ec476fa75b71db9cc48e0d504dbffad147fcd67a
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Tue Mar 31 11:54:14 2015 +0800

    [ActivityManager] Fix index out of bounds when updating next pss time.
    
    Symptom:
    System server crash.
    
    Root Cause:
    The value curProcState for array index is -1 if the process
    has not attached yet.
    
    Solution:
    Skip computing for process which is not attached or curProcState
    is nonexistent state.
    
    Change-Id: I71aaf45bb78d73097ebe9dfebf76b72f2d243232

commit 67ad9fb611b43f84647b1d1d744c9a3ef16df80e
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 7 12:56:26 2015 -0400

    systemui: Boost when expanding the notification shade
    
    Change-Id: I3b6edaf850d7453920fe553203e74afc30dc47da

commit 10bb637236b3d88bcf390401467cd420e43040ce
Author: Squadzone <ai.the.smarties.physics@gmail.com>
Date:   Wed Apr 8 13:32:32 2015 -0700

    Implement ambient display as Active Display
    
    Currently Ambient Display fully support if device has
      Significant motion sensor and wake gesture sensor
    
    with this change allow Ambient Display to work like
        Active Display
    
    -- Allow wake up using shake event
    -- use different class to manage sensor
    
    enable this via overlay custom_config.xml
    
    inside Frameworks base
    
        <!-- Doze: force using accelerometer as pick up sensor -->
        <bool name="config_dozeUseAccelerometer">false</bool>
    
    inside System UI
    
        <!-- Doze: shake accelerometer threshold -->
        <integer name="doze_shake_accelerometer_threshold">10</integer>
    
    also dont forget to setup other value for Ambient Display
    
    see https://gerrit.omnirom.org/10140
    
    PS. 12 : prepare for user configurations
    
    <!------------------------------------------------------------>
    
    NOTE:
       Shake event aka Wake up will not triggered until
       Proximity is Covered (need to put inside pocket)
    
       for shake accelerometer, you must setup based on your device
       each device has different threshold
    
    <!------------------------------------------------------------>
    
    NOTE 2 :
    
       you can also overwrite all value for Ambient Display inside BUILD.PROP
       but i recommend only overwrite value from overlay fw base and system Ui
    
       example value inside BUILD.PROP :
    
       <!-- Doze: does this device support STATE_DOZE and STATE_DOZE_SUSPEND?  -->
       doze.display.supported=true
    
       <!-- Doze: pulse parameter - how long does it take to fade in? -->
       doze.pulse.duration.in=1000
    
       <!-- Doze: pulse parameter - once faded in, how long does it stay visible? -->
       doze.pulse.duration.visible=3000
    
       <!-- Doze: pulse parameter - how long does it take to fade out? -->
       doze.pulse.duration.out=1000
    
       <!-- Doze: should notifications be used as a pulse signal? -->
       doze.pulse.notifications=true
    
       <!-- Doze: when to pulse after a buzzworthy notification arrives -->
       doze.pulse.schedule=1s,10s,30s,60s,120s
    
       <!-- Doze: maximum number of times the notification pulse schedule can be reset -->
       doze.pulse.schedule.resets=3
    
       <!-- Doze: shake accelerometer threshold -->
       doze.shake.acc.threshold=10
    
       <!-- Doze: force using accelerometer as pick up sensor -->
       doze.use.accelerometer=true
    
    <!------------------------------------------------------------>
    
    With this change now we have 3 mode :
    
        1. pocket mode = proximity enabled after screen off, if detect NEAR state (covered by hand or somethings), doze will disable
              until FAR state (uncovered), if FAR state is triggered, Doze will appears.
    
        2. pulse mode = doze is triggered by notifications, and so after notifications arrive, doze will show up, and doze will setup
              time to show again (see doze.pulse.schedule=1s,10s,30s,60s,120s inside config.xml) and reset after see doze.pulse.schedule.resets=3
        pulse mode by default is already there if device is support ambient display (e.g nexus 6), so there is no change in the code
        (still using original code logic)
    
        3. shake mode = enabled after proximity detect FAR state (pocket mode) or Doze is triggerd by notifications (pulse mode), and disabled
              if proximity detect NEAR state, or user already shake
    
    <!------------------------------------------------------------>
    
    Feature describes:
        1. Full mode (pocket,shake,pulse)
        2. Pocket and shake only
        3. Pocket and pulse only
        4. Pocket only
        5. Shake and pulse only
        6. Pulse only (default)
    
    <!------------------------------------------------------------>
    
    Note :
        Shake mode only enabled after Doze is triggered by proximity or notifications (depends on option)
        so if doze not triggered by that, shake mode will stay disabled.
    
    <!------------------------------------------------------------>
    
    AICPfy
    
    Change-Id: I6e1d634c9c8b1c3d3ac938c572d9f79902e6e9e5
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/res/res/values/config.xml
    	core/res/res/values/symbols.xml
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 9fb69d322a068eaa680fa648d50e8e7f3bf1c9e3
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 13:56:43 2015 -0700

    Revert: Frameworks: cmremix up sounds and update (1/2)
    
    Base on Frameworks: slim up sounds and update (1/2)
    Till now we modified always the aosp make files etc. Was complicated to maintain.
    Hence we add now an own slim folder and own AllAudioSlim.mk to mainatin it completely
    ourselves.
    
    As well reduce size etc etc
    
    Change-Id: I0d60a0abe0935f1000016bc5d69b4f4e36616941 (reverted from commit ffd8c658c3de90943f4cee98be717f0ab1f6a99c)

commit 3dc23c2dd514eac916da14fdd691bd28973c78f5
Author: david <davidteri91@gmail.com>
Date:   Tue Jan 13 16:38:22 2015 +0100

    Base: CM Power Menu: Remove Bugreport
    
    Change-Id: I9a9438e4e4cd1813f2a9a363ffac03b689f2c4cc

commit 362cfe55ff2311fae32ab8a606e9333c62d4f1b8
Author: Dave Kessler AlmightyMegadeth00 <activethrasher00@gmail.com>
Date:   Wed Apr 8 15:57:00 2015 -0700

    SystemUI: option to disable search panel (navrings) (1/2)
    
    Change-Id: I0d8999e19ce34495f600c25084418df7364ae79e
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 6f20ecb791f9ac9b5e36ee04eca8f47e7af7c1ad
Author: LorDClockaN <davor@losinj.com>
Date:   Sun Feb 8 17:02:35 2015 +0100

    Make proper power menu qs icon
    
    still no SVG :D
    
    Change-Id: I1f0c8664cd9d4151d8e8545854935bc888a52aa7

commit 153a27939a44c488bc203e1c84680cc068206b03
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Fri Feb 6 19:40:36 2015 +0500

    Theming Immersive mode confirmation dialog
    
    Change-Id: Ia2858ee9c39248cb5ea12f22634d2dfe29738fb2

commit 403b88794205811242424a041555c21f70121db2
Author: Alexander Westphal <westphal.alex94@gmail.com>
Date:   Sat Jan 24 16:07:05 2015 +0000

    New DocumentsUI icon
    
    Change-Id: I9ca07807bcbd73d4cd131c9edc114b4f84b01ba0

commit 1c944776de7539d7be683d3a56bf57a60b64782b
Author: karon8 <karon@yahoo.com>
Date:   Wed Apr 8 16:06:24 2015 -0700

    FWB: Add Volume Key Answer (1/2)
    
    Change-Id: I1d1c61fa64741a1b68b4a622b93d90b687eaa20d
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 17d879dd410801e2b1407fc9b9c4ab6c8d50a2de
Author: Andrew Boren <andrew.boren@gmail.com>
Date:   Wed Apr 8 16:08:16 2015 -0700

    Powermenu screenshot delay [1/2]
    
     * Only works from power menu
     * Defaults to 1 second (1000ms)
    
    Change-Id: Ic7477d4ed962b97d5bbfd980cfdb7e3516262463
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/GlobalActions.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 665cc5e3310153994a5d37dd029b19a204aaba9c
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Wed Nov 26 10:26:50 2014 +0500

    core: Materialize text select handle
    
    P7: xhdpi drawables sized by Lo Huot
    
    Change-Id: I1efcf34e9bbd678b13724711797a541bd7ca01a8

commit 926d09c941ce00742b79ebe9b3ffd8cd3c5c3a97
Author: Janson Kang <temasek71@gmail.com>
Date:   Fri Feb 13 16:13:28 2015 +0800

    DeviceUtils: Clean up code after ScreenType FWB commit
    
    Change-Id: I18d245fa62b67ca5e4d533b3ca317738e2c658dc

commit 07d7468515fa83f5f2a614d31801d4b9de2995be
Author: alviteri <davidteri91@gmail.com>
Date:   Wed Apr 8 16:12:40 2015 -0700

    SystemUI: Fix back button drawable (Height & Width NavBar feature)
    
    This revert the following commit: 2ddf021da408bd547cc36dcf9d949e81f144ed59
    
    Also we don't have the (change back button to hide ime buttom with rotate animation) problem as describe in the revert commit
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/BackButtonDrawable.java

commit 1bc7686efc9edc7b4b38895201a688294f387850
Author: david <davidteri91@gmail.com>
Date:   Sun Feb 15 19:10:52 2015 +0100

    NavBar: Fix little BackLand drawable
    
    This update the following commit: ae14a1c58f8d80629a3dd7121b4f2d3b9acf0be5
    
    Change-Id: I5f106b6da16e5e624cf1bf8f55ca56a13037ad79

commit 24ec24a1de86eda1801029511bbc14ddb055d5f7
Author: AndroidRul3z <ferrettidario@gmail.com>
Date:   Wed Apr 8 16:14:38 2015 -0700

    Navbar: add power button
    
    Conflicts:
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power_land.png
    
    Conflicts:
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_power_land.png

commit 4b9a19b90c2fddb2126be5dddb11f495bf442de2
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 16:18:08 2015 -0700

    Navbar: Fixed NAVBAR_POWER behavior
    
    Change-Id: I312593af273084c5de3464500a0668eb47e26d07

commit bd166d26ef411a7e2d4b53f47855e9d65ed6111c
Author: david <davidteri91@gmail.com>
Date:   Fri Feb 13 18:52:34 2015 +0100

    SyncTile: Updates
    
    remove secondary click due to we are not using that function here
    
    Change-Id: I9712463bdfe196f006dd60488033068c51809faa

commit 56e61e81423490e6120ea0dc68205a3550818f01
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Fri Feb 6 21:21:40 2015 +0000

    DocumentsUI: Turn advanced devices and file sizes on by default
    
    Change-Id: I443a09fb6fa25ffa9aea2e5f84ddad843ed3559f

commit 304546f96465480b675aae0eeba54e064cdec974
Author: Dirk Rettschlag (MarcLandis) <dirk.rettschlag@gmail.com>
Date:   Sat Jan 31 19:56:48 2015 +0100

    Add boot animation preview (1/2)
    
    This change is needed to get notified once the animation is finished.
    The usecase would be multipart animations where the first part is shown
    once and the second is shown in a loop.
    
    Change-Id: Ibd9c83a4662bef2a866c5bb076d94f49e714dd63
    Signed-off-by: Dirk Rettschlag <dirk.rettschlag@gmail.com>

commit 8ce98197cc5f991471fc3d925d58c55b59c354c1
Author: kufikugel <kufikugel@googlemail.com>
Date:   Thu Sep 11 10:33:47 2014 +0100

    EdgeGesture service: add more sensitivity steps
    
    Change-Id: I464f6eac89f0aba74f58fdd450245f780e1ba31a
    default: 5, minimum: 1, maximum: 10

commit 5131c507b6d3c9d4938c10f74404c2f7d2d7a7b0
Author: TheMrcool212 <themrcool212.android@gmail.com>
Date:   Wed Apr 8 01:23:47 2015 -0700

    Double tap to sleep on navigation bar [1/2]
    
    Change-Id: I5770ccd076b6b3d4e35f6fb7c80387e6dea3a4dd
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit a667f0e6fe4a7e52f9cd201f9f1fdcd8884f2fd5
Author: tiger_huang <tiger_huang@htc.com>
Date:   Mon Feb 16 16:14:47 2015 +0800

    Prevent leaking surfaces from exiting windows
    
    AM would set the exiting app to be invisible twice by calling
    setAppVisibility(). If the screen is turned off during these calls,
    the window surfaces of this exiting app won't be destroyed.
    
    The flow:
     1. Screen is on
     2. App A is finished
     3. AM calls setAppVisibility() token=App A, visible=false
     4. WM sets a dummy animation to App A
     5. WM marks App A's wtoken.inPendingTransaction=true
     6. Screen is turned off
     7. AM calls setAppVisibility() token=App A, visible=false
     8. WM calls setTokenVisibilityLocked() directly (screen is off)
     9. WM sends app visibility to App A's client (ViewRootImpl)
    10. WM clears the dummy animation from App A
    11. App A's client calls WMS.relayoutWindow() to be not visible
    12. WM sets App A's window mExiting=true but not destroy its surface
    13. App A's window surface leaks...
    
    Note:
    a. The call in 3. is from ActivityStack.finishActivityLocked
    b. The call in 7. is from ActivityStack.resumeTopActivityInnerLocked
    c. In 10., App A won't get the real animation while screen is off
    d. In 12., App A's inPendingTransaction=true; WM takes it's animating
    e. mExiting won't be cleared because App A has no animation to
       trigger WindowStateAnimator.finishExit()
    
    After applying this patch, WM would destroy the surface in 12. of the
    above flow.
    
    Change-Id: I18b79ba96695ec80d57a85dc15cf92a9e7d3a6ef

commit 612092a1f186ec8427dfffe09a3414fdddbb5ba7
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Feb 8 22:06:56 2015 +0000

    Fix: Battery saver mode
    
    Status bar & Nav bar Colors were resetting to default after screen rotation.
    
    Change-Id: I15a61c49a2cb9874a6d9f5936e75e4930531da40

commit ddf625f2dbe604b58b3d0983fcdfa3349c20dc6f
Author: BigBrother1984 <carlosavignano@aospa.co>
Date:   Sat Jan 17 16:38:37 2015 +0100

    SystemUI: Materialize volume panel in/out animation
    
    * Thanks to @David96 that had the original idea, material
      oriented, already during kitkat times.
    
    AICPfy
    PS2: FIx expanded panel not hiding derp
    
    Signed-off-by: BigBrother1984 <carlosavignano@aospa.co>
    Change-Id: Ic79d404c4a0d5bc0a83d20cd4e0d7d5ad7b7c90f
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/volume/VolumePanel.java

commit 1294b15ee42be4b90a241fcf15a06023007360eb
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Sat Jan 17 04:50:28 2015 +0100

    ExpandedVolumePanel: Fix SystemUI FC when expands volume panel from Notifications tile
    
    java.lang.IllegalStateException: The specified child already has a parent. You must call removeView() on the child's parent first.
    
    Change-Id: I3f5acf5e39e01cd74b7d039bc2189a9009f2abe7

commit 618a502f7180c6f74a23431ac68a634b6f975b5f
Author: alviteri <davidteri91@gmail.com>
Date:   Wed Apr 8 16:27:13 2015 -0700

    SystemUI: Update 'Materialize volume panel in/out animation'
    
    Fix animation expanded volume panel hide
    Add animation for volume panel expand
    
    This update the following commit: 5e46b21
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/volume/VolumePanel.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/volume/VolumePanel.java

commit 670aceb44b6a9e091dfbe4887a76bc944a30a214
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Mon Feb 16 19:18:42 2015 -0200

    [Base] Volume panel timeout
    
    - This feature keeps Google behavior on safe warning and zen panel expanded mode. All the others media will respect the custom timeouts.
    
    This feature is based in kk feature, from here: https://github.com/cristianomatos/android_frameworks_base/commit/0958e539f568352f0d44a29481275329d7c3a9dd. Thanks @UtkarshGupta for the idea
    
    Change-Id: I6197492bdf957cc9fa4258e1950c6cc875a4f431
    Signed-off-by: Cristiano Matos <cristianomatos@gmail.com>
    
    Conflicts:
    
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/volume/VolumePanel.java

commit 6782cc5f2804febc94f199ed8b17cc301b18676a
Author: Wei Wang <wangw@codeaurora.org>
Date:   Mon Mar 23 18:22:29 2015 -0700

    binder: adjust GC interval for binder ops
    
    The current value is too conservative, and causes
    janks in certain use cases due to frequent explict GC.
    
    Change-Id: Iba8eecd4e8ed7dce879c144fdc4407c12f76a749

commit dcbd8bd1bc29d63d40d998228d0660c05b3d51a1
Author: Varad Deshmukh <varadd@codeaurora.org>
Date:   Thu Mar 26 19:39:19 2015 -0700

    Trigger GC Delay for subsequent launches.
    
    Application launches for apps like GMS Music
    and Maps lead to explicit GC's due to Binder
    activity in the SystemServer. This change
    allows delaying the GC for 3 seconds after
    the application is launched. Subsequent launches
    or first relaunches for killed applications
    are also now covered.
    
    Change-Id: I945f19b1363504f4d5f61deb1a3af23149b80e64

commit 942cd620665445627bde7776e145e8e6f9affdcd
Author: garwedgess <garethwilliams21@gmail.com>
Date:   Sun Feb 22 02:13:06 2015 -0700

    [1/4] Base: Breathing missedcall/sms/voicemail
    
    Adds a breathing effect to missed call/SMS/voicemail notifications.
    
    Mms: https://gerrit.omnirom.org/#/c/4977/
    OmniGears: https://gerrit.omnirom.org/#/c/4978/
    Telephony: https://gerrit.omnirom.org/#/c/4979/
    
    Change-Id: I1b7f40c2fc5c6612303cf6575e3efe8e992cecae
    
    @alviteri: Port by me to crDroid Android
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 3951fa0ed575ec2474bbb27c452fe16e2451d1a7
Author: dankoman <dankoman30@gmail.com>
Date:   Wed Apr 8 22:43:46 2015 -0700

    SystemUI: start redrawing some navbar icons, add lastapp icon
    
    Change-Id: I0925fe7a348a8914757caaca6c97d85fb7337f7b
    
    (cherry picked from commit a624b41c837ea3018cd91c5be45b2a4323810773)
    
    Conflicts:
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_recent_land.png

commit 3cc0647066d1a02f7403da8862d36793a10da439
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Wed Apr 8 22:45:00 2015 -0700

    New NavBar icons by Manuel Labrador Vianth
    
    https://plus.google.com/u/0/+ManuelLabradorVianthi
    
    Change-Id: I1a34722d4179367582875dc2eee3474d035da9f0
    Conflicts:
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-hdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_power.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_power_land.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-mdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-xhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-sw600dp-xxhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back_ime.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_back_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_home.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_home_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_recent.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_recent_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search_land.png
    
    Conflicts:
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-hdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-mdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xhdpi/ic_sysbar_search_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_menu_big_land.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search.png
    	packages/SystemUI/res/drawable-xxhdpi/ic_sysbar_search_land.png

commit 17691c497160e09847a16e16d07b0ad524bb482f
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Feb 24 00:57:12 2015 -0700

    Add Headsup tile [1/2]
    
    - Add Heads up tile
    - Collapse panel and show toast after clicking on Heads up tile
    
    Thanks to Altaf-Mahdi.
    Took some code from Euphoria-OS/android_frameworks_base@5ae2857
    
    Change-Id: Ibfc0b813b0405b5cc159cf82d7b5b8b3fc73d298
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 8000982d5a9835d1008a8f7c74e44a32c584f64f
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Feb 24 00:58:17 2015 -0700

    NavBar tile [1/3]
    
    Change-Id: I90727432c1ea806170ef9b13d5237eabe69dd14c
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	packages/SystemUI/res/values/cmr_strings.xml

commit 4d5d5e682339c95e329570e33f7da45cf2b57bd2
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Feb 24 01:01:29 2015 -0700

    App Circle Bar Tile [1/3]
    
    Change-Id: I48aecb66bd9ec5fbab1b1ec7190f521641eb9e95
    
    Conflicts:
    	packages/SystemUI/res/values/strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	packages/SystemUI/res/values/cmr_strings.xml

commit df17539c8f510a9241c4320ef04e1e4f889e9e8e
Author: martincz <martincz@mokeedev.com>
Date:   Wed Apr 8 22:56:53 2015 -0700

    Show carrier label / custom & change color [1/2]
    
    Change-Id: Ida3321c9176e4e786fad96766dab056d8614360d
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/values/styles.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/NetworkControllerImpl.java
    
    Conflicts:
    	packages/SystemUI/res/layout/status_bar.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit f9752cf679df295597af2940f4480e5eff95c7fc
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 26 16:51:21 2015 -0700

    Show carrier label / custom & change color Use Statusbar clock style instead
    
    Change-Id: I171665396a5bb391c33bab48e362abf63b3b6ee0

commit c1a0c463128446dbaa1e6d4bf46e35b4bf3ee3c0
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Wed Apr 8 23:57:47 2015 -0700

    FWB: Hide network activity arrows (1/2)
    
    AICPfy
    Destilled from here:
    https://github.com/CyanideL/android_frameworks_base/commit/7c802f64c306a1c023a67737560b58572e46c644
    so giving all credits to the mentioned @XXMrHyde
    
    Change-Id: Ibb18a9b1988e5275da1757c5ba6b874be5943273
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/NetworkControllerImpl.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/NetworkControllerImpl.java

commit 66873246c8845252cc067f0da5af6e7cdee2c550
Author: BestPig <bestpig82@gmail.com>
Date:   Wed Feb 25 23:33:11 2015 -0700

    Add USB Tether Tile (2/2)
    
    Drawables by blunden
    
    Change-Id: I3c21d2b7e93ea65cad64dc39b15a6c6d74885f2f
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/pac_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 6f47b5f53b3280d07637d4765be8f8a5313be5d9
Author: KreAch3R <kreach3r@users.noreply.github.com>
Date:   Mon Mar 2 02:28:42 2015 -0700

    Add option to hide Bluetooth Icon when disconnected in Status Bar (1/2)
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBarPolicy.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBarPolicy.java
    
    Change-Id: I45fbc996759db7d7fe67e35101943aff0a9745b7

commit bcb67a43798eb9cdcef55c2b39811c9f94988803
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sun Mar 1 08:19:34 2015 -0300

    Power menu into navring targets
    
    - For now i'm using the same vector drawable of screen off
    - For cherry-pickers: you'll need this commit, total if you want power menu qs tile or part to have the "interface": https://github.com/cristianomatos/android_frameworks_base/commit/12551a2385e9c699516c0643d4e2dee7f9e3e808
    
    Change-Id: Ic1deb82525464a49cf707d879ac82189cbf12b56
    Signed-off-by: Cristiano Matos <cristianomatos@gmail.com>

commit d574a20a93a8170719e55215599e128b677cef70
Author: Dave Kessler AlmightyMegadeth00 <activethrasher00@gmail.com>
Date:   Thu Apr 9 00:03:37 2015 -0700

    Status bar greeting [1/2]
    
    play a text greeting in the statusbar when exiting the keyguard
    
    AICPfy:
    Add msim support
    
    Change-Id: Idd7a8c6bda2d2411fdd0a9a25d6709e541084158
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 25f4744d74cb6c7d5ba98437138ad8c94bf8859c
Author: FusionSP <dragon7780@hotmail.nl>
Date:   Thu Apr 9 00:11:49 2015 -0700

    Detect status bar carrier state when theme change.
    
    This will fix the issue when changing or applying theme,
    the status bar carrier label was set to enabled.
    Then when we want to disable the status bar carrier label
    thru Settings the systemui would crash.
    
    now we let the system detect if the user has
    enabled or disabled the carrier label when we change or apply theme.
    
    Change-Id: I062ee85f3b4912ebecfb5e1e7ad6e4d222f044fa
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 3b42f372c4bf3595f2bcd8d0b763e674353fd45a
Author: LorDClockaN <davor@losinj.com>
Date:   Thu Apr 9 00:13:53 2015 -0700

    FWB: Greeting label timeout (1/2)
    
    Also include Themes persistance
    
    Change-Id: I8e736cdbad733a66814d72bc108ce6116eec9e1a
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit ce852f50611d8e5a7ad9951bee1c8ca5a7737e20
Author: Kryten2k35 <kryten2k35@gmail.com>
Date:   Tue Mar 3 13:52:33 2015 -0700

    Call recording encoder/format choice 3/3
    
    PS1: Adds a user option between WB AMR (the default) or HE-AAC for the encoding of call recording audio. Also changes the output format of the file appropriately (WB AMR now uses the WB_AMR output format and HE_AAC chooses the MPEG_4 output. File extensions are adjust accordingly as well).
    This was in reponse to people complaining the quality of call recording audio is poor. It's noticibly better using HE-AAC, but filesizes are larger.
    
    Change-Id: I0a54ab19d07dd794e97a68f6bef4a3df141505a2

commit 824e2de69f98dd02590e36a46245c7ab932d5742
Author: martincz <martincz@mokeedev.com>
Date:   Tue Mar 3 13:54:38 2015 -0700

    base: Direct call (1/4)
    
    Change-Id: I35582b18b8dd9f9d300383cc39f0f2f4ed26d2b7
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 244157eab0962f71d80b8a68672c440b4769db99
Author: 0xD34D <clark@scheffsblend.com>
Date:   Thu Apr 9 00:29:37 2015 -0700

    [1/2] frameworks: App sidebar
    
    @ZION959 port from KK4.4 to CMRemiX Lollipop
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/res/values/cmr_dimens.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Change-Id: I4c061773ada6a37f37ea740d4ba9d6ac13c3933c

commit 8a71a12daa5d4d5e19dbfe4257b4083053ec3ca3
Author: lion0738 <lion0738@naver.com>
Date:   Thu Apr 9 00:33:56 2015 -0700

    App sidebar: some adjustments
    - Cleanup
    - fix disappearing appbar on changing appbar position
    - may fix endless FC on changing appbar contents
    
    Change-Id: I2e94290dc128447f0da8937eb5dc0ed10296a155
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 988d73b0b2e47c5c9bce8428cffd3d9004b97f3a
Author: lion0738 <lion0738@naver.com>
Date:   Tue Mar 3 21:22:05 2015 -0700

    App sidebar: notify if app is not installed
    
    better than force close
    
    Change-Id: I9eebe1a3a4be2dad16ed9a8cff9c0694900d833d

commit db1ffdf8c10911aa6fe80ae63a143b37776e339c
Author: Jmz <jmztaylor@gmail.com>
Date:   Tue Mar 3 22:15:29 2015 -0700

    Force Expanded Notifications (1/2)
    
    This will force expanded notifications for all apps that support
    expanded notifications
    
    Change-Id: I1f6fac658a3e58488bc37cafec9208a75da78ab8
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 9233f443b5b0e50977f63369ef6f42c188243774
Author: Jubakuba <Jubakuba@gmail.com>
Date:   Thu Apr 9 00:38:00 2015 -0700

    Frameworks: Slim Shortcuts
    
    Change-Id: I784b4fb37238658131779eae3b55adc0aefd8d18
    
    Conflicts:
    	packages/SystemUI/AndroidManifest.xml
    
    Conflicts:
    	packages/SystemUI/res/values/cr_strings.xml
    
    Conflicts:
    	packages/SystemUI/res/values/cmr_strings.xml

commit 4706d9cb18e8299c0fd89cba02c914ddc8ce90e7
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Mar 3 16:16:06 2015 -0700

    QS: add Ambient display tile
    
    Drawables thanks to Alexander Westphal <westphal.alex94@gmail.com>
    
    Change-Id: Ia1279d9f2295e6be42fbc1b8cd79b458de7816f9
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/custom_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/cm_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 7e4d255cf5f6e4aaa980013bf2d5d0f36592ef90
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 9 00:43:38 2015 -0700

    Framework: SlimAction as QuickTile (1/2)
    
    Configure which Slim actions you want to use as tile and then add the 'SlimAction' tile.
    Single press will switch between Slim actions and long press will execute the Slim action. If the tile has only one Slim action, single press will execute the action.
    
    Screw'd:
    Modified for Screw'd AOSP sources
    
    Change-Id: I229b2163152f73b4870878837117204dd0aad960
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit de238bc085a357f458fece6597ebc2ac96313a97
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 9 00:46:27 2015 -0700

    Action: Add kill-app and last-app actions
    
    Forward port from KitKat
    
    Change-Id: If8326ffed21faa2452e22b2afb717f4c123bd2a0
    
    Conflicts:
    	core/java/com/android/internal/statusbar/IStatusBar.aidl
    	core/java/com/android/internal/statusbar/IStatusBarService.aidl
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java
    
    Conflicts:
    	packages/SystemUI/res/values/cr_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java

commit 085be268d7e5b19feb49f30f6ddb3bf3406f6077
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 9 00:47:51 2015 -0700

    Action: Add screenshot action
    
    Change-Id: I98960f6bc9987da763342f491611dc54c44fca43
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java

commit 6ced08ab93ce299d27dbb4061fd1dbd2d39f1d42
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Mar 10 17:46:53 2015 +0100

    FWB: Dotted circle battery (1/2)
    
    thx to Griffin Millender
    
    Change-Id: I6ba0ebfd7f8e10c39d43c282b48ffca61461e78d

commit b51c711d724ef36a94382727dd07e35547641ea3
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Apr 9 00:56:19 2015 -0700

    FWB: Proper LS weather switch from XXMrHyde
    
    Change-Id: I9b730d53ac4bc40be77dab91e9f361a3ad970dcd
    
    Conflicts:
    	core/java/android/provider/Settings.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/Keyguard/src/com/android/keyguard/KeyguardStatusView.java

commit 6b47072a34f71c79a45f176b2c9d0c9e86790650
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Apr 9 01:01:17 2015 -0700

    Lock screen: Weather panel improvements, (1/2):
    
    - Move weather panel to the bottom the clock panel
    - Add wind
    - Add humidity
    - Add Condition
    - Add Timestamp
    - Add condition icons (colored and VClouds)
    - Rearrange the weather panel:
      - Left side:
        - Location
        - Wind
      - Center:
        - Condiditon icon
      - Right side:
        - Current temperature
        - Humidity
      - Bottom:
        - Condition
        - Timestamp
    - Option to show/hide the timestamp
    - Option to colorize the monochrome icons/all icons
    - Custom text color
    - Custom icon color
    
    Change-Id: I986975c13c5d29bd8103424e020ad775a8f03804
    
    Conflicts:
    	packages/Keyguard/src/com/android/keyguard/KeyguardStatusView.java

commit 00e2c0cf162eb24ca06df0e8d4f2dea803256aa0
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Apr 9 01:09:55 2015 -0700

    Lock screen: Text and icon colors, (1/2):
    
    - Global lock screen text color
    - Global lock screen icon color
    
    The weather panel is using the global lock screen colors
    
    This won`t colorize the pattern-, password-, pin-
    and face unlock views, this will follow in one of the next commits.
    
    Change-Id: I6e5591b4d78ee703d01ebd14382a2ce7b162d9a6
    
    Conflicts:
    	packages/Keyguard/src/com/android/keyguard/KeyguardStatusView.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit d2e24dd331353fe9f08ee1c27322caf8140ffbd4
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Apr 9 01:43:42 2015 -0700

    (1/2) Frameworks: allow to toggle smart cover wake
    
      * disable by default
    
    Change-Id: I83d96696fefedc19fc3bce7265a4fcf2d4c894bc
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 515e897f9fb34872f75f29252a1d0ea13d99cca1
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Mar 12 09:23:00 2015 +0100

    Preference: allow to get list of preferences from preference group
    
    Change-Id: Ifecaeb43c0a9beb79869e812ce41fafc789ba434
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit d7dd6b69c6c918a3f3d85e0a7c3f5bfde4c2c236
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 02:02:15 2015 -0700

    private View mWeatherView; removed duplicate
    
    Change-Id: I879b8e4c6b4e9e5a1a78cd6c2a503c6763fbe6b2

commit 416d5b21d4621fcd38aca80cde3dc508ea337316
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 03:01:39 2015 -0700

    derp fixed
    
    Change-Id: Ie29b5d6496b6b0594fa14a1fef94d09709804e29

commit fe5f69b5971c240a551cbd7c01e814c9fde2aab0
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Sun Jan 25 23:13:10 2015 +0100

    alarms: include Timer.ogg
    
    Change-Id: Ibaa1634dbdad8239add21c18a816f1c0bfa1f6d3
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit af5c5adcb076823680d8c3109c3a5a483a287089
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 13:15:13 2015 -0700

    Revert : [1/2] Screen Recorder
    
    http://forum.xda-developers.com/showthread.php?t=2547196
    
    Change-Id: I5bb81f909a44183fd8e011318f50a1b1e42c94e5
    
    Conflicts:
    
    	core/res/AndroidManifest.xml
    	core/res/res/values/cm_strings.xml
    	policy/src/com/android/internal/policy/impl/GlobalActions.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/res/res/values/cmr_strings.xml
    	core/res/res/values/cr_config.xml
    	core/res/res/values/cr_symbols.xml
    
    Conflicts:
    	core/java/android/provider/Settings.java (reverted from commit 146cc7f1d5fd6c9b6ab252fc00d4df2aa94f8a25)
    ScreenRecorder: Update icons
    
    Thanks to @kantjer
    
    Change-Id: Id7a752a2a1edc7aa384addd19691981f52b1cf5f (reverted from commit 8e1572d476029e26c1f17e0792cf58e73b5b40fa)
    Screen Recorder: Catch NullPointerException
    
    Change-Id: I316de00ba7761fa627071e53964412d653830c32 (reverted from commit fa6f2e02ceecf85502bb14621f725228f60a5aa7)

commit 1289f74b4ebe219b96e6a4c8fdb17843d443c5ef
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Apr 9 13:25:49 2015 -0700

    base: screenrecord: forward port from 4.4
    Squashed commit of the following:
    
    commit 06f9b5a7ebefb8ff477241269a005b9afae2be87
    Author: maxwen <max.weninger@gmail.com>
    Date:   Sun Dec 28 21:31:46 2014 +0100
    
        base: screenrecord: use different notification image
    
        Change-Id: I252144a4f5c3bdaa84974b996348885ba8dee942
    
    commit 6f9f2d83e5c86b6259bccfdfadb0e4243872f7f9
    Author: XpLoDWilD <xplod@ouverta.fr>
    Date:   Sun Jul 13 21:43:28 2014 +0200
    
        Screenrecord: Fix SystemUI loop-crash
    
        Change-Id: I25045820465d21b7d1f0e933e5e4f3324cb044b6
    
    commit b6f20490332f293df050db46f9a8ced9394b9641
    Author: maxwen <max.weninger@gmail.com>
    Date:   Tue Apr 29 23:28:06 2014 +0200
    
        base: screenrecord: update notification
    
        Update show/hide pointer button for actual state
    
        Change-Id: I02090f05b06896248483f3f9ff2eb22924a22476
    
    commit aa23ce799167f97a6e9f7beaf57d23027b5c32ed
    Author: maxwen <max.weninger@gmail.com>
    Date:   Tue Dec 23 01:04:35 2014 +0100
    
        Screenrecord: correct multi-user acces for settings
    
        Change-Id: I0bee907d190b2dc0df1c12d136f31ed379a59866
    
    commit 1fc7464c6d3efcb13e243aae7ed798d67af86ede
    Author: xplodwild <me@xplod.fr>
    Date:   Wed Nov 13 08:16:57 2013 +0100
    
        Screenrecord: Create the Screenshots directory if it doesn't exist
    
        Change-Id: I2b0458eed024dbda97e9e1ea3426c12d29add781
    
    commit 7c08a37a28bcf7b44e9de2b67c502077c0f4fb47
    Author: xplodwild <me@xplod.fr>
    Date:   Tue Nov 5 20:30:09 2013 +0100
    
        base: Add a key combo to start/stop video recording
    
        Press volume up and power to start recording a video of your screen.
        Press this key combo again to stop it.
    
        Change-Id: Id0b13ba1092a1d6e0bf7bff5f14d89764cdf370c
    
    Change-Id: Ida1ee4a5c8d334c72d549752d02bd7848932dc7c
    
    Conflicts:
    	core/res/res/values/config.xml
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	core/res/res/values/cr_config.xml
    	packages/SystemUI/res/values/cr_strings.xml
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 2b6d39b47c082cbb4408640dc2df35f0bd66e3d0
Author: eyosen <abittin@gmail.com>
Date:   Thu Apr 9 13:28:05 2015 -0700

    Add Screen Record to the Power Menu [1/2]
    
    PS1: Added to CM base
    
    Change-Id: I9e645aba1e48128a9ccfab8a1a1d85f0b0c2f337
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/GlobalActions.java

commit 2d40cf8a9bd89891837ddcfdf639fd59a56d6900
Author: eyosen <abittin@gmail.com>
Date:   Tue Mar 24 16:00:06 2015 +0100

    screenrecord: fix key combo trigger
    
    Change-Id: I9347530be4d2835ef57df1813b43628319522671

commit 3cb4f87663dfc5953045ef657df932e65737a4cb
Author: eyosen <abittin@gmail.com>
Date:   Thu Feb 5 13:49:09 2015 +0200

    QS: add Screenrecord tile (1/2)
    
    Change-Id: I2df2ff0c8b81eb77b3d112d357cdf18cb19f4c2b
    
    Conflicts:
    	packages/SystemUI/res/values/custom_strings.xml

commit f2758eed8bcb9679cf3ad326c6907c87ce07641e
Author: eyosen <abittin@gmail.com>
Date:   Sat Feb 7 18:05:12 2015 +0200

    QS: add Screenrecord tile drawables
    
    Change-Id: I2e3ac0fa2ddb775c65f9a56808b94e4bdde10c6c

commit 05b835d5821e4c21e432c7c9834c039ab1a54302
Author: louis_chang <louis_chang@htc.com>
Date:   Wed Apr 8 18:04:11 2015 +0800

    [ActivityManager] Avoid NullPointerException if no
    crash info
    
    Symptom:
    This issue happens because the ANR process got killed
    (because it crashed) before the ANR dialog dismissed.
    In that case, the process record is marked as crashed
    (ProcessRecord.crashing = true). When the ANR dialog
    dismissed by user, it will cause NullPointerException
    when writeToParcel while performing IPC because there
    is no crash info (ApplicationErrorReport.crashInfo = null)
    
    Solution:
    Check crashinfo before access it
    
    Change-Id: I2995de57684c1e13aab8297f5eea1e82ca3b7ad8

commit c3d127f5adba41263fa7bb6a579841635c9b4f2d
Author: Bing Deng <bingx.deng@intel.com>
Date:   Thu Nov 8 13:35:15 2012 +0800

    ProgressBar: Fix error of process bar cannot update on some condition.
    
    When onDetachedFromWindow in processbar, if flag mRefreshIsPosted is true,
    we should set it to false. Otherwise, this flag will stay in true status,
    cannot turn to false anymore. At that condition, processbar cannot get
    update.
    
    Change-Id: I14c4e976b165ad737aae0a403a44822a7b3b2422
    Author: Liang Wang <liangx.wang@intel.com>
    Signed-off-by: Liang Wang <liangx.wang@intel.com>
    Signed-off-by: Bing Deng <bingx.deng@intel.com>
    Signed-off-by: Shuo Gao <shuo.gao@intel.com>
    Signed-off-by: Bruce Beare <bruce.j.beare@intel.com>
    Signed-off-by: Jack Ren <jack.ren@intel.com>
    Author-tracking-BZ: 61090

commit 86bdc7f61fc5d5a5a4bbeb5ac3b010111cb0e91e
Author: Johan8 Persson2 <johan8.persson2@sonymobile.com>
Date:   Wed May 16 14:27:25 2012 +0200

    Fixed memory leak in ExtractEditLayout finish()
    
    When marking text and opening the edit text dialog
    and then rotating the device would result in references
    being kept to the edit text dialog and the memory would
    never get released again.
    
    Change-Id: I3e95083e4923844d2b496ea79174ef97e77f8686

commit 92a91af3b762dc8e92418d2d71f1c58ccc44b475
Author: Craig Mautner <cmautner@google.com>
Date:   Thu Mar 5 17:41:23 2015 -0800

    Add a timeout state to frozen windows
    
    When an activity stops drawing following a rotation the rotation
    screenshot would become stuck on top of all the other windows. The
    timeout was being acknowledged but mWindowsFreezingScreen was set to
    true which kept stopFreezingDisplayLocked() from dismissing the
    screen rotation animation.
    
    By changing mWindowsFreezingScreen from a two state variable to a
    three state variable, including a timeout state we allow
    stopFreezingDisplayLocked() to continue and dismiss the screen
    rotation animtion.
    
    This change also reduces the APP_FREEZING_TIMOEOUT from 5 seconds to
    2 seconds.
    
    Bug: 15664090
    
    Change-Id: Ida5aca002a82ec8fe1ea99f0ced814c5c8f01a95

commit f058f42233946d26f5b646a78cf994852934563a
Author: Maunik Shah <mshah@codeaurora.org>
Date:   Mon Mar 30 11:36:42 2015 +0530

    Fix memory leak in Connectivity Service when phone app crashes
    
    Upon crash of com.android.phone process, NetworkFactoryInfo is
    not getting removed from HashMap and will get accumulated on
    every start of the process.
    
    Change-Id: Iafde28daddfc82728c03208522682b1efc85a121

commit 6a95db4c728b9a87f95ec826fdade9198f7f7e35
Author: Ronnie Leng <ronnie.leng@gmail.com>
Date:   Wed Mar 25 10:57:24 2015 -0500

    [ProcessStas] fix index out of bounds when add duration.
    
    Root Cause:
    There is a defect in current ProcessStats design
    and following is the scenario:
    1. Process A is started due to activity with
    name of A
    2. Process A creates ProessState with application
    uid of A
    3. Process B is started due to isolated service
    declared in application A with name of A
    4. Process B uses ProcessState of Process A as
    it uses same application uid of A
    5. Process B is finished and it leads to
    ProcessState marked as dead
    6. Process A still keeps using the invalid
    ProcessState in dead state
    7. IndexOutOfBoundsException is triggered when
    system tries to update process state of Process A
    
    Resolution:
    use process uid to replace application uid for
    getProcessStatLocked.
    
    Change-Id: I881ad9fc492c9e1a892c9e957180cebcfef8352d
    Signed-off-by: Ronnie Leng <ronnie.leng@gmail.com>

commit 9a07b8d8a08419afa3902c1288fd5f10cf125ffa
Author: Romain Guy <romainguy@curious-creature.com>
Date:   Tue Apr 7 10:39:45 2015 -0700

    Prevent possible memory leak in SpanSet
    
    If SpanSet.init() is called several times in a row with different
    values, it is possible to change "numberOfSpans" in a way that
    will prevent SpanSet.recycle() from nulling out all the spans.
    
    This can lead to memory leaks of large objects through spans
    references. User @piwai reported this leak:
    
         com.squareup.marketfont.MarketSpan
         `-[1] of array android.text.style.CharacterStyle[]
           `-spans of object android.text.SpanSet
             `-mCharacterStyleSpanSet of object android.text.TextLine
               `-[1] of array android.text.TextLine[]
                 `-sCached of class android.text.TextLine
    
    The MarketSpan instance is kept alive through a recycled TextLine
    which itself contains a SpanSet.
    
    Change-Id: Idfb2233ca16895dbe735c312662eaf0b4a2ecd65

commit 65255f3d966f94c735c5b9916fe9ea62cc98f5a0
Author: louis_chang <louis_chang@htc.com>
Date:   Wed Apr 8 16:35:55 2015 +0800

    [ActivityManager] Finish the failed-to-pause activity
    
    Symptom:
    In some scenario, the mPausingActivity may be replaced by other
    activity. When previous activity paused, the completePausedLocked()
    won't be invoked because it is no longer the mPausingActivity. If
    the activity is also pending to finish, it would never be done
    because the activity kept in PAUSING state. Since the activity's
    window also remain visible and is above on Wallpaper, user would
    see it when back to home.
    
    Solution:
    Finish the failed-to-pause activity if the activity is pending to
    finish.
    
    A Real Case:
    (1) Screen turn off
    (2) The top activity T1 crashed
    (3) When finish activity T1, the next top activity T2 will be
        scheduled to resume and pause (due to screen off).
    (4) The activity T2 is also set to finishing due to T1 crashed.
    (5) Before T2 paused and before paused timeout occurs, there has
        a new process started which brings up the next top activity T3
        to resume and pause. So the pausing activity is now replaced.
    (6) When activity T2 paused, it cannot completed the pause operation
        T2 will remain in PAUSING and finishing state with its window
        visible. The process won't be killed because the oomadj stays
        at 1 (Visible).
    
    Change-Id: Ib10fded891b21c774b26a93071c717fa50516e22

commit ba9b94ef3ffc801c2cee63bf3d78ea9cacc6c468
Author: tiger_huang <tiger_huang@htc.com>
Date:   Tue Apr 7 17:35:13 2015 +0800

    Prevent windows from freezing screen while timeout
    
    The original logic lets windows be able to freeze screen again (by
    setting win.mOrientationChanging=true) after WINDOW_FREEZE_TIMEOUT is
    triggered before mInnerFields.mOrientationChangeComplete is set to
    true. In this case, we would lose the protection of
    WINDOW_FREEZE_TIMEOUT. If the app never finishes drawing the window,
    the screen would keep freezing that the user cannot operate the
    device.
    
    Change-Id: I45a0a9e4b3f8d5b0b0043229bfa4890236ae8ab2

commit 316c79004f3a719b9057b94fc6a9b333382f29d7
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Wed Apr 8 22:08:57 2015 +0200

    systemui: fix npe in egg
    
    Change-Id: Ie5445523f50cc4b6808af9698bbf97a20a6eeebe
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 9599e1404d627da0731fd57de4e2d8ead2d1ddb8
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Mar 1 18:54:52 2015 +0000

    SystemUI: long press lock screen lock icon to sleep (1/2)
    
    Change-Id: Ibb65141ee83fcf7c47e64254c92fd75920c2b185
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java

commit 42e90a4a0ab073a6e205c3f3d03daf2efbc7ccd0
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Apr 6 15:44:44 2015 -0700

    SystemUI: move keyguard visualizer behind notifications
    
    Also, handle hiding and showing the visualizer when dragging
    notifications, or tapping on them.
    
    Change-Id: I9402dded1cd76676887caae5f3aa075b03a6e7ea
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java

commit 6bbaf57d8b1963b7b0bb59da2bd05d6a5c20c820
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Fri Mar 13 05:20:46 2015 +0000

    Base: fix unlinking volume sliders (2/2)
    
    Change-Id: I3591cc459b8532e1a6a1d7acbc394b076ff58ccb

commit d28ab3f802097b9038d11ee232ad73bf180d44d7
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Mar 1 18:17:20 2015 +0000

    QS: fix qs main tiles settings not refreshing tiles
    
    This shouldnt have been moved into settings observer because it already has its setting in
    QSTileHost and was causing a conflict
    
    Change-Id: Ib6b0de33e2619d6ff23bf2ccf2e01928e563cf90
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/qs/QSPanel.java

commit 96e43e71e5e3cf724fa027b3bb63c0d17249e3ee
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 14:16:40 2015 -0700

    QS: Housekeeping
    
    @temasek
    
    Change-Id: I8531874c868416750c6ae56b827967d2b3cff226

commit 615198b8a7a4062bfc64463ccce7d465a9d090c7
Author: PerfectSlayer <slimroms@hardcoding.fr>
Date:   Fri Apr 10 10:50:08 2015 -0700

    [1/2] Framework: Add network meter
    
    Add a network quality meter near to signal and battery meters.
    
    AICPfy
    Add it to msim layout
    Make it coexist with current Network traffic meter
    
    Change-Id: I140d276f353c14fa88972408be570f4ed8b850aa
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBarTransitions.java

commit 26209bfb1b641a7f32254be0025af8b7246bc677
Author: LorDClockaN <davor@losinj.com>
Date:   Fri Apr 10 10:57:01 2015 -0700

    REVERT old network meter and add color to new one (1/2)
    
    Add proper SettingsObserver for faster setting reaction
    
    Change-Id: I960127b32f0e4b61d700680a8fcd5ba1341469a5
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/policy/NetworkTextView.java

commit ef91b451027dd008bc19901b2550ce9e50a0650b
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Fri Apr 10 12:22:32 2015 -0700

    [3/3] frameworks/base: National Data Roaming
    
    Credits: CyanogenMod
    
    Linked commits:
            opt/telephony: https://gerrit.paranoidandroid.co/#/c/3655/
            services/Telephony: https://gerrit.paranoidandroid.co/#/c/3656/
    
    Change-Id: I0280d516067e1ef50f7321355cbee42009657d7e
    
    (cherry picked from commit 5f1e11e061209d2406ad088b428396ad9456546e)
    
    (cherry picked from commit 5f1e11e061209d2406ad088b428396ad9456546e)
    
    Conflicts:
    	core/java/android/provider/Settings.java

project frameworks/native/
commit 941f0894c770aee416625dc535191e462b98aa3d
Merge: 5876280 a6e339b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 16:55:55 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

commit 2d921f30854b347f39e4acb8ed4850a9ca633093
Merge: 941f089 96bfb46
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 20:02:11 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

project frameworks/opt/chips/
commit d9ebf239ba12450ba151909765c2849e197dad6c
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Apr 6 18:09:12 2015 -0700

    Chips: Add a view attribute for maximum number of chips parsed
    
    Additionally add a dynamic way to set maxChipsParsed
    
    Change-Id: I8e88d4268b8e2ecc6de26d8cf69a985821c8e9f0
    (cherry picked from commit c274746186af89f4c11499771678696d18158476)
    (cherry picked from commit 9f53ad13ad78945689c6e16aad127bdfca4c4779)

project frameworks/opt/telephony/
commit 0dff47990c779dbc7e734f641937720276f99daa
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Sun Jan 12 19:46:44 2014 +0100

    Return: National Data Roaming [1/3]
    
    Credits: CM
    
    Change-Id: Ibc20b5ed2bd8c94d8aa6fb0350caf819e82bfe98
    
    (cherry picked from commit 6eef83bb7c3032847bb4c58e5f874cebf18c7d06)
    
    (cherry picked from commit 6eef83bb7c3032847bb4c58e5f874cebf18c7d06)
    
    (cherry picked from commit 55d017d958929877e702af28e9872547f1e278ea)
    
    (cherry picked from commit 55d017d958929877e702af28e9872547f1e278ea)

project hardware/qcom/audio-caf/msm8960/
commit 5ec16a156c509b5f556923b6aaa869b815fd9a92
Author: Ramjee Singh <ramjee@codeaurora.org>
Date:   Tue Feb 10 12:05:38 2015 +0530

    audio: Retained VOIP Mute State during device switch
    
    On L, Audio Policy Manager closes all input streams
    during device switch. Previous mute state is lost
    when there is a device switch during VOIP call
    
    Fix is to reset mute state only when the call is
    disconnected and retain it during the device switches
    
    Change-Id: Iaa2ad525db92fdad4d598680f5ba96e74a8c3b9c
    CRs-Fixed: 773035

commit c37af8f41b8c369fb17585e0180027165da43630
Author: Ramjee Singh <ramjee@codeaurora.org>
Date:   Thu Mar 19 15:47:50 2015 +0530

    audio: add Fast profile for USB playback
    
    - Touch tones/fast outputs and Music uses AudioStreamOut.
     USB playback state is same for Media and Fast outputs
     that is MUSIC. Fast output is finished playback will
     clear MUSIC state in standby and it will lead to no
     state for USB even though music continues leads to close
     of USB playback thread.
    - Fix is to add different USB states for music and Fast
      outputs.
    
    Change-Id: Ic54ff8862af0097698f9851025478fee73beb5e8
    CRs-Fixed: 810889

project hardware/qcom/audio-caf/msm8974/
commit ef33462dda59536cfae67f1e3242d131699a8b21
Author: Weiyin Jiang <wjiang@codeaurora.org>
Date:   Mon Mar 23 00:54:14 2015 +0800

    post_proc: add support for virtualizer capability query
    
    Add extra virtualizer interfaces to keep align with aosp design.
    Extended capabilities include:
    - Stub interface to allow querying speaker angles.
    - Force set output device as specific virtualize mode.
    - Query virtualize mode
    
    Stub function remains to be refined in sync with upcoming aosp
    changes.
    
    Change-Id: I3316f6d944db1c9954eda7643a5ce433defa1a6c
    CRs-Fixed: 810294

project hardware/qcom/display-caf/msm8226/
commit d309069f3471f52a9d9bf12c6e176648ce96ff9a
Author: luca020400 <luca.stefani.ge1@gmail.com>
Date:   Tue Apr 7 21:19:21 2015 +0200

    msm8226: add libhdmi symlink
    
    * remove libexternal symlink
    
    Change-Id: I9416ee0f263cf80a21966c1b536fb602640dd50a

project hardware/qcom/display-caf/msm8610/
commit fa1ec5d33234b4c262121860a49fcc6bba64985e
Author: luca020400 <luca.stefani.ge1@gmail.com>
Date:   Tue Apr 7 21:19:21 2015 +0200

    msm8610: add libhdmi symlink
    
    * remove libexternal symlink
    
    Change-Id: I9416ee0f263cf80a21966c1b536fb602640dd50a

project hardware/qcom/display-caf/msm8974/
commit 0ecd91cc95a189e727e6063f3bd13809133a926a
Merge: 84a171c 6386275
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:22 2015 -0700

    Merge "hwc: Bump up version to 1.4"

commit 5ae0cb1fc47da97d929c8bfc221bbc42b5ed0f3a
Merge: 0ecd91c a04a34a
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:23 2015 -0700

    Merge "hwc: Clean up scattered definitions of commonly used constants/values"

commit fb902e5ab77dbe00246364ac5e8d81daf3afbf10
Merge: 5ae0cb1 aa83212
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:23 2015 -0700

    Merge "hwc: Clean up ExternalDisplay class"

commit 898c34fa0ef4034c84e1f92c2d6712ba99444cd1
Merge: fb902e5 12f41c9
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:24 2015 -0700

    Merge "hwc: Rename libexternal to serve HDMI as primary or external"

commit 1e26f9dfab60aa5d517af69e9af00e62286452ef
Merge: 898c34f eb2b327
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:24 2015 -0700

    Merge "hwc: Add support for frame rate change on HDMI devices"

commit 81365194aec9b0ad26b9eefedf060d3459b26326
Merge: 1e26f9d 165ec68
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:24 2015 -0700

    Merge "hwc: Fixes for HDMI primary/external use cases"

commit ff0a21898b5b1c3161c06a4d2daf91295704497f
Merge: 8136519 11cddc9
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Fri Apr 3 18:33:24 2015 -0700

    Merge "hwc: Fix for HDMI MDPScalingMode resolution issue"

commit 802135e44a4139c4384ec980158f232cbe12e2a4
Merge: ff0a218 7e07e8c
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Sun Apr 5 12:13:58 2015 -0700

    Merge AU_LINUX_ANDROID_LA.BF.1.1.1_RB1.05.01.00.042.029 on remote branch
    
    Change-Id: I4f7579bc9f7a185a1fd01ce4338c153ace2ce170

commit 2d44d682e8a7dd3bd190bf7f18b19c0655425c41
Merge: 7260568 802135e
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 7 13:50:55 2015 -0400

    Merge branch 'LA.BF.1.1.1_rb1.18' of git://codeaurora.org/platform/hardware/qcom/display into cm-12.1
    
    Change-Id: I198e3dafc24aa137cb5492cfe0b989ac162d0223

project hardware/ril/
commit e732d9aa6d8988dcfc40f1f53b1709b94a3bdf71
Author: Matt Mower <mowerm@gmail.com>
Date:   Wed Apr 8 23:16:03 2015 -0500

    ril: Add missing unsol response strings
    
    A few unsols are handled, but strings are not passed to the log when
    requestToString() is called. Also, re-order a couple entries to match
    the layout in ril_unsol_commands.h.
    
    Change-Id: Ie6f1b49ff0245212e64d4e563a26ea93191deb22

project hardware/samsung/
commit e32dbfd56b6ee0152a320fad990350baf52a3240
Author: Howard Su <howard0su@gmail.com>
Date:   Wed Jan 7 15:55:57 2015 +0800

    libril: Merge xmm6262 and xmm6260 to single lib.
    
    The difference between two libs are very minor,
    includes one hack around ucsInfo and the logic
    to adjust signal strength. Besides that other
    diffs are some logs.
    The new version of code is minaly based on xmm6262,
    especially the logic to adjust singal strength.
    Merge them to easy maintain the code.
    
    Change-Id: I76390541d017576591860c8701bb9763c460b8be
    (cherry picked from commit 56b8dcfa3094f93698dda9f6731fa845f00ef287)

commit eeb7df7cf49f6abc3c185818da43f3054dc2e29b
Author: K Yasu <kyasu.m2@gmail.com>
Date:   Tue Apr 7 22:10:03 2015 +0900

    Fix the build error of some samsung devices which provides libril (e.g. ks01lte)
    
    This fixes the merge error of commit 56b8dcfa3094f93698dda9f6731fa845f00ef287
    
    Change-Id: I0efd718a85376059cad57ac9715673cbfb2e596f
    (cherry picked from commit f8e5e164804f1408c2350dade3fd92d561e7076c)

commit 68f80d8f04de1cac9ed34f9a29e69e1ad91615c4
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Tue Apr 7 19:13:42 2015 +0200

    libril: Fix processRadioState prototype
    
    Change-Id: I19c5c2319fe4110c3859012a27a08d5c7f942177
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

commit 8e5fa432f3f0e0c9cad389a5615952289350242c
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Tue Apr 7 19:14:05 2015 +0200

    libril: The data variable should be const
    
    Change-Id: I72a694e603c1ff18b09e3c3208cae8c5af937513
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

commit 8cb8de66bb7582d390e9c25da9bc143042433c54
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Tue Apr 7 18:58:14 2015 +0200

    libril: Use consistent names for modem defines
    
    Change-Id: I3ac65d2458878a6a631439be4f830c851aa50759
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

commit f68609b5d2c639bc673a5081b85f56ee7423f59e
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Tue Apr 7 19:01:34 2015 +0200

    libril: Fix #elif for MODEM_TYPE_XMM6260
    
    Change-Id: I71e64103aba6b374b6181f557030409be084bb25
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

commit eef440e4ab77f3bf3564ea9f8d4429cfec9f379e
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Tue Apr 7 19:01:54 2015 +0200

    libril: Readd support for MODEM_TYPE_XMM7260
    
    Change-Id: I395e9cbfd1a42334e5e6bbb706eef9be157ecd24
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

project packages/apps/Bluetooth/
commit 785152b1aaef67e1ac913457c1e3c2d534bff20a
Merge: d9238c1 f55ccba
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 4 14:41:52 2015 -0400

    Merge branch 'LA.BF64.1.2.1_rb2.6' of git://codeaurora.org/platform/packages/apps/Bluetooth into cm-12.1

project packages/apps/Browser/
commit 59bf41543aa2638a4ce536833316f4903df2bfd4
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Apr 3 05:07:12 2014 +0200

    browser: allow to load browser internal assets
    
    The new webview classes avoid to load urls from local file schemes.
    Just replace the load of internal browser assets (most_visited) from
    loadUrl to loadData.
    
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>
    
    Change-Id: Iee633a1a3599a7e752e15452fa04e15baac2e256
    Cherry-Picked: http://review.cyanogenmod.org/#/c/62126/3

commit 8846850ed41922b02c24aac416f8bb6bda122056
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Dec 11 03:48:24 2014 +0100

    Browser: switch from green to blue
    
    Change-Id: I0dd8e0de1ce8383b3c19fb4551969263d0233fce
    (cherry picked from commit f587c1c1f57cc3d6916425bc5d82c9c3db8d5760)
    
    Conflicts:
    	res/values/colors.xml

commit 0dd29b5181d24185d5cb71371d2ca3b975a20ef1
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Dec 11 04:40:07 2014 +0100

    Browser: and moooore material girls in blue
    
    ;)
    
    Change-Id: I8973ab613d425e311454ae0a8abbb0312acedf3c
    (cherry picked from commit 7af0cab9c117049f8e81c013fc24eb9875aa7e41)
    
    Conflicts:
    	res/layout-land/nav_screen.xml
    
    Conflicts:
    	res/drawable-xxhdpi/progress.9.png
    	res/layout-land/nav_screen.xml

commit f6ec4a9e4c69c6f691b067fd317aa0a1a4ac3644
Author: dankoman <dankoman30@gmail.com>
Date:   Thu Dec 11 19:35:01 2014 +0100

    Browser: fix incognito icons and preview thumbnail color
    
    Change-Id: Ib4c5c0b95b63b439e39afede8c99134c91b7f724
    (cherry picked from commit 3d7dd283a95c5ee333b74561c9161d380503128f)
    
    Conflicts:
    	res/drawable-hdpi/ic_incognito_dark.png
    	res/drawable-mdpi/ic_incognito_dark.png
    	res/drawable-xhdpi/ic_incognito_dark.png
    	res/drawable-xxhdpi/ic_incognito_dark.png
    	res/drawable-xxxhdpi/ic_incognito_dark.png

commit d18bb683fbbff58cf95be58644a7cb83a92c144a
Author: dankoman <dankoman30@gmail.com>
Date:   Fri Dec 12 15:51:57 2014 +0100

    Browser:  fix sizes
    
    Change-Id: I24a6aeeb3a2f30f8d182491e863677b645569856

project packages/apps/Calculator/
commit 147b8fd6e8fa907d663da56239a47c7d433224ee
Author: Bryan Owens <djbryan3540@gmail.com>
Date:   Wed Apr 1 01:30:49 2015 -0500

    Expose hard coded background and text colors from layouts for display background and floating history text entry.
    
    Signed-off-by: Bryan Owens <djbryan3540@gmail.com>
    
    Change-Id: I0ae08c79a049998bf44e8f0473ab5dbd9fa51396

commit e849cd120e3f818cd877c2a135347d15d093bb1f
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Fri Apr 3 14:01:20 2015 -0700

    Stop ', NaN' from showing up; instead syntaxexception should be thrown.
    
    Repro: enter "0 / 0" then press equals
    
    Change-Id: I66eb2a934b36e7158a58568e03c872b90b7527ba
    (cherry picked from commit 6085741c225b5c494e475b25ec6f9d20198ecf6d)

commit 847d66626be6b81af93ce019c00df6f31ea611fc
Author: Bryan Owens <djbryan3540@gmail.com>
Date:   Mon Apr 6 00:22:08 2015 -0500

    Expose hard coded background and text colors for graph
    
    Signed-off-by: Bryan Owens <djbryan3540@gmail.com>
    
    Change-Id: Ib1bec0b4db5e956cfe1edbfeec344febb7d7da92

commit 16ee73f00b24bd57d9ec4ad8b8f34dc1016f0497
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 7 03:55:04 2015 -0400

    calculator: Fix the build
    
    Change-Id: If016cae972f97eab98a00813ce400dcaafd3aa42

commit 159eb36392fb5cd2341f45c66f67d9e0dc185cd9
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 9 13:10:36 2015 -0700

    Calculator: fix error handling ripple
    
    Ripple starts from mCurrentButton, but it was never updated on button
    click.
    
    Change-Id: Ifcf60a94dbba915ee71f96e7ad68b222c243f43d
    Signed-off-by: Roman Birg <roman@cyngn.com>

project packages/apps/ContactsCommon/
commit 38c39f987b7bdcdb47277903dd20b350bdeba21f
Author: Pawit Pornkitprasan <p.pawit@gmail.com>
Date:   Sun Apr 5 19:30:08 2015 +0700

    ContactsCommon: fix NPE on importing contact with multiple accounts
    
    java.lang.NullPointerException: Attempt to invoke virtual method 'void android.content.Context.startActivity(android.content.Intent)' on a null object reference
    	at com.android.contacts.common.util.AccountSelectionUtil.doImportFromSim(AccountSelectionUtil.java:232)
    	at com.android.contacts.common.util.AccountSelectionUtil.doImport(AccountSelectionUtil.java:211)
    	at com.android.contacts.common.interactions.ImportExportDialogFragment.onAccountChosen(ImportExportDialogFragment.java:333)
    	at com.android.contacts.common.editor.SelectAccountDialogFragment.onAccountSelected(SelectAccountDialogFragment.java:113)
    	at com.android.contacts.common.editor.SelectAccountDialogFragment.access$000(SelectAccountDialogFragment.java:36)
    	at com.android.contacts.common.editor.SelectAccountDialogFragment$1.onClick(SelectAccountDialogFragment.java:86)
    	at com.android.internal.app.AlertController$AlertParams$3.onItemClick(AlertController.java:1082)
    [snip]
    
    Change-Id: Id07857200cb341ce916da46c5be852c0573f65f2

project packages/apps/DeskClock/
commit f4eb401489d941674fe51b05d468ee666899f47f
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Apr 2 15:55:58 2015 -0700

    DeskClock: re-write delayAlarm for intercepting alarms when in-call
    
    While the previous clean-up was necessary, it no longer meets the spec.
    This feature needs to trigger the alarm immediately after the call finishes.
    
    Change-Id: I71107277926c891f79b1e46fb27878994ac15ce0
    (cherry picked from commit 544c5e8365499611d627d84ebc6b899f1860811b)

project packages/apps/Dialer/
commit 9c45e51e9218f692501a03f7c1cd5cfe94358fcb
Author: Pawit Pornkitprasan <p.pawit@gmail.com>
Date:   Sun Apr 5 13:05:48 2015 +0700

    Revert "Dialer: truncate hint text for search box"
    
    This is fixed in AOSP 5.1
    
    This reverts commit afd6610cd2f0760e17a7e42719dd85f1a8f9becc.
    
    Change-Id: I483159a3210286da909ffa4ad715f638e6f20182

commit 4b4b9ad2964929b8552d92c42d6f77a83531d150
Author: Kryten2k35 <kryten2k35@gmail.com>
Date:   Tue Mar 3 14:26:34 2015 -0700

    Call recording encoder/format choice 1/3
    
    PS1: Adds a user option between NB AMR (the default) or HE-AAC for the encoding of call recording audio. Also changes the output format of the file appropriately (NB AMR now uses the NB_AMR output format and HE_AAC chooses the MPEG_4 output. File extensions are adjust accordingly as well).
    
    This was in reponse to people complaining the quality of call recording audio is poor. It's noticibly better using HE-AAC, but filesizes are larger.
    
    PS2: Removed unnecessary code in DialtactsActivity (see Teleservice patch). Removed whitespace and changed coding style to meet the standard
    
    PS3: Fixed whitespace, finally!
    
    Change-Id: I95620bf944e18491652c716890396c3da4be70c4
    
    PS4: Imported from kitkat and made working for lollipop.
    
    Signed-off-by: BlackDragon <blackdragon.fusionteam@gmail.com>

commit 6988778d7bdfd7b50a2cdf9170e109711d9b675c
Author: martincz <martincz@mokeedev.com>
Date:   Thu Apr 9 22:18:15 2015 -0700

    Dialer: Direct Call (3/4)
    
    PS2: Change location of Proximity sensor java file.
    
    Change-Id: I6709f2a00852cb1021fc46114ee9810c03d86876
    
    Conflicts:
    	src/com/android/dialer/dialpad/DialpadFragment.java

project packages/apps/InCallUI/
commit a441cea12dcfe335becad1e60892d0cb867bb68a
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Apr 6 14:29:38 2015 +0200

    Fix broken string reference usage.
    
    Change-Id: I422d5a7534b0ac2714cb92b2de3b8ea9f90ba9bb

commit 3e5d3f0907d17819718b885d57fa0d835b525b1d
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 7 08:55:06 2015 +0200

    Properly unregister supp service failure receiver.
    
    Change-Id: Ib2929c848f7cf63a9c037613647db549efbcf923

project packages/apps/KeyChain/
commit fc3b9e43dd71fb38bcedb7735ec81451aec6716d
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Tue Apr 7 23:08:51 2015 +0200

    Revert "KeyChain: Fix certificate dialog needs twice Cancel to disappear."
    
    This reverts commit 250c621d61859fe9db6338a7b5c42bff5c3e2d92.
    
    This change breaks the callback invocation caused by finalization of the activity
    before the responder asynctask finished, so sender will never received the
    user selection. This breaks, for example, exchange certificate requestor.
    
    Change-Id: I152984a194be543fdf71658aa85da8de5c7312f7

project packages/apps/LockClock/
commit 97a36704aacc7aef49a971a0bfeacd77154818fc
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Wed Apr 8 02:38:51 2015 +0300

    New Material icon
    
    * Created by Jovie Brett Bardoles
    
    Change-Id: Iff67e8e347c2c21ccbdc4618fb0603ea5a0bb625
    (cherry picked from commit c0a0b63cb148a038a71985f900eac113e630f8b5)

project packages/apps/Mms/
commit 3608041ffd1887e666116dbd0667529a8d84e344
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Apr 6 16:15:58 2015 -0700

    Mms: Fix for adding too many recipients to the Message
    
    There is a lot of jank when the user adds a large number of
    recipients to a message. This is because of the appends required
    to notify the RecipientsEditTextView of the new contacts that
    need to be "chipped." This is results in an unmanageable amount of
    work being done on the main thread. This workaround turns off
    chips when the user adds 15 contacts. RecipientsEditTextView already
    has an internal max of 50, but this is too high for this batched
    recipient entry.
    
    Change-Id: I1a292302ec783ebf75f48ab4aeac30645297df1f

commit c8319d36fe478ec3652b6535a5d32df4e98fa443
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Mar 30 11:08:28 2015 +0200

    Use subscription ID instead of phone ID.
    
    The subscription ID is more fine granular and is part of the API 22
    contract, so prefer it over the phone ID and populate it in the DB.
    
    Also fix a couple of slot ID <-> subscription ID mixups.
    
    Change-Id: Ia43b2a64b33a9bb366635f7678aa0582c81c238f

commit 06e2220148534d8ae8515080bd2194e071bf7dbc
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Mar 30 12:14:53 2015 +0200

    Replace slot spinner by subscription spinner.
    
    Change-Id: Id306b31eebda4596258c403e0e69e4f754604dc0

commit b0cb1718ed633787e625f9747e74320d3b464ba8
Author: Danny Baumann <dannybaumann@web.de>
Date:   Thu Apr 2 09:07:41 2015 +0200

    Replace some home-grown summary management logic by a simpler version.
    
    Change-Id: Iab989f6c738c376ab36752b7ddad352bd4476278

commit 95abfab428cd16d8d0fe49ca3fafe66692b3acdb
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Apr 8 18:14:29 2015 -0700

    Mms: do not populate RecipientsEditor while mAddNumbersTask is running
    
    Repro (~50% or less)
     - Open a new Message
     - Click the select recipients button
     - Click done
     - Observe: no recipients were added
    
    Change-Id: I34a4de7ef4bc6f88b66535f46bbd14b7bfaf163c
    (cherry picked from commit af78a28ee219d557a7bf94df56e526dd70f0ac49)
    (cherry picked from commit 79df913a9d538f228593e4eb676a899472cec791)

commit 0b6da5c6cf8f3ff03107a6242a4f90c527d7dc54
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Apr 9 11:11:26 2015 -0700

    Mms: add a drawable for the calendar event
    
    Change-Id: I367e44f98b217afe4ae5eb9336e6fcf0358d61cf
    (cherry picked from commit 3c3806adc3bad904d07b87d0b597ad16bdf142d9)

commit 153b227b529c63275f356b61318a8bbf940222bc
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Apr 9 11:49:46 2015 -0700

    Mms: use string resource for Select Recipients progress dialog
    
    Change-Id: I019514ffecdb43baac62ce3c2f63552b15408420

commit 9cdc5d5b704800aa9d35fc33f2e21df355accb77
Author: martincz <martincz@mokeedev.com>
Date:   Tue Mar 3 14:32:53 2015 -0700

    Mms: Direct Call (4/4)
    
    Change-Id: I2d3807150c12349bdcf2eda10904faf28f42169e

commit 30c04959a777174583aa9441c2166b13579e0a9e
Author: Bajee11 <bajee11@gmail.com>
Date:   Sun Feb 22 02:18:07 2015 -0700

    [2/4] Mms: Breathing missedcall/sms/voicemail
    
    Base: https://gerrit.omnirom.org/#/c/4976/
    OmniGears: https://gerrit.omnirom.org/#/c/4978/
    Telephony: https://gerrit.omnirom.org/#/c/4979/
    
    Change-Id: Id12182719315a6e5bcbabd8f843eff70c8c3ed3a
    
    @alviteri: Port by me to crDroid Android
    
    Conflicts:
    	res/drawable-hdpi/stat_notify_sms.png
    	res/drawable-mdpi/stat_notify_sms.png
    	res/drawable-xhdpi/stat_notify_sms.png
    	res/drawable-xxhdpi/stat_notify_sms.png
    	src/com/android/mms/transaction/MessagingNotification.java

commit bb2d9191ec99598633eeb2ae8794dbe3ca5dcfe6
Merge: 30c0495 153b227
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 22:38:58 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

project packages/apps/OmniSwitch/
commit 2d64ac761622700fefb674b93a6b79ab5b75aa1b
Author: david <davidteri91@gmail.com>
Date:   Sun Feb 22 17:00:22 2015 +0100

    OmniSwitch: Hide from Drawer Launcher
    
    This was picked from the following commit: b282406fc52ba910210ebb40f23e8bde5612de57

project packages/apps/PackageInstaller/
commit ba58bf85f3983557d62e6d78d44e38f72c5541d6
Author: Dirk Rettschlag <dirk.rettschlag@gmail.com>
Date:   Thu Dec 12 16:08:07 2013 +0530

    PackageInstaller: Show current & new version
    
    Change-Id: Iee10d988c095475e1ccbcea7a9c64d9e114d79e6

project packages/apps/PerformanceControl/
commit b18c0df1df2184587ae3f3d62ba15bdaa9543f8c
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 02:06:06 2015 -0700

    Revert : [2/4] PerformanceControl: power profiles
    
    Change-Id: I68d009212e1bf7498ae10b461b2027088c96a8a9 (reverted from commit f6edc2a61949619e77b553e1b83ee88390e60fa0)
    PerformanceControl: always reload installed apps for power profiles
    
    Else you cant set profile for new installed apps right away
    
    Change-Id: Ib4714735120e7648d0ea920debfa2a53a2d3dfeb (reverted from commit 3225ba7427dd57c3fcf83dd9da22994ea2795c09)

project packages/apps/Settings/
commit eedf62168aaf8a06ef5681d3691c5218dbc8cd5d
Author: Allan Hedelain <tristan202@gmail.com>
Date:   Fri Apr 3 13:28:33 2015 -0700

    Add margaritov colorpicker from SlimRoms
    
    Change-Id: Iff172ffcfcdef5b3338eadf2dd479743bdf5c290
    
    Conflicts:
    	res/values/pac_strings.xml

commit 6c9dd3c7bf8b8830d9e499f99bc8da69e6f4c62a
Author: faust93 <monumentum@gmail.com>
Date:   Sun Dec 21 02:27:47 2014 -0700

    Wakelock Blocker [2/2]
    
    Change-Id: Ib765e0478ed71fa11a51546c0359f7cd10539a58
    (cherry picked from commit 5d65f7a25eb5d07e6584a03a9188bc58bb9f9a50)
    
    Conflicts:
    	res/values/cmr_strings.xml

commit ddaa86dca8c2542f6ef01a8c9f319e2174bf2f26
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Dec 21 02:38:45 2014 -0700

    add dslv controller
    
    a lot of our settings have drag swipe features
    this is the central controller for it to have
    easy access
    
    Change-Id: I665b9128fc370b194fee9f35fa17879d4f685fd6
    (cherry picked from commit 56b7fc9fa99512e87bb848262b97b9f71a08682f)

commit a00232df121276941b6321091db7a201e4b462e7
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Fri Apr 3 13:33:49 2015 -0700

    Settings: add central slim ActionListViewSettings class back...
    as well shortcutpicker helper and several other stuff which is needed
    for nearly every feature we have regarding navigation or shortcuts.
    
    Imported from kk
    
    changes:
    - Renaming to be inline with fwb part
    - code cleanup
    - disabled code where features are not present till now
    
    NOTE: This patch from graphics group is needed as well
          https://gerrit.slimroms.net/#/c/19987/2
    
    Change-Id: I6671287c40f0711a2347c1457396487217278dad
    (cherry picked from commit 5907cb206b22835404620f5611e78e2f9add0c64)
    
    Conflicts:
    	res/values/cmr_arrays.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit deb7f94eeb92926769690d098d42c5e9e6af2225
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Dec 21 02:49:13 2014 -0700

    Settings: add a default slim actions array
    
    Change-Id: Ice789c2331fa60fe421f642884285a4a7ae6f0c3
    (cherry picked from commit 22ea1f155b1c428a95890395363c669600abf0a3)
    
    Conflicts:
    	res/values/cmr_arrays.xml

commit 49605ac3352a4c4b65ec497300cf73c8e2db2332
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Dec 21 02:51:41 2014 -0700

    Settings: add default slim actions for screen off gestures
    
    Change-Id: I374ef8e5b9aef8d9381a97b3ebf8240fbf4cabef
    (cherry picked from commit 25f89f403b7ec754a11135a43eb43653eae6222c)
    
    Conflicts:
    	res/values/cmr_arrays.xml

commit 48b6f63ea68fa6dc03a6734d3ac7fb038d0058aa
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Dec 21 02:53:23 2014 -0700

    Settings: Materialize DSLV
    
    Change-Id: I8efe75ee2b571136a7983b9a0b36090294650c80
    (cherry picked from commit 084414271597553f169a9389c512ddeb84a99b71)

commit f41a1ef03c54bb41842deb4dcc1230d67d1907c8
Author: dankoman <dankoman30@gmail.com>
Date:   Mon Dec 8 22:09:26 2014 +0100

    Settings: materialize grabber icon
    
    Change-Id: I74908674c8d6b5e5f3fbca8e54778c8d9d9dd6b7
    
    (cherry picked from commit 5b1320fab67aae1ad4cb093d002d2e56a44c7047)

commit bad92be3cadeb88966935978fa561297e390e5aa
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Fri Apr 3 13:36:00 2015 -0700

    Settings: add user configurable lockscreen shortcuts (2/2)
    
    Change-Id: I6333792830f7357a9f4fcd5d42c479ec60a71915
    (cherry picked from commit e76ab278d01621143a1c5624a072cf1ab8cb4088)
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 1486357d3e47cabd17bc0a008c6e02507ea41371
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Wed Dec 10 19:53:14 2014 +0100

    Settings: its not an icon anymore...its an option
    
    we moved reset option on dslv into the menu. So the help text is a bit missleading.
    
    Change-Id: Ic502f668432ac76ffda03a9221bd28dabbc889c2
    
    (cherry picked from commit 2dc9f32467876e95b8a046d66a699c608d362eaf)

commit fb1e9b69cdbb19b2bc06d273fd46773fdcbfc96e
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sat Apr 4 00:39:16 2015 -0700

     [Settings] Nav bar tweaks + HW keys tweaks
    
    - Toggle on/off (CyanogenMod alredy did but only for hw keys devices). crDroid allow all devices to do that for those using PIE apps.
    - Nav bar dimensions (height and width)
    
    PS: THIS COMMIT IS A SQUASHED PORTED FROM crDroid KK and 99% od the codes are from SlimRoms. I want to say a HUGE thanks to @kufikugel
    
    Conflicts:
    
    	res/values/cm_strings.xml
    	res/xml/button_settings.xml
    	src/com/android/settings/ButtonSettings.java
    
    Change-Id: I1a61338996985d722c829c23efb13b22ca7781a5

commit 56347b0881d49afe60d17577f24d32302aa071e6
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Apr 3 20:07:52 2015 -0700

    [settings] long press back to kill configurable timeout (2/2)
    
    1 - 2 seconds (default)
    2 - 1,5 seconds
    3 - 1 second
    4 - 0,5 second
    
    Forward ported from crDroid kk
    
    Conflicts:
    
    	res/values/cmr_arrays.xml
    	src/com/android/settings/DevelopmentSettings.java
    
    Conflicts:
    	res/values/mcr_strings.xml
    
    Change-Id: Ib773d4e3f066b299b216329610968e269af2887a
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 38aa324a5c318ab0b0c52739a89fdf82eb5ef3fc
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 20:30:18 2015 -0700

    Add back CMRemix helper pref that holds a system setting
    
    Base on CM
    
    Change-Id: I56e7ad049bd932cc4d6ef57e14bfd1a0c9103eb0

commit 0d5533ef5dc7c0567ccdeae01a9a8e84da7efa9c
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 10:48:00 2015 -0700

    add changelog to cmRemiX Settings
    
    Change-Id: Iece3b482076a009b208e1407c7664a10e76fb3bb
    (cherry picked from commit 592e2a5bb3d71374307dc3f358ec706a1295bfc5)
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/cmr_main_settings.xml

commit def6377f361c66687db12dbaf3f22bb0b6c989a6
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Sat Nov 29 22:30:14 2014 +0100

    Fix ADB Notify Reset on USB Debugging Toggle
    
    Change-Id: Iea299577463cf3b40d245bd50a18a1dcb2a7cbf9
    
    (cherry picked from commit 6b9a47cab752e6594e5de92213c4f593c4c64e55)
    
    (cherry picked from commit 2fd251fc0beb9fe10d88da937ee9f35754e27494)
    
    (cherry picked from commit 2707d85b12c568396e42935032e9f751a2d1b05e)
    
    (cherry picked from commit 5dd2a1af834072d77a4f47c2d9b739aec5ac3683)

commit 6a15dd387c9655b14a8e280121b00c87c4397db9
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 16:09:38 2015 -0700

    Partition Info
    
    Change-Id: I75ddf1638e0ef252a5c0d5fc5a6d5956a448e287

commit b90abb8100f7dce483b53ffe893389ab8bf5581d
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 16:11:38 2015 -0700

    Partition, cpu & ram Info
    
    Change-Id: I75ddf1638e0ef252a5c0d5fc5a6d5956a448e287

commit 7ecd962fdc661e8c0680a215356e1f0b3e73b3a5
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sat Apr 4 16:13:59 2015 -0700

    cmRemiX Extra Info
    
    Port from our Kitkat branch
    https://github.com/DirtyUnicorns-KitKat/packages_apps_Settings/commit/6274d966b15d2a0a910d99aa3f13816f89746763
    
    Change-Id: Iaaa2c137b857dc8ddc73f1464063c1f806bb12f7
    
    (cherry picked from commit e6edea03ab25b8337d3517e701b92bdccce2d601)
    
    Conflicts:
    	res/xml/device_info_settings.xml

commit 18f203773f9830fc162a4f37acaf331c5e459599
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 16:16:56 2015 -0700

    [SQUASHED] [2/2] Settings: Status bar Network traffic
    
    This codes are not mine an here i'm giving the proper credits
    
    Commits inside and they authors:
    @tectas: omnirom/android_packages_apps_OmniGears@2dc8674
    @Haus1: omnirom/android_packages_apps_OmniGears@cac09ff
    @Haus1: omnirom/android_packages_apps_OmniGears@391eadd
    @cristianomatos: 2f817be
    
    @alviteri: Added SeekBar from KK for autohide and Switchialized
    
    Change-Id: If404b17fd21d852e8398d05122bdc3a3a611e825

commit 521757841b11f6a632eeed8924db9bd24aee1139
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sat Apr 4 16:16:56 2015 -0700

     Settings: Network traffic supercharged (2/2)
    
    Bring back AICP kk traffic
    Add back SeekBarPreferenceCham for it
    
    Change-Id: I91d409dc72a8b526fc8d279d62d5fae7fd6ba52c

commit 8d6e76e70aefe3e10372b259b827607fbb3686ed
Author: undefined <undefined@codebug.es>
Date:   Fri Dec 12 14:34:07 2014 +0100

    Settings: Wi-Fi WPS Materialized icon
    
    Both aosp and factory images the icon is not visible
    
    Let's make it visible and materialized.
    
    Patchset: redraw vector and add xxxhdpi versions
    
    Change-Id: I00580cfb719dd955f243b24afd186ee2c8f9cad0
    
    (cherry picked from commit 63a8c7c18d5d63d4041aa7b617c7ea23ebdd1253)

commit 9abda1df950a09688486c099f605d86c78cc7f7b
Author: 0xD34D <clark@scheffsblend.com>
Date:   Sun Apr 5 13:30:47 2015 -0700

    Gesture Anywhere [2/2]
    
    Change-Id: Ifd1d6752afa680ccd2db3ba9a73825ca7417f399
    
    Conflicts:
    	AndroidManifest.xml
    	res/values/cmr_arrays.xml
    	res/values/pac_strings.xml
    	res/xml/cmremix_tweaks.xml

commit 022812d564af5821b2127d70227e4b0c390cb1bb
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sun Apr 5 15:26:36 2015 -0700

    [SQUASHED]: recents panel clear all button tweaks
    
    Including
    =========
    Settings: omniswitch as default recents (2/2) by maxwen
    
    Conflicts:
    	res/drawable/ic_cmremix_ui_settings.xml
    	res/values/cmr_strings.xml

commit 5e9c429a87338b478fb47760718e3cca9343ce6b
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 15:37:25 2015 -0700

    Settings: Remove all bug report options
    
    removed it just in the xml which is a pretty bad idea if java code
    still assumes it is there.
    
    Due that we will never need it we remove the code completely.
    
    As well remove bug report in power menu option.
    
    Change-Id: I234dee3a19639f89b5a7b5295ca408142e4223dc
    
    Conflicts:
    	res/xml/development_prefs.xml
    	src/com/android/settings/DevelopmentSettings.java

commit a4995a77b212a1789040ca0774b827ad7ec8c7f2
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Fri Apr 3 19:33:11 2015 -0400

    Revert "Settings: Disable contributor cloud for now."
    
    This reverts commit 9ad27a5f7aa6adac322f4884daf3ccdb75d16bad.
    
    Change-Id: Iaa011448f4e517a181f3a2d25c231e2a78cea3c7
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit 624ab3ba976e96a44832860d1603382ea704effe
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Fri Apr 3 19:34:11 2015 -0400

    Revert "Add CM Legal"
    
    This reverts commit cf9656946a5ae9713c3fa57a905c2b258ad6cae1.
    
    Change-Id: Ic236131f35d1bfe418e8ecccfb2b791858e0f4b6
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit bac7dcc8bd8eeda35afd401c3837e048cfed3682
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Fri Apr 3 19:36:00 2015 -0400

    Revert "Settings : Add contributors word cloud"
    
    This reverts commit 721dcced980ab935321b8370f61d3cf9d76d00cf.
    
    Change-Id: I196cac9b6b845430ab2226a9d74795d4f6150b1d
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit 9a881fb03a17c989b7cdd2a1616540e2f6195ac2
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Fri Apr 3 19:36:26 2015 -0400

    Revert "Settings: Add FOTA updater"
    
    This reverts commit 8f11aab272e0bcde0b975acac9b53924bb9cc09d.
    
    Change-Id: I344283561309c694d6d024070c67c5cc201bf503
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

commit 2ef3c00a32f6d5c336a883ce7dea074eb286cc4c
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Sun Apr 5 15:43:00 2015 -0700

    Revert "Settings: Add CM Updater"
    
    This reverts commit 5b08cdc5ef7e2fa4c5d633ba01102b6cb1db193a.
    
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    Change-Id: Ie95ab0c3fc2fb78e8e8adbe06432ccfa00bac33e
    
    Conflicts:
    	src/com/android/settings/DeviceInfoSettings.java

commit fe06b109deb3a0193da978b5244ae91a73ff5e0d
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sun Apr 5 15:46:09 2015 -0700

    Settings: Media Scanner on boot behaviour (2/3)
    
    Settings part - fb part is merged and mediaprovider repo was patched up to LP
    
    Change-Id: Ib9cf62b0e3550e6557248cd3d910908882a91c7f
    (cherry picked from commit e7091f63866af809966cbef5b30270ed817b3a6b)
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/device_info_memory.xml
    
    (cherry picked from commit bc8437937b641b0da9a0acf787f05a7de11ad80d)
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml

commit 977f4000b85272d2160225ba2d8d547926f8a09c
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 16:47:34 2015 -0700

    add vector drawer for wakelock blocker
    
    Change-Id: Icd3d8469c47bdbe88ddf69d6ec09a7a06d50b50d

commit ccc22c6aa738dca10ea7d8ea44080f6a79688ab8
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Mon Apr 6 00:19:15 2015 -0700

    Settings: Implement App circle sidebar [2/2]
    
    Change-Id: Ia3f50e1d67c8a19ad9ce704e6a096caa2f17602a
    
    Conflicts:
    	res/values/pac_strings.xml
    	res/xml/cmremix_tweaks.xml

commit abf9b210e01368fff58684252b82a57aa5296246
Author: Stevespear426 <stephen.k.spear@gmail.com>
Date:   Sun Apr 5 18:56:11 2015 -0700

    Settings: All in One Animation Control [2/2]
    
    Allow configure System, ListView, Scroll, and Keyboard Animation
    
    * System from
      AOKP Animation Control https://github.com/AOKP/frameworks_base/commit/015c9cf00a8e49aea22d70b57b0af87c9134be73
      thanks to Steve Spear <stephen.k.spear@gmail.com>
    
    * ListView Animation https://gerrit.omnirom.org/#/c/2863/
      thanks to jkl5616<jkl5616@gmail.com>
    
    * Keyboard Animation https://github.com/zst123/XuiMod/commit/975cd531a9a847769b2af306495643a55ec44aaa
      thanks to zst123 for patches
    
    * with slight modification to OmniRom
    
    * Scrolling Animation https://github.com/zst123/XuiMod/commit/48c180cfa762617f59b4ceb3da50a6c28befe24f
      thanks to zst123 for patches
    
    * add toast animations
    
    * add separate option for them
    
    Change-Id: I89d880250867c41aecbb4cbe3ba1d473e780ebb4
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/pac_strings.xml
    	res/xml/cmremix_tweaks.xml

commit 432530becf2424b02dafa8f1634888556425c199
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Sun Apr 5 19:17:35 2015 -0700

    AOKP animations: Add and entry for TRANSIT_TASK_OPEN_BEHIND [2/2]
    
    Change-Id: I7a8f4ea6602ff34fd1bfe39e08549b81c90c5e12
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/system_animation_interface_settings.xml
    	src/com/android/settings/cmremix/animations/SystemAnimationInterfaceSettings.java

commit 8ef574eb5b10c993e86410f32f578c554d0eb4c5
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Sun Apr 5 19:19:02 2015 -0700

    System Animation updates
    
    Change-Id: Ibb872aa2a2b33be1fec05336a578974c94ea7cf6
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    
    Conflicts:
    	src/com/android/settings/cmremix/animations/SystemAnimationInterfaceSettings.java

commit e1abc0e27431d7c38c9403ff1c49c28cd45e5a85
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Feb 12 22:08:44 2015 -0700

    add vavious icons from DU (credit Alex Cruz)
    
    Change-Id: I9dc47942bdc0439d17b64c6f67ef39f09ae1da4d

commit 3307f1ec5757eedc40359e6b57504daf84676020
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 5 21:36:30 2015 -0700

    moved recents show search_bar from display to cmremix recents settings
    
    Change-Id: I0d923571b4851ac6168e38fd3b8bf12edaab9aa4

commit 1d7c741444f25ddd2d280a29ccb171f7a2299c2b
Author: alviteri <davidteri91@gmail.com>
Date:   Wed Mar 11 12:28:51 2015 +0100

    Settings: Rework 'add ability to change the color in battery saver mode'
    
    Adapt to new changes following cm's one
    
    This update the following commit: 152650ed3a20bc777f1f8e6c474c506e9b304975
    
    Change-Id: Ib09bba559a75b1bace013ae9a275f0a60a97b068

commit ae239105b940fd1616d43f22b22b06b6c08717db
Author: Yin Liu <yin2.liu@sonymobile.com>
Date:   Fri Dec 14 11:48:52 2012 +0800

    Fix memory leak issue in application settings
    
    If opening Main menu->Settings->Apps, and rotating the phone
    about 50 times, Settings force closes and out of memory occur.
    This is because after ManageApplications onDestroy, references
    of ApplicationsState have not been release. So, they will not
    be garbage collected. It leads to OOM and force close. To
    avoid this we need to release the references of
    ApplicationsState when ManageApplications onDestroy.
    
    Also, when exiting ManageApplications or InstalledApps in
    Settings there is a memory leak due to not releasing some
    objects. This fix releases the Session objects to avoid
    memory leak.
    
    Change-Id: Icca7100bded0653a4ec7f2b4bd48a29262432a3b

commit 2b95c5d63ea0be791906c7bc4c3befd644160d18
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 01:03:02 2015 -0700

    move sound and display from main settings to cmremix settings
    
    move viper4android from tweak to sound settings
    
    Change-Id: I15f1d58bd5a8498f788cdd3014ccd3940f28a5e1

commit 944a026dd45e3997a652e0020a4506e8d2394f15
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 17:35:12 2015 -0700

    [2/2] settings: add CPU info overlay
    
    this shows
    CPU temp (if available)
    for every core governor + online + freq
    
    Change-Id: I28c1e48c2e613b33c301b61cead70678ab6a2e9b
    
    Conflicts:
    	res/values/cmr_strings.xml
    	src/com/android/settings/DevelopmentSettings.java

commit 45a7c06f188efe8cec9bbdac2d43b04a4f39cad5
Author: yank555-lu <yank555.lu@gmail.com>
Date:   Sun Jan 11 21:30:30 2015 +0100

    DeviceInfo: remove unused variable in getMemInfo()
    
    Change-Id: Ic4275d7f5168383d051ca499d0dd8a83ab26b3b0
    Signed-off-by: yank555-lu <yank555.lu@gmail.com>
    
    (cherry picked from commit 61d9d5d53c664f293470ea439f3337297f91e9a9)
    
    (cherry picked from commit 61d9d5d53c664f293470ea439f3337297f91e9a9)

commit 2a5074ef61ab1b885f530fc0c42d847da0a6aa92
Author: yank555-lu <yank555.lu@gmail.com>
Date:   Sun Jan 11 21:29:44 2015 +0100

    DeviceInfo: correctly grab the processor info from /proc/cpuinfo
    
    Change-Id: I1eb299ed97589e094c8306fa807cc8b7facf448c
    Signed-off-by: yank555-lu <yank555.lu@gmail.com>
    
    Conflicts:
    	src/com/android/settings/DeviceInfoSettings.java
    
    (cherry picked from commit ac590a86ec2070875a9ea56ca7e82f75b1029228)
    
    (cherry picked from commit ac590a86ec2070875a9ea56ca7e82f75b1029228)

commit 45ca1c0c99ec02cee91f6a0ba267479c03cb9464
Author: Somber73 <nytesblood@gmail.com>
Date:   Mon Jan 26 03:52:45 2015 -0700

    Added SaberMod Android banner in About Phone
    
    Change-Id: Id23a1ac74b4a5eac0d2f57479780eb2d0e97de68
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	res/xml/device_info_settings.xml
    
    Conflicts:
    	res/xml/device_info_settings.xml
    
    (cherry picked from commit 5098b45bf70b113aa6fa85b3d5d57b346bf5bd15)
    
    Conflicts:
    	res/xml/device_info_settings.xml

commit 4b04fdb8aaab30952b04abf55578db80eae75569
Author: maxwen <max.weninger@gmail.com>
Date:   Mon Apr 6 01:59:17 2015 -0700

    settings: Add PerformanceControl [1/2]
    
    Change-Id: I06b0815208041dd00f34ce01ca6b468cf54d26dd
    (cherry picked from commit ab15edf99742bad8ddd2384534941fcaf6088b60)
    
    Conflicts:
    	res/values/pac_strings.xml
    
    Conflicts:
    	Android.mk

commit 847af6919e890ef77d1ce1e7ee64edad1c96b622
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Dec 23 13:21:03 2014 -0700

     Add back Utils we had in kitkat
    
    Don't know original authors
    
    (cherry picked from commit e511c619645af41414a6d8660ceb2f7d9f8a1d9f)
    
    (cherry picked from commit 01cb2f3ef713ccf882970d2703f20134eda93521)
    
    Change-Id: I17cbd388430b1cd2d93c2faa6c7c84f4f6e8584a

commit 048d897f0754f3891906732e12c24dc292b18235
Author: Zion-Tran <ziontran@outlook.com>
Date:   Mon Dec 29 16:34:54 2014 -0700

    add slim SeekBar
    
    (cherry picked from commit 7276cd0a4f7ec452d62dde56d819fd0e62bfd02f)
    
    (cherry picked from commit a4e39ce85fa02a1f5a54a50b67de0d7f0d994340)
    
    Change-Id: I80c00760e9e7427e4ccd6093c2e6fee9bdb40744

commit 046d54a2db3514de66c47297b759ad1d8b686712
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 17:44:35 2015 -0700

    fixed device type to screentype
    
    Change-Id: I9877d5b50f7009f9962f7528db3de907f79826dd

commit e50b859fe26f04e968fe5b3dc6906a7658e0ae00
Author: Der-Schubi <schubi@erlangen.ccc.de>
Date:   Mon Apr 6 17:47:31 2015 -0700

    Add option to Restart SystemUI to DevSettings
    
    Change-Id: I1dd55510a878198f245ff90c011717ac5fb65f93
    
    Conflicts:
    	res/xml/development_prefs.xml
    	src/com/android/settings/DevelopmentSettings.java
    
    Conflicts:
    	src/com/android/settings/DevelopmentSettings.java

commit 89b456c139ce8d9dc0a46774d947bf94e6f4824b
Author: Evisceration <eviscerationls@gmail.com>
Date:   Fri Jun 20 18:37:55 2014 +0200

    Settings: do not crash if development app is not installed
    
    Change-Id: If136b509e8727399b1dcfa42ce5b4043612f868f

commit 1a8621194d60af2ee269c0fa59273d4e175aa4cb
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 17:52:26 2015 -0700

    Remove taps to become a developer
    
    Developer settings are enabled by default, so having this "feature"
    in the Settings app is pointless and annoying. Remove it to improve
    the UX.
    
    Change-Id: I010e798f40273a6c4b8f44983d5ebb0657039c87

commit b602703c5b5639260809da92b194b4fd288c5ba2
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 17:53:09 2015 -0700

    Display: Avoid another ArrayIndexOutOfBoundsException and catch if necessary
    
    credit @temasek
    
    Log provided by andreasltcf of xda
    
    FATAL EXCEPTION: main
    Process: com.android.settings, PID: 7139
    java.lang.RuntimeException: Unable to start activity ComponentInfo{com.android.settings/com.android.settings.SubSettings}: java.lang.ArrayIndexOutOfBoundsException: length=7; index=7
    at android.app.ActivityThread.performLaunchActivity(A ctivityThread.java:2298)
    at android.app.ActivityThread.handleLaunchActivity(Ac tivityThread.java:2360)
    at android.app.ActivityThread.access$800(ActivityThre ad.java:144)
    at android.app.ActivityThread$H.handleMessage(Activit yThread.java:1278)
    at android.os.Handler.dispatchMessage(Handler.java:10 2)
    at android.os.Looper.loop(Looper.java:135)
    at android.app.ActivityThread.main(ActivityThread.jav a:5223)
    at java.lang.reflect.Method.invoke(Native Method)
    at java.lang.reflect.Method.invoke(Method.java:372)
    at com.android.internal.os.ZygoteInit$MethodAndArgsCa ller.run(ZygoteInit.java:898)
    at com.android.internal.os.ZygoteInit.main(ZygoteInit .java:693)
    Caused by: java.lang.ArrayIndexOutOfBoundsException: length=7; index=7
    at com.android.settings.DisplaySettings.updateTimeout PreferenceDescription(DisplaySettings.java:344)
    at com.android.settings.DisplaySettings.onCreate(Disp laySettings.java:167)
    at android.app.Fragment.performCreate(Fragment.java:2 031)
    at android.app.FragmentManagerImpl.moveToState(Fragme ntManager.java:863)
    at android.app.FragmentManagerImpl.moveToState(Fragme ntManager.java:1067)
    at android.app.BackStackRecord.run(BackStackRecord.ja va:833)
    at android.app.FragmentManagerImpl.execPendingActions (FragmentManager.java:1452)
    at android.app.FragmentManagerImpl.executePendingTran sactions(FragmentManager.java:483)
    at com.android.settings.SettingsActivity.switchToFrag ment(SettingsActivity.java:955)
    at com.android.settings.SettingsActivity.onCreate(Set tingsActivity.java:581)
    at android.app.Activity.performCreate(Activity.java:5 933)
    at android.app.Instrumentation.callActivityOnCreate(I nstrumentation.java:1105)
    at android.app.ActivityThread.performLaunchActivity(A ctivityThread.java:2251)
    ... 10 more
    
    Change-Id: I53fb599b43e8db82ae844e828bc8351e0117c0d1

commit b73c2c64b7db7580d5fecc9fd4e761701fbbf0db
Author: Zion-Tran <ziontran@outlook.com>
Date:   Thu Dec 25 15:40:46 2014 -0700

    Settings: Enable Advanced Reboot by default [1/2]
    
    (cherry picked from commit e20794cd3a99280da0f6eb0d6e7aac74eae0a679)
    
    Change-Id: Ia9bd71edcb6849ee93c4acfdf6a9026bc9f4a322

commit ca13d9440550bce9c2f593512ec67904701dc78a
Author: Tom Marshall <tdm.code@gmail.com>
Date:   Mon Apr 6 18:52:24 2015 -0700

    Add LCD density setting
    
    (cherry picked from commit 6c87122f95e90d072edda9c114395bfbe0b5bce2)
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/cmremix_custom_settings.xml
    
    Change-Id: I186dfc28c359edee8b3cb28c3df617a75bcb17c1

commit dfccf4a848f301c5848346709ef1d0671659a8c7
Author: LorDClockaN <davor@losinj.com>
Date:   Wed Jan 21 02:53:55 2015 -0700

    Add custom option for DPI selection
    
    PS2: only numbers for EditText
    
    Change-Id: I1af75f276ea4691acd06cb3ed2089d3d828e390c

commit 638fa4006c6ad116d4ed2657c693e0379446601d
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Mon Apr 6 18:55:34 2015 -0700

    [LCD density] be nice and show a dialog for user confirmation
    
    - little hardcoded for sure
    
    Conflicts:
    	res/values/cr_strings.xml
    	src/com/android/settings/temasek/DisplaySettings.java
    
    (cherry picked from commit dd07a693e7d8aff43dceb1ab2b368cb9b8cddd91)
    
    Conflicts:
    	res/values/cmr_strings.xml
    	src/com/android/settings/cmremix/DisplaySettings.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Change-Id: I194f047b871dafc20ad9d35c9f829036ab40d0a9

commit fb0eb16333379b545091cf7dfa9594d2e3ed63e6
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 19:13:43 2015 -0700

    Settings: add safe headset volume and less annoying sound notification
    
    Add settings for both features.
    
    Change-Id: I8ab4f4b9ec320238b05ac51fb76ac24b93c37d37
    (cherry picked from commit 5d8d5cfaec835f7a4168131c1a508aa71bd788dd)
    
    Conflicts:
    	res/values/cm_plurals.xml
    	res/values/slim_strings.xml
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/xml/sounds.xml

commit 6357860862d5ee2071cba15d41c40ba1f481cb94
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Nov 20 21:29:20 2014 -0700

    Option to use volume keys to control media volume anytime [2/2]
    
    The volume keys control the Media volume rather than the Ringer
    hence removing the issue of accidentaly changing the Ringer volume.
    
    Credits: Pawitp
    
    Change-Id: Ic0a1c04ae41eac65e9535d6de5f11c0456730315
    
    Conflicts:
    	res/values/cr_strings.xml
    
    (cherry picked from commit 82e813263298ab084a1f428489b3ea2fcd5a23b9)

commit bd133c1502d136aba2bc3c0fba4915e8e0cb7951
Author: Muhammed Nazim <mnm9994u@gmail.com>
Date:   Mon Apr 6 19:15:51 2015 -0700

    Forward Port: Add Camera sound toggle [2/3]
    
    Change-Id: I3ed04229c51d578b874328297eac5e9e255f51f0
    
    Conflicts:
    	res/values/slim_strings.xml
    
    (cherry picked from commit d272e083fae88c0b3f1dd1b140d13bce2922f771)
    
    (cherry picked from commit 4e436e76a48bb2a28b29f2d929558f85932dbe2f)
    
    (cherry picked from commit fd6f29d417a5fb7aa3313951b652f4734d055497)
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 868c2f77d1f3c0d35e1f399d8727bec7f0f55ddb
Author: Roman Birg <romanbirg@gmail.com>
Date:   Mon Nov 10 08:29:31 2014 -0500

    Enable Developer options by default
    
    Change-Id: I2cfc1b2d0e918f5df3ee6b794084caf67b44de41
    
    (cherry picked from commit 0bd1d50209a4639b76fbde6d60638dabc2a6c653)

commit d24e1ca0267a952ecc1d59a5aa12ff38b2d4210a
Author: Adam77Root <adam77root@gmail.com>
Date:   Sat Sep 6 18:13:18 2014 +0200

    Open app when clicking on icon in App Info screen
    
    Based on Xposed module Shortcut in App Info:
    http://repo.xposed.info/module/com.mohammadag.shortcutinappinfo
    
    There is no vibration as in the module as I didn't find it necessary
    
    Change-Id: I07b3f947aaaa13702adba3b4e78bb780fe861baf
    
    (cherry picked from commit f0faadcc85a02bca06d5872655e46940770c4d75)

commit 734c5f09e1e451497d1546bac9372b9887f33dce
Author: Tom Hite <tdhite@gmail.com>
Date:   Mon Apr 6 19:42:42 2015 -0700

    volume steps: lollipop implementation [2/2]
    
    credit to Pac team
    
    This amounts to a complete rewrite of the volume steps Settings
    app implementation. Settings is entirely different from the same
    in KitKat, thus the ultimate need for a rewrite.
    
    Still, the original author, Meticulus <theonejohnnyd@gmail.com>,
    deserves credit for the original volume steps feature. See:
    http://review.pac-rom.com/#/c/467 for the kitkat commit.
    
    PS2: just fixing the commit message to match the other in the set.
    PS3: Move to PAC settings
    PS4: Never mind
    PS5: Rebase
    PS6: Move to PAC Settings table
    PS7: Add a preference category
    PS8: Remove unnecessary commented code.
    
    Change-Id: I03f72867de579c7fb8f2932627f89ea2e94c1613
    
    Conflicts:
    	res/values/pac_strings.xml

commit 3c348939cbc3b68461421d25d46ce643fe478532
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Nov 24 08:56:27 2014 -0700

    Lockscreen: Add timeout and instant lock option to slide lock (1/2)
    
    This adds AOSP's new timeout and instant lock options to the
    slide (aka chooser) style lockscreen.
    To Do: Add the vibrate option as well.
    
    AICPfy:
    brought from kitkat
    PS2: CheckBox -> Switch
    
    Change-Id: Ide8e8d14603e5111debcc7a7cf6c4b74898bfa3d

commit f6c347de413d339d2fbf9dde0ddb71fa8bb06748
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 19:49:35 2015 -0700

    Settings: Option to enable/disable scrolling cache @temasek
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    	res/xml/development_prefs.xml
    
    Change-Id: Idd353094e7ab922a25f95dc898912ce360944ef8

commit bf77eb4e4200519051cf4ca91fc192f92ae67b16
Author: Allan Hedelain <tristan202@gmail.com>
Date:   Mon Apr 6 19:55:22 2015 -0700

    Settings: add back status bar date & style options (2/2)
    
    * Date style
    * Date format
    
    * 0 - Regular style
    * 1 - Lowercase
    * 2 - Uppercase
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java

commit cd4fdac1ec697a72aff1bc1c25c48fc42c3947af
Author: 0xD34D <clark@scheffsblend.com>
Date:   Mon Apr 6 20:04:42 2015 -0700

    [2/2] Screen recorder by 0xD34D
    
    http://forum.xda-developers.com/showthread.php?t=2547196
    Thanks to OmniROM for the icon!
    
    Change-Id: I0f2300128f88218d36f3423c4959fa4ef6d83605
    
    Conflicts:
    	res/values/slim_strings.xml
    
    (cherry picked from commit bcb61252c38070cccd826fbd45e6987e8d473767)
    
    Conflicts:
    	res/xml/screen_and_animations.xml
    
    (cherry picked from commit 5f9004c138218a7a0fe6633ea4711c56e87a5609)
    (cherry picked from commit fe573a5f8661bffddb3a450baf2061016e451655)
    (cherry picked from commit d4a6e4706d6a4071dc4fbc37edb2c71920055ee9)
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/cmremix_interface_settings.xml

commit b96ffd5f6ac36930c189d64c43e8a6bb9a48d81d
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Mon Apr 6 20:18:01 2015 -0700

     [2/2] Settings: Configurable overflow menu button
    
    Forward port from SlimBean. It was part of the hardware key custom rebinding.
    
    (cherry picked from commit 10e658f258a07f8aa2961c2eca266f08b7ff47e4)
    
    Conflicts:
    	res/values/cmr_strings.xml
    	src/com/android/settings/ButtonSettings.java

commit 43b17fbf651f233fb6864b08ba42f6cc9d274a18
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Apr 6 22:25:47 2015 -0700

    Settings: Disable Quick Settings on secure Lockscreen (2/2)
    
    credit to Pac Team
    
    We have a lot security guys as user due of using the phones as business phones...that
    said a lot complains go into the direction of google how it is possible to have
    access to quick settings on a secure lockscreen which is absolutely understandable
    due that you are able to control Wifi BT AirplaneMode data etc.
    
    This patch takes care on this problem and adds an option to control this behaviour.
    
    ATTENTION: Due that this is really an UX derp for an average user this feature is
    enabled by default now. User need to disable it explicit in settings to get on secure
    locksreen the original android behaviour back.
    
    PS2:
    - fix derp
    
    Change-Id: Iea5311cdeb793a605fffe87abab72f323e755dca
    
    Conflicts:
    	res/values/pac_strings.xml
    	src/com/android/settings/cyanogenmod/NotificationDrawerSettings.java

commit e7ce64d1d00d1bfe61c846a1897bbf96d9777616
Author: Johnnyslt <ionut.darescu@gmail.com>
Date:   Mon Apr 6 20:33:27 2015 -0700

    Settings: AdBlocker [2/3]
    
    Change-Id: I4b5a2aca90665ef018e35a9abface1f01fbb75a2
    
    @alviteri: Liquid --> crDroid ---> cmRemiX
    
    (cherry picked from commit c002664d8de031fdb9d499bf93cfe87e1ff7c5e5)
    
    Conflicts:
    	res/xml/crdroid_custom_settings.xml
    
    Conflicts:
    	AndroidManifest.xml
    	res/xml/cmremix_custom_settings.xml

commit 86f8dac62af58f6fbeba0a10b4b45986ae101655
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 6 20:36:27 2015 -0700

    HFM: Add whitelist to HFM
    * also fix not being able to switch off the ad disabler
    
    AICPfy
    CheckBox to Switch
    Move settings to main Extras menu
    
    Change-Id: Ifa8adf2313f0c0932882c3ac6cd4bda7e8b250de

commit e2ecade252baf73d518b37a2ddc6e3788bf4e251
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 7 01:45:43 2015 -0700

    Revert: Display: Avoid another ArrayIndexOutOfBoundsException and catch if necessary
    
    credit @temasek
    
    Log provided by andreasltcf of xda
    
    FATAL EXCEPTION: main
    Process: com.android.settings, PID: 7139
    java.lang.RuntimeException: Unable to start activity ComponentInfo{com.android.settings/com.android.settings.SubSettings}: java.lang.ArrayIndexOutOfBoundsException: length=7; index=7
    at android.app.ActivityThread.performLaunchActivity(A ctivityThread.java:2298)
    at android.app.ActivityThread.handleLaunchActivity(Ac tivityThread.java:2360)
    at android.app.ActivityThread.access$800(ActivityThre ad.java:144)
    at android.app.ActivityThread$H.handleMessage(Activit yThread.java:1278)
    at android.os.Handler.dispatchMessage(Handler.java:10 2)
    at android.os.Looper.loop(Looper.java:135)
    at android.app.ActivityThread.main(ActivityThread.jav a:5223)
    at java.lang.reflect.Method.invoke(Native Method)
    at java.lang.reflect.Method.invoke(Method.java:372)
    at com.android.internal.os.ZygoteInit$MethodAndArgsCa ller.run(ZygoteInit.java:898)
    at com.android.internal.os.ZygoteInit.main(ZygoteInit .java:693)
    Caused by: java.lang.ArrayIndexOutOfBoundsException: length=7; index=7
    at com.android.settings.DisplaySettings.updateTimeout PreferenceDescription(DisplaySettings.java:344)
    at com.android.settings.DisplaySettings.onCreate(Disp laySettings.java:167)
    at android.app.Fragment.performCreate(Fragment.java:2 031)
    at android.app.FragmentManagerImpl.moveToState(Fragme ntManager.java:863)
    at android.app.FragmentManagerImpl.moveToState(Fragme ntManager.java:1067)
    at android.app.BackStackRecord.run(BackStackRecord.ja va:833)
    at android.app.FragmentManagerImpl.execPendingActions (FragmentManager.java:1452)
    at android.app.FragmentManagerImpl.executePendingTran sactions(FragmentManager.java:483)
    at com.android.settings.SettingsActivity.switchToFrag ment(SettingsActivity.java:955)
    at com.android.settings.SettingsActivity.onCreate(Set tingsActivity.java:581)
    at android.app.Activity.performCreate(Activity.java:5 933)
    at android.app.Instrumentation.callActivityOnCreate(I nstrumentation.java:1105)
    at android.app.ActivityThread.performLaunchActivity(A ctivityThread.java:2251)
    ... 10 more
    
    Change-Id: I53fb599b43e8db82ae844e828bc8351e0117c0d1 (reverted from commit b602703c5b5639260809da92b194b4fd288c5ba2)

commit 0684787ca8b81d8ddbad995d682bde46cd252900
Author: Dragon <dragon7780@hotmail.nl>
Date:   Sun Jan 25 22:52:50 2015 +0100

    Allow disabling of FC dialogs [2/2]
    
    Change-Id: I66d022c815c2af8b85f78c7be76edf9a16e1abe1
    Signed-off-by: Dragon <dragon7780@hotmail.nl>
    
    (cherry picked from commit 078102b1997f8e0895094bef0f48b0fe4cc967ef)
    
    (cherry picked from commit 078102b1997f8e0895094bef0f48b0fe4cc967ef)

commit 5f107e2c2779a3b80774a51c470b6cef16181b6d
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 7 14:44:07 2015 -0700

    Privacy guard: option to disable notification (2/2)
    
    (cherry picked from commit b383d085d7cf2f17ae6211f1f74fa3c3875783b7)
    
    (cherry picked from commit b383d085d7cf2f17ae6211f1f74fa3c3875783b7)
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 1043d3ba8814e8976f873bb98bb805c4f17fa3e3
Author: Gianmarco Reverberi <gianmarco.reverberi@gmail.com>
Date:   Tue Jan 20 19:09:01 2015 +0100

    Wifi: add option to show quick settings detail view (2/2)
    
    Added a switch preference in notification drawer settings
    to enable detail view for Wi-Fi tile
    
    Change-Id: Ibbc5d5c1ca9e98988bdf6375c18c96866cb7d158
    
    Patchset: 4
    http://review.cyanogenmod.org/#/c/86325/

commit e5f1663361368a79b07f15fd06fe43c78ccad649
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 14:46:32 2015 -0700

    Quick Settings: Auto collapse panel (2/2)
    
    Signed-off-by: Altaf-Mahdi <altaf.mahdi@gmail.com>
    
    Change-Id: I7052a2df7e92d2828769d5a8d3230ba47b11faa9
    
    Conflicts:
    	res/values/cr_strings.xml
    	res/xml/notification_drawer_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit e635766134ef6a87663d9310fc2ae9ffe9f2bab0
Author: Evisceration <eviscerationls@gmail.com>
Date:   Mon Dec 29 07:01:54 2014 +0000

    [2/2] Settings: Add Haptic Feedback to quicktiles
    
    Change-Id: I792a00a2689a572110963db00362f8e9d77b3fkjdudu
    
    Conflicts:
    	res/xml/status_bar_settings.xml

commit 54ef3d3b1d4cf9c2abd97f93de0e867282500db4
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Sat Jan 17 21:55:16 2015 +0000

    QS: Squashed from EuphoriaOS (2/2)
    
    Change-Id: If9378713650e7ad74d647c36f788771559ed596c
    
    Conflicts:
    	AndroidManifest.xml
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java

commit 5347b85a713989eb1058b9192404452476656d30
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Feb 1 07:23:50 2015 +0000

    QS: add Screenshot & Sync tile (2/2)
    
    Change-Id: Ieb3eddd45be2a8c6c4bf19b5931c40998794324d
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit d53cb624ea89b18219ea974c3d4b4ab37c1339f0
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 19:59:31 2015 -0700

    QS: Option to show four tiles per row (2/2)
    
    This also changes tile picker grid to 4 tiles per row
    
    Change-Id: I8b876da5a8d8a0b635d90f330e18bc70b2238844
    
    Conflicts:
    	res/xml/notification_drawer_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/notification_drawer_settings.xml

commit 7ffac212cb973daf5a268bdc43c91409b8ecd306
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 7 14:55:43 2015 -0700

    QS: add newly added tiles
    
    * Battery saver
    * Brightness
    * Expanded desktop
    * Screen off
    
    * also add notifications tile
    
    Change-Id: I64956333bd22d26db6ce72a6149b496d4542bfec
    
    Conflicts:
    	res/values/custom_strings.xml
    	src/com/android/settings/SettingsActivity.java
    
    Conflicts:
    	src/com/android/settings/Settings.java
    
    Conflicts:
    	res/values/cm_strings.xml

commit 083e26a9fda897e7dcab6535b55277b9ed85731e
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Sat Feb 21 22:52:31 2015 +0100

    QSTile: Reboot/Recovery tile (2/2)
    
    Change-Id: I4b49f915ee8829102489578a75369c48c99fceaf

commit 29b9ee28cba50584d8e2744836479491135d13d9
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 7 15:21:25 2015 -0700

    settings : fixed display_and_lights_settings
    
    Change-Id: Ic186f6a3823891fec062292c6cf735f56f61ef8c

commit 5e8829d46bc5cb40a353b7d55e4faf88b79246a1
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 7 16:00:16 2015 -0700

    Quick settings customizations, (2/2): (useername)
    
    - Custom background color
    - Custom icon color
    - Custom text color,
      (this won`t change any text which is using the accent color)
    
    AICPfy
    PS2: fix build
    PS3: swag
    PS4: more swag
    PS5: proper stock bg
    
    Change-Id: Ib6f8836b778fc5ec1584b5ef1b352c0f48892497
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 4e7f4f13c600e8a8672caf7a2a7b8b2c78e57f5b
Author: LorDClockaN <davor@losinj.com>
Date:   Sun Mar 1 10:42:15 2015 +0100

    QSColor: Improvements - transparent shade (2/2)
    
    PS2: string edit
    
    Change-Id: I55ae691baea8b4f28fbf6be37b07c95ab4582041

commit 7d8876a05c5f05dec39527e84dc0f8e979d16abc
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Mar 3 20:26:19 2015 +0100

    Settings: QS colors master switch (2/2)
    
    Change-Id: I1b8624c823ec1a1016a01c4b47482c68c9499e01

commit 946326d01a8b4d6dcca7f90c33f10c02e3a9e385
Author: LorDClockaN <davor@losinj.com>
Date:   Sat Mar 7 17:06:00 2015 +0100

    QSColors: No more SystemUI restart on switch
    
    Change-Id: I532a50927cf81d8720069c51d8a32429f9ca2729

commit 29230fe1c7dc1311db7722df88561279a07ff252
Author: Janson Kang <temasek71@gmail.com>
Date:   Fri Nov 28 10:58:28 2014 +0800

    Add settings reset icons
    
    Change-Id: I4b4e6ea7cf4825ffc2dce8af1a5b4003501ad083

commit 1b87b65cbd79ba8f82c5a6d3ac3a85bc16d70baf
Author: Joey Rizzoli <io.nolinuxnoparty@gmail.com>
Date:   Tue Apr 7 21:34:52 2015 -0700

    Settings: HeadsUp options [2/2]
    
    Includes:
    
    * Settings: forward port HeadsUp options [2/2]
    
    -Global on/off
    -Blacklist and Do not disturb
    
    (by Adnan Begovic)
    
    * HeadsUp settings: fix enabled state on clean install
    
    (by Altaf Patel)
    
    * My changes
    
    - Swype action selector (delete/hide)
    
    Change-Id: Ia2ecc52034f04b11590abd62c5119f736985450a
    
    Modified to temasek
    
    Conflicts:
    	res/xml/temasek_settings.xml
    	src/com/android/settings/temasek/TemasekSettings.java
    
    Conflicts:
    	AndroidManifest.xml
    	res/values/cmr_strings.xml
    	res/xml/cmremix_custom_settings.xml
    	src/com/android/settings/cmremix/CustomSettings.java

commit 085e783fa4508cb62fe817425bd8b3f6acee5bd7
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 7 21:35:56 2015 -0700

    HeadsUp: add timeout option (2/2)
    
    Conflicts:
    	res/values/cmr_arrays.xml
    
    Conflicts:
    	res/values/cmr_arrays.xml
    
    Change-Id: I1d90f9f344a17e4ace64a078e46536353cf7bb1d

commit 5812f69bf31fb30a93d7b67b811bbbadd5567632
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Mon Feb 9 14:45:42 2015 -0700

    [Heads up Swipe] A more user friendly summary
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Change-Id: I4c94a51f2a41aad55663d141b8464dde0971a65d

commit c4fb52e4aee048cdd06da89179c40eecf0869ae2
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Fri Feb 6 08:02:07 2015 -0200

    [Heads up] Touch to hide (2/2)
    
    - Also clean up swipe behavior and fix summary
    
    Change-Id: Ibd0be064deb9e357740dc38e767a8024a78a550e

commit 75108fb8e8a8b40900db3366395d7425f9510099
Author: Janson Kang <temasek71@gmail.com>
Date:   Thu Feb 12 17:32:58 2015 +0800

    Heads Up: Clean up code after ScreenType FWB commit
    
    Change-Id: I6835014cbd1fdf8a78f6e6f8ee9561bcc7866aee

commit 8b5a89099fa414948c61571209a984b623fda7bb
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Tue Apr 7 23:42:43 2015 -0700

    [Settings] Add the ability to hide superuser status bar icon
    
    - Add a simple option to hide the su icon placed in status bar when a session is active
    
    coded by @cristianomatos
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml
    
    Change-Id: I859b0f72e59705c51faad4c85a8cd7bd9ae40c84

commit 14bef8370fe6478997d23979d583de0ff7c32c66
Author: lichti1901 <lichti190185@gmail.com>
Date:   Tue Apr 7 23:47:35 2015 -0700

    Navigation bar button color (2/2)
    
    Modified to temasek
    
    Conflicts:
    	res/values/cr_strings.xml
    	src/com/android/settings/ButtonSettings.java
    
    Conflicts:
    	src/com/android/settings/ButtonSettings.java
    
    Change-Id: I41bb7e9e7c50901e8059cee79e0c9f698b80102a

commit 32207e927ab1d49d685c2b5ef1196facb13c4951
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Mon Nov 17 03:37:33 2014 +0100

    Settings: Tint Black drawables
    
    Change-Id: I8fd49b6ad89036edbb5b7a0679b0ecddf5cd66dc
    
    @alviteri: this commit was made for material black but we won't use it so only copy the tint drawables and paste to our settings repos

commit bc4843bec43eaae61c61a0fb65c6277589f86e8d
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Dec 4 00:17:01 2014 +0100

    Settings: tint ic_drawer image
    
    Change-Id: Ibe1dbb6ae64f166311fc73824d34cb3abd6bb350

commit 26f8f6f0bb814ea18e221cd5d656738cec74b6af
Author: david <davidteri91@gmail.com>
Date:   Wed Jan 28 19:17:44 2015 +0100

    Settings: add more drawables to Slim LockScreen Shortcuts (1/2)
    
    Chrome
    Github
    Paypal
    Youtube
    Whatsapp
    Messenger
    Office Suite
    Tapatalk
    
    Change-Id: I2e9e73e4ffc13e51303f9f00257892e8a1443037

commit 54cc19142657980df89cf9c0767a91fdcb30cf43
Author: jukiewalsh <xxxwilsonxx@gmail.com>
Date:   Thu Jan 29 00:37:44 2015 -0500

    Settings: add snapchat lockscreen icons [1/2]
    
    Change-Id: I3ef41e9c11e7e6c2ca3dc7e0d3c1e17859586356

commit 203fbd9a6c014a8770c1eec108cbd66915991249
Author: lirokoa <lirokoa@hotmail.com>
Date:   Sat Apr 4 12:13:28 2015 +0200

    SoundSettings: Fix NPE in sound settings
    
    Fix a NullPointerException when there is no telephony on the device.
    
    Change-Id: I66994f8f18c2a560b0c370514f61fc45894c9f8b

commit 1c5916ae32855a08da4d7783ba299d903f5355b8
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 2 12:56:56 2015 -0700

    Settings: improve empty Profile trigger icons
    
    The icons that were used were being scaled up and looked choppy and
    ugly. Use some vector drawables instead.
    
    Signed-off-by: Roman Birg <roman@cyngn.com>
    (cherry picked from commit abd4d4aa7dac8f0b3241aea4d3c48c4a54dd03ba)
    
    Change-Id: Ia66d79f706f5de5b835fdcc503f1e92944e8b7dd

commit 16c112170e1476630bc30621557906105dda1006
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Wed Apr 8 02:21:42 2015 -0700

    Settings: Ambient Display configurations
    
    AICPfy
    Move all to system settings
    Add SystemSettingsCheckBoxPreference that we had in kk
    PS2: Added Time category and played with strings
    
    Change-Id: Ib85c25d50dc924d4f07658dac033e6581184317d
    Signed-off-by: scott <scott@beanstalk.com>
    
    Conflicts:
    	res/values/bs_strings.xml
    	res/xml/display_settings.xml
    	src/com/android/settings/search/SearchIndexableResources.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/display_settings.xml
    	src/com/android/settings/DisplaySettings.java
    
    Conflicts:
    	res/xml/display_settings.xml
    	src/com/android/settings/DisplaySettings.java

commit 5ca78fee5d931711ce422d3bf3232a414e6b5c8c
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Feb 17 16:02:39 2015 +0100

    Update Ambient to PS23
    
    Change-Id: I1268e75ff3b84cdaacfee93634973837c6c6a1ab

commit b169f9b4f2f46e07804677baa89d105f5baccc25
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Wed Feb 18 15:05:19 2015 +0100

    Update Ambient to PS29
    
    Change-Id: Ia1080b736b89ac02e817d34c93da1a63e5049863

commit dd52e38d32ac2449d774093addbeedab21a860d3
Author: LorDClockaN <davor@losinj.com>
Date:   Wed Feb 18 15:25:31 2015 +0100

    Fix build aftger ambient patch update
    
    Change-Id: Id53ec1d6cffb2278b39a14240e0cf6dbdff051c0

commit 51bc07f8e1683740e3f09c1bfed25167c3425f9c
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Thu Feb 26 21:56:29 2015 -0700

    Settings: use switch preference for Ambient Display
    
    Change-Id: I2dc12b83ac24ac7a120d2a8808c17b2425c118ef

commit 7bd6811cfa11ff394390eb62bc5e8f3cf58665f8
Author: Janson Kang <temasek71@gmail.com>
Date:   Wed Feb 18 15:47:43 2015 +0800

    USB Settings: Use SwitchPreference
    
    Change-Id: I2a93b9d1f0939f2d11bf336c939e924e1ccdae07

commit e164538c907c39e4f15042153c85afff7320556d
Author: david <davidteri91@gmail.com>
Date:   Tue Jan 13 16:26:21 2015 +0100

    Settings: CM Power Menu: Remove BugReport
    
    Change-Id: I7d6f5b1c18dd5f689f4d1f13019af8ed600d5785

commit d807ed034789303d104e4e0112603c8cdbcabe01
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 14:28:24 2015 -0700

    PowerMenu: Use SwitchPreference
    
    Change-Id: Ia1c6962fc94f09d2764d2cfd66d0b4991ac9d5d2

commit 404203973d6a7bcbce352f34f26faa14d15a4e19
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 14:25:56 2015 -0700

    complete CMRemix Settings dependencies
    
    Change-Id: I068a530fb1d0a29b9c9390bca0f0c0ad9d71f368

commit 759b0316466ed72d43ea5214574d6795a8d92dbc
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 20:29:42 2015 -0700

    house keeping: move recent panel to tweaks
    
    Change-Id: Ibe238cf6ed0b5391820252f6961408b14aa0fe6f

commit bd99762333c19f0e79085eeec80d0d212383cb98
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 8 18:53:26 2015 -0700

    update navigationbar
    
    Change-Id: Ice03a83b0b64854ba261be8d8820a7d3627da3b3

commit 29cf1585ec8dfa27ab05392c7b6cb45adc01db2d
Author: Evisceration <eviscerationls@gmail.com>
Date:   Wed Apr 8 19:05:59 2015 -0700

    Add toggle for captive portal check
    
    In order to detect working data, the portal check connects to
    google servers.
    But in some countries, for example china, google servers are
    blocked and the check was never successful.
    
    This change adds a toggle for users, who are in a restricted
    network which blocks "clients3.google.com" and allows them
    to use their network as usual
    
    Change-Id: I2cb75a3234c1df894c238ed6b5e37495434a417f
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    (cherry picked from commit d8c1cbf200eab5eb3d9e002e59c1cfb59c83ec0f)
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 8e73fe8e731e32c377d52d349e2ad3c99a6bf5d8
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Apr 8 19:11:32 2015 -0700

    Settings: option to disable search panel (navrings) (2/2)
    Change-Id: I573fd6fab4c24866f58b4062c5eb516719c0855b
    
    Modified to temasek
    
    Conflicts:
    	res/xml/button_settings.xml
    
    Conflicts:
    	res/xml/button_settings.xml

commit 85472daf84fa37c0d5947389d52d19f781ad658c
Author: STELIX <ssspinni@gmail.com>
Date:   Wed Apr 8 19:14:59 2015 -0700

    Settings - Add PowerMenu QS Tile (Reboot on longpress) [2/2]
    
    PS2: delete unneeded drawables
         string edit
    
    Change-Id: I5c60a23f85df9d6f9e264ffba970ea8a49af5cbd
    Signed-off-by: STELIX <ssspinni@gmail.com>
    
    Conflicts:
    	res/values/cm_strings.xml
    
    Conflicts:
    	res/values/cm_strings.xml

commit b6aaf2266a5e36309c72297e95ff007975f54031
Author: scott <scott@beanstalk.com>
Date:   Thu Feb 12 20:59:43 2015 -0700

    Settings: Add Volume Key Answer (2/2)
    
    Change-Id: Icccdcd1f1947323cfbd7483604e7a4d2f8a58521
    Signed-off-by: scott <scott@beanstalk.com>
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/button_settings.xml
    	src/com/android/settings/ButtonSettings.java

commit a7e4dcacd75518063e08bd8bc39d6b7c071a78bf
Author: preludedrew <andrew.boren@gmail.com>
Date:   Wed Apr 8 19:18:17 2015 -0700

    Powermenu screenshot delay [2/2]
    
    AICPfy
    
    Change-Id: I34a2213a2d3333c05feaba02a9058a097aa561ee
    
    Conflicts:
    	res/xml/power_menu_settings.xml
    	src/com/android/settings/cyanogenmod/PowerMenuActions.java
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/PowerMenuActions.java

commit 50f00e7cd7c4e6fa3b1173d534d808b548741b01
Author: TheMrcool212 <munirmohamadrani@gmail.com>
Date:   Wed Apr 8 21:48:47 2015 -0700

    Double tap to sleep on navigation bar [2/2]
    
    Amend for temasek build
    
    Conflicts:
    	res/values/cr_strings.xml
    	res/xml/button_settings.xml
    
    Change-Id: I99cb836686ebe6b7851559c4bc173416e009d9ea
    
    Conflicts:
    	res/values/cmr_strings.xml

commit f9f2a76f3ada98557412775bdd85c195cc31472f
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Wed Apr 8 19:39:28 2015 -0700

    [Settings] Volume panel timeout
    
    Change-Id: I75576f2ed8c4bd4e4e18788a4c2f38692258326f
    Signed-off-by: Cristiano Matos <cristianomatos@gmail.com>
    
    Conflicts:
    	res/values/cr_strings.xml
    	res/xml/sounds.xml
    	src/com/android/settings/SoundSettings.java
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    	src/com/android/settings/SoundSettings.java
    
    Conflicts:
    	src/com/android/settings/SoundSettings.java

commit 05e7dd663fa62f26eb5182796131266163ff4997
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Thu Feb 19 10:33:00 2015 -0200

    Change expanded desktop options based on our navbar switch implementation
    
    We have navbar on/off switch to every device supported and with this we need to check if navigation buttons are visible or not and update expanded desktop option based on it
    
    Change-Id: I7357142c2536b5c0957e7fa1425f43b151e9eb99
    Signed-off-by: Cristiano Matos <cristianomatos@gmail.com>

commit 2b3509abe014d72e7774e89f5d2c427029036523
Author: UtkarshGupta <utkarsh.eminem@gmail.com>
Date:   Thu Apr 9 14:02:26 2015 -0700

    [3/4] Settings: Breathing missedcall/sms/voicemail
    
    Base: https://gerrit.omnirom.org/#/c/4976/
    Mms: https://gerrit.omnirom.org/#/c/4977/
    Telephony: https://gerrit.omnirom.org/#/c/4979/
    
    Change-Id: Ifcf39ec5d4dba543ab4416fc489399f760aea7d8
    
    @alviteri: Port by me to crDroid Android
    
    Conflicts:
    	res/values/custom_strings.xml
    	res/xml/bars_settings.xml
    	src/org/omnirom/omnigears/interfacesettings/BarsSettings.java
    
    Conflicts:
    	res/xml/status_bar_settings.xml

commit 3b9620b981854c1d685ae80917210bab115906fc
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Sun Feb 22 18:56:29 2015 -0700

    captive portal: remove extra whitespace
    
      * thanks to ghbhaha for pointing this out, i need more sleep
    
    Change-Id: I2cf34bbc2c15e7bf98a55456b5813f2e201d04c3
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    
    Conflicts:
    	res/xml/development_prefs.xml
    
    Conflicts:
    	res/xml/development_prefs.xml

commit 04cf4c143d9b26f5cd721878ee17641e442596a8
Author: snak3ater <saeedyasir91@gmail.com>
Date:   Tue Feb 24 00:02:43 2015 -0700

    Add Headsup tile [2/2]
    
    Change-Id: I2d0f222e0a4dc382819f862402c312000b720c7c
    
    Conflicts:
    	res/values/strings.xml
    	src/com/dirtyunicorns/dutweaks/fragments/QSTileHolder.java

commit 07a009907b503adee384e93bc093b08442d9b7bd
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Feb 24 00:21:54 2015 -0700

    NavBar tile [3/3]
    
    Change-Id: Ic705dff976a70eb766c2629c1100223355653f4d
    
    Conflicts:
    	res/values/strings.xml
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit 985d659623ba41f6e6955c7ee2bba8e673d0eebc
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Feb 24 00:23:11 2015 -0700

    App Circle Bar Tile [3/3]
    
    Change-Id: I2863c4f24ed15f2d860daca9323d7e761b7575ff
    
    Conflicts:
    	res/values/strings.xml

commit 969634698332e16ad143095070ef88071ca6439a
Author: Beeko <bcobine@gmail.com>
Date:   Wed Feb 25 23:27:31 2015 -0700

    Add USB Tether Tile (1/2)
    
    Change-Id: I44c0fe278d5e1db85f450cac38b9cdf733eb5d08
    
    Conflicts:
    	res/values/pac_strings.xml
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit cdfd9cfc8cb1640dc390ff1cb1bb025524fd4080
Author: martincz <martincz@mokeedev.com>
Date:   Thu Apr 9 14:11:46 2015 -0700

     Show carrier label / custom & change color [2/2]
    
    Change-Id: I122f57b42341483ffbcb574d18da74bd65aa70c7
    
    Conflicts:
    	res/xml/statusbar.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml

commit 2988b8fd13a02ac7562dca2413d33f9a7ed68f18
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 14:25:35 2015 -0700

    Removed screenrecord
    
    Change-Id: I54e81db751af9e1d6f0fb708e967f45c2b045e57

commit f6c6ca659d4e617793a0ee94a97a4c86045c92a6
Author: eyosen <abittin@gmail.com>
Date:   Thu Apr 9 14:33:05 2015 -0700

    Add Screen Record to the Power Menu [2/2]
    
    PS1: Added to CM base
    PS2: cleanup on isle 5
    
    Change-Id: Ia61545db9a313865e38cc68f85c0c22b67cb87a5
    
    Conflicts:
    	res/values/cm_arrays.xml
    	res/xml/power_menu_settings.xml
    	src/com/android/settings/cyanogenmod/PowerMenuActions.java

commit 13e2a6c17cfecd9f11f6cf3e7a54ae5ce749bf9e
Author: eyosen <abittin@gmail.com>
Date:   Thu Feb 5 14:21:01 2015 +0200

    QS: add Screenrecord tile (2/2)
    
    Change-Id: Ie2a283fedbffe4f94ccd448421eabc879225868a
    
    Conflicts:
    	res/values/strings_aicp.xml

commit e2ef7af8f3060a9a4f1f6348a69eefe27d649ed5
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 9 14:35:36 2015 -0700

    move QS string to cmremix
    
    Change-Id: Ifc1cf757ae56816cd6b50cab76b38cafd1d45c37

commit dd4a5f5b88d2e72927dc15c68a78e7e6fb62ca89
Author: LorDClockaN <davor@losinj.com>
Date:   Thu Apr 9 15:42:36 2015 -0700

    Settings: Hide network activity arrows (2/2)
    
    PS2: Rebase
    PS3: Track proper logic
         Add dynamic summary
    
    Change-Id: I5108d47385a3a7f5d33d9c23963bdb67754f03da
    
    Modified for temasek
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java

commit d7f85d437639e2692030fe69d197322eb7ef7575
Author: KreAch3R <kreach3r@users.noreply.github.com>
Date:   Sun Mar 1 00:44:07 2015 +0200

    Add option to hide Bluetooth Icon when disconnected in Status Bar (2/2)
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    
    Change-Id: Ide1f8295895aeef60e00c9086caf0c7ecee66f39

commit 5d0b3bc7270c282941506a974e1fb49d7b087c2a
Author: Dave Kessler <activethrasher00@gmail.com>
Date:   Thu Apr 9 16:28:07 2015 -0700

    Settings: Statusbar greeting (2/2)
    
    organized statusbar
    
    Change-Id: Idfb665132983b109852ae6ede999baf190183fe3
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java

commit 4709cc593b1ff4711af8d65a2e1cb637f0e8a18d
Author: LorDClockaN <davor@losinj.com>
Date:   Thu Apr 9 18:02:11 2015 -0700

    Settings: Greeting label timeout (2/2)
    PS2:
        Use string for suggested greeting
    PS3:
        Fix build - derp
    
    Change-Id: Ife010911c6ed4615e766ac46393fbc9f3f0b0a2a
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cmremix/utils/SeekBarPreferenceCham.java
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java
    
    Conflicts:
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cyanogenmod/StatusBarSettings.java

commit 27214554d857692d0aa290e36a30566d6a9f4604
Author: martincz <martincz@mokeedev.com>
Date:   Thu Apr 9 09:48:42 2015 -0700

    SQUASH Settings:Smart control center and Direct Call (2/4)
    
    Change-Id: Ib3c1dd4e45ee02d2c4179c1e0187483187054c78
    
    Conflicts:
    	res/xml/temasek_settings.xml
    
    Conflicts:
    	res/xml/cmremix_custom_settings.xml

commit 6f2268b86ff3cc9ffe84604dffeecadc6372d410
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Thu Apr 9 09:54:57 2015 -0700

    Settings: long press lock screen lock icon to sleep (2/2)
    
    Change-Id: I091de18ad5a3c4eb28ef9571cc92af8eb72e3626
    
    Conflicts:
    	res/values/custom_strings.xml
    	res/xml/security_settings_password.xml
    	res/xml/security_settings_pin.xml
    
    Conflicts:
    	res/xml/security_settings_chooser.xml
    	res/xml/security_settings_password.xml
    
    Conflicts:
    	res/xml/security_settings_chooser.xml
    	res/xml/security_settings_password.xml

commit a2620f7b13d746eed4d3112f09ab19574e8c0311
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Thu Apr 9 18:08:08 2015 -0700

    QS: add Ambient display tile
    * add Ambient display settings activity for long press on tile
    
    Drawables thanks to Alexander Westphal <westphal.alex94@gmail.com>
    
    Change-Id: Id52c668d7d73d66feac7282861459bd15972f4ac
    
    Conflicts:
    	res/values/custom_strings.xml
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java
    
    Conflicts:
    	AndroidManifest.xml
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java
    
    Conflicts:
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java
    
    Conflicts:
    	res/values/cm_strings.xml

commit b03b84cd87f5864ec927df892bc30f4392c2d3d8
Author: 0xD34D <clark@scheffsblend.com>
Date:   Thu Apr 9 10:01:00 2015 -0700

    [2/2] App sidebar
    
    port from KK4.4 to CMRemix Lollipop
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/cmremix_custom_settings.xml
    
    Change-Id: Id61a02cf942cb5b6f680654147a4fe9c955be252

commit 9a3392075faa117b96a2bd35a5886d7cd214ada9
Author: alviteri <davidteri91@gmail.com>
Date:   Tue Mar 3 22:22:14 2015 -0700

    Settings: Add 1 second to Volume Panel Timeout
    
    This update the following commit: e1f51414164098a50125dc5877b6309d76cf8454
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    
    Change-Id: I12ee620e7cb4eb629edc2325b73a1f0beea28139

commit 3eec4d81fa8cae0b48b97a7556f8ecb65beea4cb
Author: Jmz <jmztaylor@gmail.com>
Date:   Thu Apr 9 18:24:28 2015 -0700

    Force Expanded Notifications (2/2)
    
    AICPfy
    
    Change-Id: I986715c71f8cc4b02700afa0be5550e4efc4ba2d
    
    Conflicts:
    	res/values/cr_strings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/notification_drawer_settings.xml

commit d5fe1503424a023f2ced97e02eb1642d14cf441f
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 9 10:17:26 2015 -0700

    Settings: Slim Actions to Shortcuts
    
    Change-Id: I8c9a524f3628c47e882347225372ff065b4f2b94
    
    Conflicts:
    	res/values/cr_arrays.xml
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml

commit 9193b5f908f6eff2e741181e3773394b9abb2219
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 9 10:19:35 2015 -0700

    Settings: SlimAction as QuickTile (2/2)
    
    Configure which Slim actions you want to use as tile and then add the 'SlimAction' tile.
    Single press will switch between Slim actions and long press will execute the Slim action. If the tile has only one Slim action, single press will execute the action.
    
    Change-Id: I6a01ca065801a2ceabf1b0c21dc9d9c0a0289af2
    
    Conflicts:
    	res/xml/notification_drawer_settings.xml
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/xml/notification_drawer_settings.xml
    
    Conflicts:
    	res/xml/notification_drawer_settings.xml
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit 3511e269385f804a0763f28d5a3504e00b6c047b
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Mar 10 17:48:08 2015 +0100

    Settings: Dotted circle battery (2/2)
    
    Change-Id: I025ba037143fcdfff99acd955532e34a3befd944

commit f98ce369bfbb2faa25aba571ff9a51c787a2a4c8
Author: alviteri <davidteri91@gmail.com>
Date:   Thu Mar 5 06:00:00 2015 +0100

    Settings: Materialize standard colors in colorpicker
    
    Change-Id: I8afa8fec913d74444ec040d397a9a3db7244f58f

commit e897e5e79538b0e1d4c35c1c26d9d1f1961a2838
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Mar 12 20:41:23 2015 -0700

    (2/2) Settings: allow to toggle smart cover wake
    
      * disable by default
    
    Change-Id: I1f97dc1a945520d2b563cdafdb19becad23cb993
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit b0e4ba7953148e5c0e0505f9055a4c3480d3da73
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon Mar 16 11:55:44 2015 +0800

    Fix Settings FC in non-Advanced mode (Buttons Setting)
    
    Change-Id: Ib6915094dca9ade3752696734bac9a800c2eeb89

commit 3f6effe2057092588fe6cadfbc4845bff1440359
Author: cristianomatos <cristianobmatos@gmail.com>
Date:   Thu Apr 9 20:50:52 2015 -0700

    [Lockscreen shortcuts] centralize all option in our custom settings
    
    Change-Id: I2000a66e6dd50a73ef0dcb41e283f6492207007a

commit 56a6c30a0596a55ccc15d6f50b11af775fbdcce1
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 10 08:25:41 2015 -0700

    we use CMRemix now
    
    Change-Id: Ib57906c18f22d5ed1b1e06f0c2741942c81a2255

commit 24b9c4d58d0a5a1768c73d99f90738b34e8c0716
Author: PerfectSlayer <slimroms@hardcoding.fr>
Date:   Fri Apr 10 11:09:05 2015 -0700

    [2/2] Settings: Add network meter
    
    Add the neterwork meter settings to slim statusbar settings
    
    AICPfy
    Edits to work with existing Network meter
    
    Change-Id: Id989b9a13c25e2d0d7ef742e9c54f9ca6ea9f2ae
    
    Conflicts:
    	res/values/ids_aicp.xml
    	res/values/slim_ids.xml
    	res/xml/cmremix_display_settings.xml
    	res/xml/status_bar_settings.xml

commit 11ec37f1a4989ac5823735f56e8e89036800ec8f
Author: LorDClockaN <davor@losinj.com>
Date:   Fri Apr 10 11:19:07 2015 -0700

    REVERT old network meter and add color to new one (2/2)
    
    Change-Id: I8bee14cbc1a00353f334830fa5817c0980ef84ad
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    	res/xml/network_traffic.xml
    	res/xml/status_bar_settings.xml
    	src/com/android/settings/cmremix/NetworkTraffic.java

commit f395d02b26fcfd88b03d094b3d11c68d85ab25a1
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Fri Apr 10 11:28:45 2015 -0700

     Lock screen: Weather panel improvements, (2/2)
    
    CMRemix's fy
    
    Change-Id: I9588769b26b0b797c3f19a7e0887fbf8238588cc

commit 5de1aadea10c36cf2540c13f472aa2b850137bb7
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Fri Apr 10 11:36:21 2015 -0700

    Lock screen: Text and icon colors, (2/2)
    
    Change-Id: Ib4a085aa00769b05530f6dfdfbf18c0792b31cc3
    
    Conflicts:
    	res/values/cmr_strings.xml

project packages/apps/SlimLauncher/
commit e16b8cb2aabda7bc1863b7bcd6b205dd72fbd041
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Thu Nov 6 01:40:33 2014 +0100

    Change module name
    
    Change-Id: Ie4f9d6d0ed03160954ea5de61d982d19af129b14

project packages/apps/SoundRecorder/
commit d5d1811590d6c2afe8e272d459c113348eaf3525
Author: Adnan <adnan@cyngn.com>
Date:   Tue Mar 17 14:51:39 2015 -0700

    SoundRecorder: Rewrite logic to funnel all recorder interaction.
    
      Otherwise we're sleeping on the ui thread for no reason and causing
      jank which confuses the end user and just provides an overall bad
      experience.
    
      Instead, create a separate thread for everything related to the recorder
      and pump all ui events back to the ui thread via empty messages.
    
    JIRA: ALCATELTCL-126
    
    Change-Id: I95e55cf88d332b78ef68250b99655dfc2746d476
    (cherry picked from commit b31b6a148807248ddf8f9a2d1414c62682a49f3f)

project packages/apps/ThemeChooser/
commit 87096d5517185217527f5f8301363408b4e9b22d
Author: david <davidteri91@gmail.com>
Date:   Sun Feb 22 17:07:59 2015 +0100

    ThemeChooser: Hide from Drawer Launcher
    
    This was picked from the following commit: 0ddaa79207d08f239aec1eae1c78d90753278137
    
    Change-Id: I2192ef1b22cb56eafd23843eb1014187b3ac0788

project packages/inputmethods/LatinIME/
commit ad70be9e21db84dd4bc7d71123867d48f6a70ee9
Author: KhasMek <Boushh@gmail.com>
Date:   Tue Feb 4 22:59:52 2014 -0700

    Rearrange morekeys
    
      Some of the symbols such as *,!,-,+ were moved in kitkat,
      this moves the moreKeys to be inline with the moves.
    
    Change-Id: I5aff699b268dd32a5b1e4539163e6ec153021f0a

commit 6d1c8e97854e547220b0ada7aa26439db12a5de1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Apr 4 01:14:38 2015 +0300

    Rearrange Slavic & Greek morekeys
    
    * Following the previous change
    
    Change-Id: I5b5a9bff8dd97c0bf31bc5e28245a9c14662d583

project packages/providers/ContactsProvider/
commit 210a1abffd40104cc7b8172355be3d4c4524becb
Author: emancebo <emancebo@cyngn.com>
Date:   Thu Apr 2 15:28:00 2015 -0700

    Fix upgrade path for phone_lookup table
    
    Previously the phone_lookup table had a column named NORMALIZED which had
    a non-null constraint.  That column is no longer populated but there is no
    upgrade path to remove it, hence new contacts cannot be inserted into
    phone_lookup when the old schema is present.
    
    Change-Id: Iba35003f4fa122a174af804ed94e3991a320e416
    (cherry picked from commit e61272843fcf01c20b2db960fe31131bb81d18a2)

project packages/providers/MediaProvider/
commit e6041cdf95e310bfd5d7aa72a6cac05a82287b1f
Author: blk_jack <jcorcoran+github@gmail.com>
Date:   Mon Feb 2 01:42:36 2015 -0700

    MediaProvider: MediaScanner behavior on boot (2/3)
    
    Lets you enable/disable/ask (with a notification) media scanning on boot.
    Can speed up boot and reduce initial boot lag from MediaScanner
    
    - added xxhdpi icon
    - no need for multiuser due that this should be a one time set
      general option set by the owner of the device
    
    Change-Id: Iad0b72f8b653b3d567b27de3ccf5c6cfb07e40ed
    
    (cherry picked from commit 8b534858102b02eedce70c01bd81a6e791111253)
    
    (cherry picked from commit 8b534858102b02eedce70c01bd81a6e791111253)
    (cherry picked from commit b9fee0272cd6b974bacd802722d244ab7c2271d1)

project packages/providers/TelephonyProvider/
commit 553933c7399ef8a06cf9035b1781926bcf566cf5
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Mar 31 09:01:56 2015 +0200

    Add proper DB upgrade path.
    
    Add back the CM11 upgrade path and a phone_id -> sub_id conversion.
    
    Change-Id: I1f26dca48ac1536a524177ff20e59d7242100861

project packages/services/Telecomm/
commit e611ca7dcabe0be837c401a304e97cc310d6f099
Author: Pawit Pornkitprasan <p.pawit@gmail.com>
Date:   Sun Mar 15 08:33:32 2015 +0700

    CallsManager: fix starting call from Contacts app with MSim
    
    The extras bundle may be Bundle.EMPTY, which immutable. Create our
    own copy to modify.
    
    Change-Id: If875eddc6afe9c5ca4b0d59a51902529cf115487

commit b8fcaec6a8551b68d592c100b8baf87305868600
Author: Pawit Pornkitprasan <p.pawit@gmail.com>
Date:   Sun Apr 5 10:15:00 2015 +0700

    Revert "Subscription selection when dialing USSD"
    
    This is already handled by AOSP in Dialer.
    
    This reverts commit 63605bb077cf87d0678197b42527f6c0a4eb6436.
    
    Conflicts:
    	res/values/colors.xml
    	res/values/strings.xml
    	src/com/android/server/telecom/AccountSelection.java
    	src/com/android/server/telecom/CallsManager.java
    
    Change-Id: Ib5d49a6b7685c3781fad122f2d1e612993ff9e6a

commit f94f958fdd78fe5c150e68c372e66f7b3a120942
Merge: b8fcaec e611ca7
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Apr 6 11:38:01 2015 +0000

    Merge "CallsManager: fix starting call from Contacts app with MSim" into cm-12.1

commit 283b4cec87cdbcbd1d3310f4113511c3503f4dc7
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 7 11:30:23 2015 +0200

    Fix merge failures.
    
    Re-apply the following patches which seemingly got lost while merging:
    - d5c2fcf3bc8fc8ae08c05d7172e2244335c73e8f
      "Fix connection <=> call capability conversion."
    - a21edb812cc2c5af94bdbb1f7d2d96ee1d9f4fb9
      "Properly convert GENERIC_CONFERENCE capabilities."
    - 79d646f9a02d03f8cdc1dd81bb35cccbff09bf47
      "Remove line to allow hiding SMS response from InCallUI in multiSIM."
    
    Change-Id: Ic6c11c60e6dddb813cc822ffefb438d75e7ddba9

commit 51eb0a9406bf015dbaf158abb90806a0f716cce8
Author: garwedgess <garethwilliams21@gmail.com>
Date:   Sun Feb 22 02:22:10 2015 -0700

    [4/4] Telecomm: Breathing missedcall/sms/voicemail
    
    Base: https://gerrit.omnirom.org/#/c/4976/
    Mms: https://gerrit.omnirom.org/#/c/4977/
    OmniGears: https://gerrit.omnirom.org/#/c/4978/
    
    Change-Id: I0e0d6762d1b2aeeb2109a358dffe62ecc825c932
    
    @alviteri: Port by me to crDroid Android
    
    This commit is special due to Lollipop is using Telephony repo for notify voicecalls so this commit is divided in two (2/2)
    
    Conflicts:
    	src/com/android/phone/NotificationMgr.java

project packages/services/Telephony/
commit 85ca7b7da35fcc1ef85187370b0447ab18ea6d19
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 7 10:22:14 2015 +0200

    Fix CAF merge issue.
    
    [s|g]etCallCapabilities map onto [s|g]etConnectionCapabilities now, so
    don't use separate methods to generate the flags. This fixes
    connection type specific flags (e.g. CAPABILITY_MUTE) getting lost.
    
    Change-Id: I9a306374eef44ac45fee66f4f2c26f6c02e64b37

commit fcfe4d4b5ef781bad02895fd088be2c2e54a0635
Author: garwedgess <garethwilliams21@gmail.com>
Date:   Sun Feb 22 02:25:36 2015 -0700

    [4/4] Telephony: Breathing missedcall/sms/voicemail
    
    Base: https://gerrit.omnirom.org/#/c/4976/
    Mms: https://gerrit.omnirom.org/#/c/4977/
    OmniGears: https://gerrit.omnirom.org/#/c/4978/
    
    Change-Id: I0e0d6762d1b2aeeb2109a358dffe62ecc825c932
    
    @alviteri: Port by me to crDroid Android
    
    This commit is special due to Lollipop is using Telecomm repo for notify calls so this commit is divided in two (1/2)
    
    Conflicts:
    	src/com/android/phone/NotificationMgr.java

commit c1c4e6c0c2b0135e2a2a296b309d2a5893fb80a7
Author: Kryten2k35 <kryten2k35@gmail.com>
Date:   Thu Apr 9 22:46:07 2015 -0700

    [2/3] Call recording encoder/format choice
    Adds a user option between NB AMR (the default) or HE-AAC for the encoding of call recording audio. Also changes the output format of the file appropriately (NB AMR now uses the NB_AMR output format and HE_AAC chooses the MPEG_4 output. File extensions are adjust accordingly as well).
    This was in reponse to people complaining the quality of call recording audio is poor. It's noticibly better using HE-AAC, but filesizes are larger.
    
    Change-Id: I31f4a57042cf9e221ea2292922f071c955170e1e
    
    PS: Imported from kitkat and made working for lollipop.
    
    Signed-off-by: BlackDragon <blackdragon.fusionteam@gmail.com>
    
    Conflicts:
    	res/values/cmr_strings.xml
    	src/com/android/phone/CallFeaturesSetting.java

commit d926c3ccae2f28f56be3e107d48d803c49099cd0
Author: lichti1901 <lichti190185@gmail.com>
Date:   Fri Apr 10 12:29:00 2015 -0700

    National Data Roaming [2/3]
    
    (cherry picked from commit 470bb05199b199ed9d2a663a87ed6e39ac69ed22)
    
    Conflicts:
    	res/values/cmr_strings.xml
    
    Change-Id: I212bd696d8ab1afe6dbaa6df4d93ad6d42007a16

commit 6290b31550c8d3cbba834879655cae4f85df173c
Author: Janson Kang <temasek71@gmail.com>
Date:   Thu Jan 1 10:12:18 2015 +0800

    Fix National Roaming
    
    (cherry picked from commit 81bcf4c2c8c5fa98af996e657f4d3a5bc27a142d)
    
    (cherry picked from commit 81bcf4c2c8c5fa98af996e657f4d3a5bc27a142d)
    
    Change-Id: Ib001cec3ab868273b71480cd3c8fd935e7817c1c

project system/core/
commit 34fe8ef397197949785d1c9616b7cf991c239b51
Merge: 27f8ec6 354483f
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 16:56:29 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

project system/vold/
commit b240c858bb81b0d0e61a74c49579b8eba14982a8
Author: kallt_kaffe <kallt_kaffe@apedroid.com>
Date:   Thu Oct 13 14:38:29 2011 +0200

    vold: add ro.vold.umsdirtyratio property
    
    This allows control of what /proc/sys/vm/dirty_ratio is used when USB mounting.
    Some platforms like the HTC Desire (bravo) get a _HUGE_ performance boost when
    writing to the sdcard when USB mounting if this is set to 20 (which is the default)
    on the HTC Desire.
    
    This addresses this issue: http://code.google.com/p/cyanogenmod/issues/detail?id=2949
    
    Basicly it makes it possible to undo or control the effect of this commit:
    https://github.com/CyanogenMod/android_system_vold/commit/a28056b38275003895ff5d9576681aca01544822
    
    Change-Id: I86b7bbd02695fb0c19f39448714a219257bf806f

project vendor/cm/
commit 779bc74e40aaa6d31fa1207451d50b667feff3a3
Author: Howard M. Harte <hharte@cyngn.com>
Date:   Fri Apr 3 18:23:18 2015 -0700

    Update APNs for Smartfren
    
    Change-Id: Id88ff4a559f50e83c52e709e8887d91a4f9ba132
    (cherry picked from commit 2036a6fe36af24e5bd6cd7b3838d6fb47b13c12e)

commit da87a7db233b8ad19eb8bd216f28ac84d5f6c1ad
Author: Emerson Pinter <dev@pinter.com.br>
Date:   Sat Mar 28 01:36:47 2015 -0300

    userinit: kill userinit.d
    
    We can't give exec permissions on /data, userinit.sh is sufficient for
    most cases.
    
    Change-Id: I924cecb2cd2ecf71bc15f77dccd2c28a19341b91

commit ffe07b85ebc8613b8f93e1f3fa397c2abde064e2
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Apr 5 10:59:21 2015 -0400

    cm: CM-specific build macros
    
     * vendor/*/build/core/definitions.mk is automatically sourced by the
       build system to load custom macros. Start using this for some
       of our own.
     * Adds a "uniq" macro to remove duplicates from a list without changing
       it's order.
    
    Change-Id: Id5f1eb4b9f81bb31ca0b3d5e74c298b3d105da10

commit 700484dbcc5511445b132960fd7f0c8b0c318dc1
Author: Andreas Blaesius <skate4life@gmx.de>
Date:   Tue Apr 7 11:30:04 2015 +0200

    Fix generate-half-res-anims.sh and halfres bootanimation.zips
    
    bootanimation.zip contains PNG files and not JPG
    
    Some zips aren't resized and use original resolution instead half resolution,
    fix it too.
    
    Change-Id: Ic12f93dc2a18f7ca9c9c7bff6b34dc0821bbfb4c

commit 1db6cf185fde70e218dd160f79cabbcedd40f4a3
Author: Zyg0te <edvard.holst@gmail.com>
Date:   Wed Apr 8 10:44:24 2015 +0200

    apns: Added APNs for Movistar Peru
    
    This references CYAN-6451.
    
    Values based on movistar support document: http://catalogo.movistar.com.pe/ArchivosUsuario/ArchivoGuia/LG-T310-Plum-2G-CONFIGURACION-PERFIL-MMS.pdf
    
    Change-Id: I98822dc2c29ed00ccf2792e83a06a8ed14051de7
    (cherry picked from commit 4203778b54fa511c26a9498bd346c653f2d6add6)

project vendor/cmremix/
commit 3e523eb7649d2193923d1e14e60c2bd31cb7accb
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 3 15:59:42 2015 -0700

    Removed: Add Prebuilt libwebviewchromium libs
    
    * I can't seem to fix libwebviewchromium without losing optimizations so let's see if these will replace the libs and work for people
    
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>

commit 601c75956cea7eef1c4a74d6e3c9dd5ac463c57b
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 13:38:01 2015 -0700

    fixed chromium

commit 75a6bf80f653ecaaa2d577a685a322c3d8ff4b2e
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 4 13:44:17 2015 -0700

    build Slim Launcher
