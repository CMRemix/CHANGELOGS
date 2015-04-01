
project bootable/recovery/
commit 471eb4e140b36c9a6092c70bf4e286961b1378e3
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Thu Mar 26 14:11:04 2015 -0700

    update-binary: support reboot_now on older recoveries
    
    Attempt to reboot using older methods in case the recovery that we
    are updating does not support init reboots
    
    Change-Id: I9d6ec23c65291221e99d67b2361a2bd150319eee

project build/
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

commit 808f27628e83ee31ad751b3970b1598024bd2832
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 00:37:27 2015 -0700

    build: add cmremix version info
    
    Change-Id: I0fecd60a97b5c46f3262d5f030c6a23b2d2de5d0

project cmRemiX/
commit 3f2093da9b3d93d025b2ee8ebc3532458f277165
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:19:07 2015 -0700

    track SM arm-linux-androideabi-4.9

project frameworks/av/
commit b2de0c19b11c8b83873510eb6c629cf4cfd62b1e
Merge: cf8c5de c29fb05
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 27 20:24:13 2015 -0700

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

commit b1fc70a8b913fb01889586d3b6bdf5453562383f
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
commit cb410679dc0c9871af9e003e9487d9d7d205f4ba
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 24 16:31:42 2015 -0700

    C M R

commit 013558da4e65ec19301223da4815c114cfcb4d82
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 29 11:49:47 2015 -0700

    vendor: update sabermod.mk

commit 8fb14ce8ddf4683b1cd132cac87a45e5c0fe9198
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 03:37:31 2015 -0700

    tools: change CMRemix major version

commit e5e5a01527fd0eed608de774ff3f07fe41963eed
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 31 04:03:34 2015 -0700

    update ota version

commit 3a88e06bc94087727d854da79fb1b14bf7f5331d
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 1 01:46:51 2015 -0700

    build CMRemix Center

project vendor/samsung/
commit e9fb886f2f23701c9e3e0b55343fc3da1c66ac7e
Merge: cb8d668 9024b30
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Fri Mar 27 08:44:39 2015 -0500

    Merge pull request #602 from sbrissen/cm-12.0
    
    KK ril update for p4notelte and t0lte
