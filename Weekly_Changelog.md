project CMRemix/
commit 91f917aa9e1911d8bccf87f6173d746d93a103eb
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 03:25:51 2015 -0700

    track development

commit 330b2937e85eb77e4eb3a66a13683c59dfbd58be
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 18:57:25 2015 -0700

    fixed prebuilts_ndk

commit ac181a21ce14b46fe11ce45e6594e10931d550d9
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 19:00:58 2015 -0700

    fixed copy and past again

commit c17345cd04d5ee3e0e66dd6a667872d8fe187e5e
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 11:39:39 2015 -0700

    track ContactsProvider

project bootable/recovery/
commit 0225ffe3ff195eae032131b0c1ff9c9fb87fc047
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Apr 20 11:27:18 2015 +0200

    Remove spammy debug output.
    
    Change-Id: Id152a6b57a8749fb6a68d8132bbd6bb5e87b7336

commit e63fbec600fecfc5038bc6e6babb8f476b906144
Author: Johan Redestig <johan.redestig@sonymobile.com>
Date:   Tue Apr 14 21:20:06 2015 +0200

    imgdiff: Avoid infinite loop if inflate fails
    
    Break out of the loop if inflate returns an error
    and print some details.
    
    Change-Id: Ie157cf943291b1a26f4523b17691dfcefbc881dc

project build/
commit cfc20667a3a9f572bd188563903891478d333c93
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Apr 28 10:44:20 2015 -0600

    Add a option to disable vectorization flags (2/2)
    
    Change-Id: I2bd7a1a554b0680faa2da36be1866e8f57e0166c
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 3ae29bccd6304fba3b45d850d169bf649dd16ffc
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Apr 29 13:11:59 2015 -0600

    Update for vendor changes
    
    Change-Id: I16418f4d80cc9ba4cdd557fe748d9d5d594401eb
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 50cbe76e881b78a82eb9e9fb8cceb1b12eeb995b
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 30 10:09:24 2015 -0600

    No optimizations for bluetooth modules
    
    Change-Id: If5b5b115be5e4affff55aa275055dcda61dffc3d
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

project device/samsung/qcom-common/
commit 1366afc75da0277ee032c15a19cdb4ed68abe621
Author: Brinly Taylor <uberlaggydarwin@gmail.com>
Date:   Tue Apr 28 05:27:00 2015 -0500

    qcom: remove TARGET_CPU_SMP flag
    
    * TARGET_CPU_SMP defaults to true in Lollipop
    
    Change-Id: I2a80290861d47eeab0bf615ac05a17e7544c6841

project device/samsung/trlte-common/
commit f26cc2e73a0b96832bb94b72e09746f24334ccd5
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Fri May 1 20:39:53 2015 -0400

    increase mic volume
    
    Change-Id: Ia695f4b08563f58449facd520a9168a8e92bc487

commit 04ae406f067aa102d8db2788df8f34fa9934a7fb
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Sat May 2 09:55:49 2015 -0400

    trlte cam wrapper to use nv12-venus
    
    Change-Id: I004ec622cc99f29905fa0c0baa2eb9835baac284

commit acd21e9eeb1618dda94ef27e7b71d4f9afc38708
Author: Tony Layher <layhertony@gmail.com>
Date:   Sun Apr 5 22:23:01 2015 -0400

    trlte: mediaserver doesn't actually need access to serial devices.
    
    Change-Id: I8ce17f2f394763e2a335b18ca49e585a5bb380c2

commit 51e09398dfc24c4c74942d20642405080051e54e
Author: Tony Layher <layhertony@gmail.com>
Date:   Sat May 2 14:12:10 2015 -0400

    trlte-common: Clean up camera code, fix up wrapper for multiple apps.
    
        Add board define to change the way we handle the HAL.
        There are some differences between the US and INTL
        variants we are accounting for.
    
    Change-Id: I189da6c02fe6ed0b39d6d848ed020147f35b663f

commit cc58943b336ba1e9985e2a5fb843574faf422b9a
Merge: 971eb7c 51e0939
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 11:32:13 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 330c7b00a797d8633a5ec22c13e8e91bd55cc24c
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 21:43:55 2015 -0700

    Revert: init.qcom.rc: Stop mpdecision at boot (reverted from commit 3e5ee728e704a0f7867452c3e2084d90f5356dd7)
    
    Change-Id: I2c1c090a3b3352f5513a6aa86cdb41c7cf349d11

project external/tinycompress/
commit dcc9b99df25c419297ff0aca9b53dcbf26aa3526
Author: Rashed Abdel-Tawab <rashed@linux.com>
Date:   Fri May 1 17:33:39 2015 -0400

    tinycompress: Fix build on msm899x
    
    Oops, put the ifneq in the wrong place, the CFLAG was
    getting reset only 2 lines later when the build system
    clears the local variables
    
    Change-Id: I7541359706d1144f1c2afa60816c1209371e4b0f

project external/whispersystems/WhisperPush/
commit 519b1132bf6549ebc06691e8362b930c37e2c5a1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:55:17 2015 +0300

    Automatic translation import
    
    Change-Id: I0078d634e54e91daec6f80633f6523ce40e7a180

project frameworks/av/
commit fb629ad8e893fb6f1817dbccb5178ab04de63f54
Author: RenJian <jian.ren@ck-telecom.com>
Date:   Wed Apr 15 11:32:15 2015 +0800

    Ensure there is no two same storages showing on the computer.
    
    [Preconditions]
    1. Insert a SIM card into phone and set the SIM lock as "on"
    2. Select MTP mode
    3. Power off the mobile
    
    [Procedures]
    1.Connected the phone and PC with usb cable
    2.Power on the phone->Input PIN code of SIM lock to enter the IDLE view
    3.Check the storage list on PC
    
    [Reproduce]
    Rarely
    
    Change-Id: I8efc3f812b669f2d4e2c3be89e3f97b5cc895628
    (cherry picked from commit 8b8d02886bd9fb8d5ad451c03e486cfad74aa74e)

commit bd4881c961173dd7b5aa4708a7444cc4d556c2ca
Author: Diogo Ferreira <defer@cyngn.com>
Date:   Wed Apr 29 17:36:32 2015 +0100

    stagefright: Configure codecs correctly in the mediatek platform
    
    We were setting the width/height as stride/sliceheight for both
    MTK and software codecs, which is wrong, it is only required in the
    former and will cause visual corruption in the later.
    
    Additionally, this adds buffer alignment which prevents MTK codecs
    from following a slower path.
    
    Finally, we're now also using stride/sliceheight whenever extracting
    a video frame.
    
    Change-Id: I3c40e17ad1757d3b27d919bf5378974b971aaacf

commit f519217633249883bcaaf6e79cc457cd2a50a2af
Author: Eric Laurent <elaurent@google.com>
Date:   Tue Oct 28 15:46:45 2014 -0700

    audio policy: validate stream type received from binder calls.
    
    Bug: 18001784.
    Bug: 18002005.
    
    Conflicts:
    	services/audiopolicy/AudioPolicyInterfaceImpl.cpp
    	services/audiopolicy/AudioPolicyInterfaceImplLegacy.cpp
    
    Change-Id: I8efa674dceff5a6e10251b1c7a55e9bb2d532395

commit 9fe3b80f53ed419e5dba1034e72f072e100beace
Author: Leena Winterrowd <lenhardw@codeaurora.org>
Date:   Wed Feb 25 14:28:52 2015 -0800

    mpeg2ts: Enable timestamp reordering for HEVC TS content
    
    If HEVC TS content contains B-frames and the frame rate is not
    explicitly set, the decoder may receive out-of-order timestamps
    which manifest as a/v sync issues. Enable timestamp reordering
    for HEVC content in the TS container to resolve such sync issues.
    
    CRs-Fixed: 801290
    Change-Id: I13a2fe382caebc07c8dc046a1344a1b73036cd2e

commit 4f684351042220af8e6fc9b501e12044d54a54b8
Author: Leena Winterrowd <lenhardw@codeaurora.org>
Date:   Thu Apr 2 11:41:59 2015 -0700

    mpeg2ts: Clean up HEVC format checks
    
    - Fix an invalid IDR frame check in ATSParser to avoid a crash on seek
    - Move custom HEVC TS parsing logic to private namespace
    
    CRs-Fixed: 808563
    Change-Id: I1c5ce6719fedd1e2cc9a68c04eb8a7ad795ad3c8

commit 4828d45d0c8d8f6bc144ee2e7d87a4e234246093
Author: Mingming Yin <mingming@codeaurora.org>
Date:   Tue Apr 14 14:14:20 2015 -0700

    Audioflinger: fix for hardware accelerated effects memory leak issue
    
    - Initialize hwAcc to NULL in AudioMixer constructor and delete allocated
      memory in deleteTrackName
    
    Change-Id: Iffe862d1d17345697ac7e233220c2e3f26343f77
    CRs-Fixed: 814304

commit fbe18e6c00c48145017d49c8e073e00348479abf
Author: Satya Krishna Pindiproli <satyak@codeaurora.org>
Date:   Mon Apr 20 12:04:01 2015 +0530

    audiopolicy: fix crash in camcorder during voice call
    
    - During an MO call when camcorder recording is done,
      a crash is observed for the first time.
    
    - The crash is due to an assert that fails because an
      inappropriate value is returned.
    
    - Fix the issue by returning NO_INIT to avoid the assert.
    
    CRs-Fixed: 823350
    Change-Id: Id83111957dab04a3db396401547989db8e8ed573

commit d851d899284fcb060be03a79196578ce48a11eb5
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 28 23:20:32 2015 +0800

    Revert "nuplayer: Modify seek and resume latency calculation"
    
     * Dead code.
    
    This reverts commit 1aff8485242a72417615833d3522363c03ce9a31.
    
    Change-Id: I755f93368e3773add56178eb283b00f9bf8bbb69

commit ec8cc54df791d2000ae46f77e5052a00b4340a7f
Author: Steve Kondik <steve@cyngn.com>
Date:   Wed Apr 29 18:50:53 2015 +0800

    nuplayer: Fix bitrate propagation
    
     * We use "bitrate" rather than "bit-rate".
    
    Change-Id: I4699194e3e3f7ef55b4eb554f5de7a6b5f6b80ce

commit a024ef41bf8471bd2b8452bc01b2974ad2a5164c
Merge: ed8f875 ec8cc54
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 30 11:35:06 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1-2

project frameworks/base/
commit 571c7ed0cf23764e76a41b321ca3ff91103b8da3
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 28 03:01:41 2015 -0700

    fb: TRDS 5.0 (1/4)
    
    patchset: add holodark resources
    
    patchset: add to slim actions
    
    patchset: import Toast library in Action.java
    
    patchset: some tweaks and fixes
    
    patchset: change auto detect light conditions method
    
    patchset: fix possible UI freeze on auto mode change
    
    patchset: import ServiceManager library into uimodemanagerservice
    
    patchset: fix aapt shit
    
    patchset: fix context in UiModeManagerService?
    
    patchset: set mContext to BroadcastReceiver's context,
            add toasts to debug light sensor stuff
    
    patchset: adjust DARK_CONDITION value
    
    patchset: clean up toasts
    
    patchset: fix NPE in Resources.java?
    
    PS20: update BridgePowerManager to fix SDK build
    
    PS21: revert to original BridgePowerManager (if building SDK tools,
            need to use patchset 20 or it will error out)
    
    PS22: more debugging toasts grrrrr
    
    PS23: change holodark to darktheme, hololight to lighttheme.
            remove holodark resources.
    
    PS24: add darktheme resources.
    
    PS26: qs tile
    
    PS27: reset theme mode on longpress qs tile
    
    PS: fix qs icon
    
    CyanideL: Fix up to work ALONGSIDE theme engine
    Change-Id: Ic88838247c47d2a92b55d1cb1b00330f2d62fb88
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/res/res/values/cr_symbols.xml

commit caa3276748106ddd69652bdc9ebcae4bb32e1fb2
Author: rogersb11 <brettrogers11@gmail.com>
Date:   Thu Apr 23 03:43:57 2015 -0400

    Update trds colors
    
    Change-Id: I3f97326752d71d142212a99fcc220975032654d0

commit 2247cbf697d4d216c34949ecfec500f84041cea4
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 28 03:03:32 2015 -0700

    Frameworks: SlimPie give user ability to reduce trigger heights if IME keyboard shows (1/2)
    
    Add a user option to reduce left and right trigger of SlimPie if keyboard shows up
    (especially usefull for swipe keyboard which most keyboards are nowadays). Enabled
    by default user can disable it in settings.
    
    Change-Id: Idc985ebc1d2b14706c26c5c69894b4393b5d57ff
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit cc55fe45881125d3471053e0a7c13b39158b6282
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Tue Apr 28 03:05:19 2015 -0700

    SlimPIE: Configurable sensitivity [1/2]
    
    Change-Id: I636bbbf3a63104625e1cf4698392a480c1f9458a
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 3da027ea507b0f22e902d04d8458e87cd4c04463
Author: Richard MacGregor <rmacgregor@cyngn.com>
Date:   Wed Apr 15 17:13:40 2015 -0700

    Apply sounds on theme update
    
    Add content observer so themeservice knows whether ringtone was
    changed outside of themes.
    
    Change-Id: I83a5dff8e9574019f4d1a5bd58368b0ec3c09c88

commit f9d10ddb15a427277e14abecee8ee32c35bb2d71
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 28 10:55:15 2015 +0200

    Unset frame listener before tearing down GLThreadManager.
    
    Otherwise might lead to messages being delivered to the then dead
    mGLHandlerThread via RequestThreadManager.mPreviewCallback ->
    GLThreadManager.queueNewFrame().
    
    Change-Id: I60001149787c584bfee88c961f1e07cdb8cf3927

commit 3e66f1cbb8f3e82ff5184a2dac7fa485db014563
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Apr 15 09:19:09 2015 -0700

    Torch: remind user flashlight is still on
    
    Post a notification which informs the user the flashlight is still
    enabled. But only do this when the user turns the screen off *while* the
    flashlight is still on, so they see it next time they use the device.
    Tapping on the notification will disable the flashlight.
    
    Change-Id: I3689ff6498b97b813ccc10dc7dca3527fc8455aa
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit d08ecfcf1eb599e873d35522bc2af3ef7a5abbea
Author: Taiju Tsuiki <tzik@google.com>
Date:   Wed Apr 22 16:59:00 2015 +0900

    Fix NullPointerException in Bundle#hasFileDescriptors
    
    Add null check for array elements in Bundle#hasFileDescriptors to avoid NPE on
    null valued array.
    
    Change-Id: Ic6ef8864ca6add023c7a69ba3c9474b0f6291723

commit 0c8b2cdc52629fadf92a6fe168c6e234aecb2df6
Author: Taiju Tsuiki <tzik@google.com>
Date:   Tue Apr 28 13:36:15 2015 +0900

    Fix NPE in Bundle#hasFileDescriptor on null-valued SparseArray
    
    Add a null check for each values of SparseArray in Bundle#hasFileDescriptor
    to avoid NullPointerException.
    
    Change-Id: I43ecc01f2759ccbe85b902fa118d55cb74ebf38b

commit d0481e081e03120a0ad2e22aca8fab0a2a418e2e
Author: Henrik Engström <henrik.engstrom@sonymobile.com>
Date:   Tue Apr 24 15:30:19 2012 +0200

    Fix for infinite loop in RemoteViewsAdapter
    
    This patch fixes an error in RemoteViewsAdapter when there is only one
    view in the cache, and it is bigger than the cache size threshold. This
    would cause the cleanup of the cache to get stuck in an infinite loop
    while holding the mCache lock that is also needed by for example
    getView which is called on the UI thread, leading to ANRs. This patch
    breaks the loop when it sees that it can not remove the next view up
    for removal.
    
    Change-Id: I331259bb10eae9fe91e5112102e08f49cc078a1b

commit 9f42bcf59a548c15ee6dde69f5048acffce5f336
Author: UtkarshGupta <utkarsh.eminem@gmail.com>
Date:   Wed Apr 29 19:40:49 2015 -0700

    [1/2] Battery light: 100% charged level
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 3f75cb94bf0f461246b4c59e7bd26e325cc674a1
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 28 12:46:41 2015 +0200

    Fix fetching application context for ThemedUiContext.
    
    Change-Id: I7719fc8823fef93556f5a9ab088a77b73cf7eeff
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/96386/

commit a0422c3e3e76956627dd4dd2626dca3d8b5b634f
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Wed Apr 29 19:54:37 2015 -0700

    Frameworks: Add ability to control default value of DOZE_ENABLED
    
    Devices can enable the doze feature. Devices without AMODLED screens can use it
    but it will use then of course more battery. This devices should disable this feature
    by default and let the user decide to turn it on.
    
    to change the default behaviour add into device overlay
    
    config_doze_enabled_by_default and set it to false
    
    Change-Id: I1afbf1d09fa0d7e68aea40f2f165a72ff34d0040
    
    Conflicts:
    	core/res/res/values/cmr_config.xml
    	core/res/res/values/cr_symbols.xml

commit 6cf375416da5cb2b31f78c1f5c1d568e50293755
Author: Mikael Gullstrand <mikael.gullstrand@sonymobile.com>
Date:   Tue Jul 9 14:41:28 2013 +0200

    Context leaks in EditText causes out of memory
    
    In android.widget.Editor, Blink runnables can be posted even if
    the related TextView is not attached to a window. If a message has
    been posted to the Blink message queue and the run method of
    the Blink runnable has started executing, the removeCallbacks call
    in onDetachFromWindow method is not enough to abort the execution
    of the Blink runnable. This results in a memory leak when
    the activity is destroyed.
    
    The solution is to cancel the execution of the Blink runnable by
    calling the suspendBlink method from onDetachFromWindow method.
    Hence the Blink thread will halt, and the referenced context can
    be released by GC when the activity is destroyed. Also adding
    a corresponding resumeBlink method call in onAttachedToWindow
    to start executing the Blink runnable.
    
    Change-Id: Icb26c9c947b3cc1158f7629ae35d7b4e42b80f17

commit 04878974c6d62a1eea4423ef5597c8acf82ca778
Author: Lin Ma <lma@cyngn.com>
Date:   Wed Mar 25 17:44:52 2015 -0700

    Fix ro.telephony.default_network setting parsing
    
    * The code that parses ro.telephony.default_network is broken,
    instead of reading numbers separate by comma, it reads the first
    number and replicates it for other slots. Settings like "8,1" will
    be written to the db as "8,8"
    
    Conflicts:
    	packages/SettingsProvider/src/com/android/providers/settings/DatabaseHelper.java
    
    Change-Id: I6b77000e00ada02ec89b09c752a9b337a6a8182b
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/96401/

commit 76921219c7d8d3267a02df1aa05424c93b966b7f
Author: Patrick Lower <devvortex@gmail.com>
Date:   Wed Apr 29 15:25:46 2015 -0400

    MMS (change 1 of 2): Add DATA_PROFILE_MMS constant = 5 to RILConstants.
    
    Some carriers require a separate apn just for MMS.  RIL needs to be aware of this differnt type in order to set the correct network interface information and not interfere with the existing data connection.
    
    Change (2 of 2) 96584
    Change-Id: I793982c1f2032e98a069ff86a748301af4ff6377
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/96582/

commit c1dbd2756034df84e3e3341e8bb035c431d2673a
Author: Danny Baumann <dannybaumann@web.de>
Date:   Thu Apr 23 09:28:43 2015 +0200

    Clean up keyguard carrier text handling.
    
    Return to AOSP code, which both simplifies the code and fixes the
    left alignment.
    
    Change-Id: I1b8974948ace3d55ff92eceace7ea22b715d010d
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/95932/

commit 50d446011731fa572a136f77339373eb89b91a80
Author: dankoman <dankoman30@gmail.com>
Date:   Fri Mar 20 16:54:05 2015 +0100

    slimseekbarpreference: set monitorbox text as string
    
    setting as integer was trying to reference a resId,
            so integer needs to be converted to string
            before setting monitorbox text.
    Change-Id: I085d49240be30e12475db7d88d3b2154d2e65ffd

commit 35e8ce98ee63ed8dd1555cb7da824159b64a7449
Author: d34d <clark@cyngn.com>
Date:   Wed Apr 29 09:04:47 2015 -0700

    Themes: include new icon features in shouldComposeIcon()
    
    Change-Id: I509ae1989fe1ec701cec7bc6ead78ab4e69bd64d

commit 846813104e4ea9b03f03fc0c3f9a010753f1646b
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Apr 15 19:04:19 2015 +0100

    Base: enable/disable doze through Profiles (1/2)
    
    Change-Id: I37a3613a7e4a8d54b43ec9336c4aebc5a92d8d77

commit 82aab46c1b3cffc25bc3649a1c9f2496ad1a8e14
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Thu Apr 30 13:55:58 2015 -0700

    Base: Add a controller for in-call proximity sensor (1/3)
    
    Change-Id: Icd17599ef3e0c45ee10fede7d663ea9a30446257
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 0b0b9b73abe913b54159286f28dbc07e93138328
Author: longyu.huang <longyu.huang2014@gmail.com>
Date:   Thu Apr 23 04:17:14 2015 -0700

    optimize wallpaper load,avoid show black wallpaper.
    
    [Preconditions]
    open auto-rotate
    
    [Procedures]
    1.enter Contacts app, and rotate 90 degrees to the right
    2.press power key to lock screen,and unlock
    3.rotare 90 degrees to the left and exit Contacts app
    4.the wallpaper will be black first,then show the really wallpaper.
    
    Change-Id: Ia8f77b9a685c49cfc0a33e661ef073d90b8b363c

commit 5bf6f6fda1bc09836ea858c76116da142373b390
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 30 11:44:57 2015 -0700

    SystemUI: bluetooth tile: fix disconnect action
    
    Change-Id: I3858dae5539baeb6e70220e39af9cc22134280c9
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 84512731ebca12d01e4c585ca7a9f7a9fd9bd5d7
Author: Apoorv Raghuvanshi <apoorvr@codeaurora.org>
Date:   Mon Mar 30 17:58:55 2015 -0700

    audio: Playback over USB DAC connected before boot
    
    Playback over USB DAC does not work if USB cable from MTP
    to USB DAC is connected before phone bootup. Fix by making
    sure if USB is connected then picking the same
    
    Change-Id: Ifb10e794ed7f21bcf26349440d2c2a9baf7a28aa
    CRs-Fixed:803353

commit ab858c8b6b01f6468cd1591ce8569f4a0466b562
Author: Ravinder Konka <rkonka@codeaurora.org>
Date:   Tue Dec 30 16:57:36 2014 +0530

    Tethering: Set sys.usb.tethering to true on Tethering
    
    Set the system Property "sys.usb.tethering" to true when
    tethering is enabled on UI
    
    Change-Id: I805a38b2d3ed055a562298d71f33fd5030b3a4a0

commit 0e988e896ed37de936b094bc6303d1f1777f18e2
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Mon Jan 5 10:44:19 2015 +0800

    Widget: Catch null point exception in AbsListViewAutoScroller
    
    The first view of AbsListView is null, so there is a NullPointerException
    happen.
    
    Add a judgement for the first view of AbsListView.
    
    CRs-Fixed: 776294
    
    Change-Id: I7e25d1430b1bab0cff313492163a419fbf5960b5

commit c3de0de6ada8e078d7229aec1a4f0a397f4b7eb7
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Mon Feb 9 14:08:14 2015 +0800

    WindowManager: Disable rotation for BootAnimation screen
    
    BootAnimation screen is not rotated when device bootup or shutdown.
    And still should not be rotated when device doing factory data
    reseting. Otherwise BootAnimation layer would only cover the left
    part of the screen and display error.
    
    Change-Id: I79515dcc87965257e1773142138a84449fb711e4
    CRs-Fixed: 784522

commit ba19da1b8c46ad287afa263701cc8b2b46705825
Author: Kun Liang <kunliang@codeaurora.org>
Date:   Tue Jan 6 15:21:04 2015 +0800

    AppOps: allow MEDIA_RW uid to start activity
    
    Sdcard daemon, which is running with MEDIA_RW uid, need start activity
    to show dialog to users when apps try to access protected files.
    
    Change-Id: Iac1efb862e9579d3f59786c57cf18fe6518ce87b

commit d2a5e2f6bfc6297a419fd113f8adcdcbdd925807
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Wed Feb 11 11:40:51 2015 +0800

    RP: Notification and ringtone can't be overlaid by carrier
    
    There are some logic error for ringtone and notification
    overlay when sound customized. Reconstruct these code to
    make it overlay the right ringtone and notification.
    
    Change-Id: I0fd0abfe833c7920bf3ce6829998b92644eae48c
    CRs-Fixed: 761741

commit 7cba896938a0984dd673ecf4581963a1c3d4f898
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Mon Jan 19 10:26:05 2015 +0800

    MMS: Fix the edit options menu disappear after click edit button
    
    It should not check if the PopupWindow is not showing before hide
    the PopupWindow.
    
    It should check if the PopupWindow is showing before hide PopupWindow.
    
    CRs-Fixed: 778105
    
    Change-Id: I80fe49c270ca3ba4d6c22c6aa32408826ff3ac5c

commit c338a9928cf72618084d8a6ee61cf3f0ba22088c
Author: Matt Garnes <matt@cyngn.com>
Date:   Wed Feb 11 18:37:57 2015 -0800

    Do not play the default ringtone if it cannot be retrieved.
    
    In performAuditoryFeedbackForAccessibilityIfNeed() if the default
    ringtone cannot be retrieved, do not try to set the stream or play it.
    
    TODO: Find the invalid condition that caused this scenario to occur in the first place.
    
    Change-Id: I79d00e016fc07e66f32723c49090a2098163f905

commit c66239ee7f298b93b97cb257ca2ff25e0f01f21c
Author: Pan Fang <fangpan@codeaurora.org>
Date:   Thu Mar 5 15:40:47 2015 +0800

     WindowManager: remove freezing window to fix UI freezing issue
    
     In some corner case, some window is at exiting state, but can't be
     removed. This will result the windownmanger fall into freezing state.
     The fix will remove this exiting window when encounter this case.
    
    CRs-Fixed: 803491
    Change-Id: I8ba72ab0566e9d13a0405be1fa4472f826d0af50

commit 896f7498c218239e465248ed62af43d148d14c9a
Author: laufersteppenwolf <laufersteppenwolf@gmail.com>
Date:   Mon Jan 5 21:33:19 2015 +0100

    Fix GPS for old GPS HALs
    
    Some old GPS HALs like the one on the Optimus 4x HD are broken without this
    and can also cause bootloops (like on the 4x HD).
    To enable this just add the following to your config.xml overlay:
    
    <bool name="config_legacyGpsHAL">true</bool>
    
    Change-Id: I3108d9f1baf728132f048ddba846d3db96173ec7

commit ecfcaf903552b3fb17b4800940bdba6aaa903df3
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Thu Mar 19 01:11:55 2015 +0800

    Fix no vibration during shutdown.
    
    In ShutdownThread:rebootOrShutdown, the vibrator is created
    by "new SystemVibrator()" which will use default constructor
    of Vibrator.
    
    And because system server is not bound application,
    ActivityThread.currentPackageName will be null.
    Then the member mPackageName of Vibrator is null.
    
    When doing vibration:
    VibratorService.startVibrationLocked
     -> mAppOpsService.startOperation
     -> getOpsLocked (null package will get null op)
     -> return MODE_ERRORED
     -> no vibration
    
    https://code.google.com/p/android/issues/detail?id=160830
    
    Pass null context in SystemServer.performPendingShutdown
    because vibrator service is not ready, and from the call
    sequence, there is no available context to use.
    
    Change-Id: I3e0175ba6dc2e1a92787873eda4461fba6e89783

commit 973c4fea609a447146361464f308cdee7c0f4785
Author: Alan Viverette <alanv@google.com>
Date:   Tue Apr 28 17:30:04 2015 -0700

    Adjust display inversion matrix to account for luminance
    
    Bug: 20346301
    Change-Id: I10633705f2bfddbdeec063f9489a4f8679b9e8ee
    (cherry picked from commit 6437518061fc8718590e0272ed17ea64710d2299)

commit dd54db4e9e334f9383d99b82bd3bcdbf2ea10e05
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 28 10:54:52 2015 -0600

    Add missing/needed lines for TRDS
    
    - These fixes were pulled from KK as we had theme engine and TRDS then.
    
    Change-Id: Id8eaa485937e8b28a7a52eabae4044ba371897db

commit 40585e2b027c96d2d75e32d7bc873068a199c891
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 10:35:34 2015 -0700

    Revert :Fix Ambient Display tile (reverted from commit 4b3d10b0dde9ad2a8a966ef155f18939f2d0f4b9)

commit bcd58eb7dd65d2bbf4752ea540f64865f49a37a1
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 10:36:53 2015 -0700

    Revert: QS: add Ambient display tile
    
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
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java (reverted from commit 4706d9cb18e8299c0fd89cba02c914ddc8ce90e7)

commit 9b17edbf1baf5c16dedfd815a1f86890f6e8a902
Author: Noeljunior <liamgliam@gmail.com>
Date:   Fri May 1 18:29:51 2015 -0700

    QS: Add Ambient Display Tile (1/2)
    
    Change-Id: I31ffd7d83a65db294759374900da0fca1c760549
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/cm_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 2509ae63d08c65995ec2bd0b8d994477d05bb4ae
Author: rogersb11 <brettrogers11@gmail.com>
Date:   Fri May 1 17:54:40 2015 -0700

    Add back TRDS Tile now 1/2
    
    Quick fix, at the time of the original commits it was easier to just come back to this
    
    Change-Id: I439f6e40a6b6a9b6d7a861496a10b8d7cc4a7c34
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 947692b335e3db4166fb205ebc448383a9a0219b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 10:43:36 2015 -0700

    Revert "MMS (change 1 of 2): Add DATA_PROFILE_MMS constant = 5 to RILConstants."
    
    This reverts commit 802e7455d7b390fbcf29c999a26d41d85f959395.

commit daf6b73a4f64f8183e71be8453f2488f2e3d3998
Author: Shaun Eaton <shaunsibu@gmail.com>
Date:   Fri May 1 00:31:28 2015 -0600

    Add missing line to update NavBar upon theme change.
    
    Change-Id: I31bdbda8eb98c89c2dec0e2daa5434bf8eb46b5b

commit b6c90fae3c885e33fd01ebcd243f9b65ccfa0e20
Author: Connor Tumbleson <connor.tumbleson@gmail.com>
Date:   Wed Nov 5 07:24:08 2014 -0600

    iBotPeaches aapt changes for lollipop
    
    Change-Id: Ia2e8609692b43cc9df9ab24f24866662404b34d5

commit dde4cef9f903adbe936eb3a2c50c00f8b1082deb
Author: Jean-Luc Brouillet <jeanluc@google.com>
Date:   Fri Apr 24 15:59:02 2015 -0700

    Overhaul of the RenderScript reference documentation.
    
    This CL replaces the Doxygen generated documentation by one that's created
    by our internal tool found in framework/rs/api.  The big advantages:
    
    - Can handle overloaded functions.  Doxygen could not and RenderScript has many.
    - Can have version information.
    - Can match the look of the Java documentation.
    - Cleaner look and no leaking of internal paths.
    
    This CL also include changes introduced by the L release which was missing
    previously.
    
    Change-Id: I5ff712cb6dc9993a93cb3c356602825fdfc8d81e

commit e5c22a5594b1356cbb04b344fa7b69f6d0bbaa5e
Author: 0xD34D <clark@scheffsblend.com>
Date:   Fri May 1 17:26:02 2015 -0700

    Identicons: Add identicons to ChaOS Lab [1/3]
    
    Change-Id: Ie0ffc4a4c2a41d6a5f35aad761c4c17a725bbc2a
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit a29d20c393f684b8744652d15ab6c9c788cb1a9f
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 20:57:09 2015 -0700

    Revert: Revert: App sidebar: some adjustments
    - Cleanup
    - fix disappearing appbar on changing appbar position
    - may fix endless FC on changing appbar contents
    
    Change-Id: I2e94290dc128447f0da8937eb5dc0ed10296a155
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java (reverted from commit 8a71a12daa5d4d5e19dbfe4257b4083053ec3ca3) (reverted from commit 5e5cef254474a64db7dcf3f2d480942fb614770a)

commit 1f06ed74d18ed820ace1c6e8da3876a49094fea9
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 20:57:21 2015 -0700

    Revert : Revert: App sidebar: notify if app is not installed
    
    better than force close
    
    Change-Id: I9eebe1a3a4be2dad16ed9a8cff9c0694900d833d (reverted from commit 988d73b0b2e47c5c9bce8428cffd3d9004b97f3a) (reverted from commit ec575a1de0f27bbff360ee6ced08575b710ac0d0)

commit 399fd8b1f7c51b45c6393f079046eac670badac4
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Mar 19 14:32:33 2015 -0700

    SystemUI: small optimization for notification icon numbers
    
    Don't create the paint object used to draw notification icon count
    badges in the status bar unless the user actually wants to see those
    counts.
    
    Change-Id: Iabba316102583a798acdc124d9fb51c0d7826a0d
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 9737d028d638c2f33566cfcfe2ba7ffb5d1817d6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:50:39 2015 +0300

    Automatic translation import
    
    Change-Id: I3936018c255cec208050fce2f24d658ba8f69bbb

commit af36d46ebaf165dd772d0be13b03170fba590458
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Tue Nov 18 20:28:11 2014 +0100

    (1/2) Base: instant reboot action trigger
    
    Change-Id: If32b4fb898866a3064443074344e8ea494ec5ff7
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit 5861ba386cc9c648865ff444932bc4e1e2239035
Author: LuK1337 <priv.luk@gmail.com>
Date:   Sat May 2 19:09:41 2015 +0200

    SystemUI: Use smaller battery padding
    
    Change-Id: I70ee56d3281ea7e8cf0380824784d2c2cee4b021

commit 68fb921d48f4f86f6481e8675e269590989098eb
Author: Rajshekar Eashwarappa <reashw@codeaurora.org>
Date:   Thu Nov 7 12:34:24 2013 +0530

    framework:Thread synchronization for UI update
    
    Issue : Framework reboot was observed due to out of sync between
            two threads which inturn causes Null pointer exception
            while updating airplanemode.
    Fix : Handled Null pointer exception and the crash is not observed.
    CRs-Fixed: 570122
    
    Change-Id: I2e969f6e7726ffcf8648b366ebb54cb2b0afc292

commit c53dd31934075c8ae99135d0faa510d0dfffbb24
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 00:57:39 2015 -0700

    Revert "AudioManager: update references to application context"
    This reverts commit 8a366a1.

commit 9ea79a257e2bf499ff67e99f50123a02b364c706
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 00:58:00 2015 -0700

    Revert "Sometimes the application context is null"
    
    This reverts commit e6713e6a88ecef4fbbbd511122cb17946eb69896.

commit 7111135c76f9aa186444cd4b763897f8a809f720
Author: Marco Nelissen <marcone@google.com>
Date:   Fri Apr 17 09:50:56 2015 -0700

    Sometimes the application context is null
    
    when called from systemui.
    
    Bug: https://code.google.com/p/android/issues/detail?id=152173
    Change-Id: I27153a48d7edce7006517507d813e24ce6f63a7d

commit f703c040a5bc0fc7a73196160bef92f876b176c4
Author: Mathieu Chartier <mathieuc@google.com>
Date:   Fri May 1 11:30:22 2015 -0700

    Look at map extensions before /dev/ + ashmem.
    
    Prevents stuff like:
    dalvik-classes.dex appearing as GC overhead.
    
    (cherry picked from commit 9308462a5972192a1ad9abd01b36e1ad545eef99)
    
    Bug: 20752953
    Change-Id: Iab0935e882a5d938651ec2581845d8242aaf98af

commit e9af3e17f2380f091af9da060d2d86c3b843f4d2
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Tue Apr 21 15:51:13 2015 +0200

    AudioManager: update references to application context
    
    Change-Id: If458c17c44bc68f1a0c4172b11240e2053fad42e
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit 1554d3ef38ce2148f165805b908012637f893566
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Fri May 1 01:52:58 2015 +0800

    Fix NPE in JobServiceContext when closing job.
    
    Disconnect may come after job is canceled.
    Add a finished state to avoid cleanup finished job again.
    
    Real case:
    http://code.google.com/p/android/issues/detail?id=170814
    
    * CP from here:
    https://github.com/android/platform_frameworks_base/commit/6a94aba734b0dffedeb1744bdbe59341760b56b6
    
    Change-Id: I9c7a1b944a8393e30396f473ebeb8332e51f21f1

commit f4c96230fd5e1b99701cc737251348a804d707e1
Author: abun880007 <tigger2014@team-ub.co.uk>
Date:   Sun Apr 5 18:48:14 2015 +0100

    Fix showing heads up if IME is showing

commit d48b0f1019d26546a85506c57a6bd00976f8ad52
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Fri May 1 06:15:47 2015 -0400

    ambient display: Fix volume key music control
    
    Previously the dream service would only report whether or not it was dreaming.
    Ambient display counts as dreaming.  When dreaming, the volume inputs are
    passed back to the application which is not what we want for ambient
    display.
    
    Fix this by exposing isDozing() and allow volume keys to control music
    when we are dreaming and have moved into doze mode (aka, sleeping).
    
    Change-Id: I508c86668bc62c47acd0fc6958270362464213f5

commit eae82b7a48f497c16a766a5ea581cf7b7873c0d2
Author: Mathieu Chartier <mathieuc@google.com>
Date:   Tue Apr 28 16:30:30 2015 -0700

    Properly describe exception
    
    Previously we used DetachCurrentThread which raised a SIGABRT from
    within ART. The new approach is to use ExceptionDescribe and exit.
    
    Bug: 20640601
    
    * includes fix of commit 97a29433c33f4e2c8ab60167a4be41664f56c314
    
    Change-Id: If87d9de46fde71a72ae7687f42ff1de182f651bd

commit d0dd78363731bc02cf09279b0369f563924ac404
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 00:59:49 2015 -0700

    Revert "SystemUI: small optimization for notification icon numbers"
    
    This reverts commit 177abf951bd74f5d4dbdd13c0aff6bacbcbd5869.

commit 9c99037df5f3791000ec3e2de6e662b29ac635cb
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 01:48:07 2015 -0700

    AppSideBar Tile 2/2
    
    Drawables stolen from bliss(thanks) and modified by @TheGeekyNimrod
    
    Conflicts:
    	packages/SystemUI/res/values/cyanide_strings.xml

commit ac4ec52fa5636166bf60f09d8704004ddb3496e8
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 02:00:00 2015 -0700

    [Squash] Revert: (Omni) Implement ambient display as Active Display
    
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
    	core/java/android/provider/Settings.java (reverted from commit 10bb637236b3d88bcf390401467cd420e43040ce)
    SystemUI: Update doze pulse-in option
    
    * add hardcoded stock values if using overwrite option instead of fetching them from resources
    
    Change-Id: I0765e2068e58286425adf1c1360c2c67bb1636bb
    
    Conflicts:
    
    	core/java/android/provider/Settings.java (reverted from commit 79a2f361169248c97ca7121e1f7a865e532c1edf)
    Frameworks: Add ability to control default value of DOZE_ENABLED
    
    Devices can enable the doze feature. Devices without AMODLED screens can use it
    but it will use then of course more battery. This devices should disable this feature
    by default and let the user decide to turn it on.
    
    to change the default behaviour add into device overlay
    
    config_doze_enabled_by_default and set it to false
    
    Change-Id: I1afbf1d09fa0d7e68aea40f2f165a72ff34d0040
    
    Conflicts:
    	core/res/res/values/cmr_config.xml
    	core/res/res/values/cr_symbols.xml (reverted from commit a0422c3e3e76956627dd4dd2626dca3d8b5b634f)
    doze: Do not bother checking proximity for the DOZE_ACTION intent
    
    The intent is a desire to show the intent and trust the sender to
    determine whether or not it should really be shown.
    
    Change-Id: I1c613071b136de61f12bc0556283a80e1248a4a8 (reverted from commit 80a6a21d36b367ad7e2ce49d6bf2ecb94d523913)

commit 37b64087602550917e6cf74e585aa73f097fd4b9
Author: dankoman <dankoman30@gmail.com>
Date:   Mon Feb 2 01:37:07 2015 +0100

    [2/2] Framework: Slim doze options
    
    option to turn off TriggerSensors for doze pulse (pick-up/
            significant motion sensors)
    patchset: doze schedule preference
    patchset: notification trigger preference
    patchset: split pickup gesture sensor and significant
            motion sensor triggers into two preferences
    patchset: doze brightness
    patchset: custom values to slim_config
    Change-Id: I2a1be925ac58721f12da04a6164641ffa1c4a654

commit 8cbdf0d692c30ec2944642004aea07499235abf2
Author: Uday Kiran jandhyala <ukiran@codeaurora.org>
Date:   Wed Apr 8 00:18:34 2015 +0530

    MediaSessionService: Error checks for UserRecord object
    
    Checking UserRecord object for NULL, before accessing its members
    
    Change-Id: Icf1fbbe35647a9cbc22cb4418c468c4a275db36d
    CRs-Fixed: 817083

commit fd84cbdc7ee6393b2e1c74084d92b55126444d85
Author: wangjing <wangjing@codeaurora.org>
Date:   Thu Apr 9 16:16:31 2015 +0800

    libandroidfw: Fatal exception of dlfree often causes the system crashed
    
    When the function 'getBuffer' are called at the same time by the threads,
    mZipInflater will be 'delete' twice if mZipInflater isn't NULL,
    that is 'mZipInflater = NULL' has not be reached,
    at this time it will cause system server crashed.
    
    Add AutoMutex at the beginning of the function to avoid getBuffer to
    be called at the same time.
    
    CRs-Fixed: 812950
    Change-Id: I283b43a01b97ae6a149749ff2186efda9df4dc42

commit 9b8ce89d4c09b8f51ff7be074c7e85336f2b770d
Author: 0xD34D <clark@scheffsblend.com>
Date:   Sun May 3 22:17:15 2015 -0700

    Frameworks: Gesture Lockscreen (1/2)
    
    This adds the ability to us a hand drawn gesture as
    a means to unlock the device.
    
    In the case that the gesture is forgotton or not
    being recognized correctly, the fallback will be the
    same as when using patterns.
    
    Androidx:
    Some changes needed for 5.0
    
    pimpmaneaton:
    Some changes needed for 5.1
    
    Change-Id: Iedaed283bfc317d4b14f21bad6fca1a3ffd4a190
    
    Conflicts:
    	core/java/android/gesture/GestureOverlayView.java
    	core/java/com/android/internal/widget/LockPatternUtils.java
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit f85843c76d65738572d6a5f62110a129fb566808
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon May 4 09:53:35 2015 +0800

    Add missing boolean for gesture

project frameworks/native/
commit 5ac19fa6c9a52bc1a97c66feda0f84e2ccd92017
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Sat Dec 14 02:58:19 2013 +0100

    native: TRDS 5.0 (2/4)
    
    Change-Id: Ibc5aaec5661455477815043440fae86052a395ce

project frameworks/opt/telephony/
commit ce6bd446dfdb2dec08629b55d7b6507d5168da06
Merge: d4df7d2 d61a188
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 19:22:33 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 6d2524626b7e006425ed23d757b4a6b11cc631f2
Author: maxwen <max.weninger@gmail.com>
Date:   Wed Apr 15 23:30:24 2015 +0200

    telephony: kill IccSmsInterfaceManager log spam
    
    Change-Id: I11aba1edb5af50ccd769f6102875ab09e2895d5f

commit e2199ed78f186bf15f6445e2ea945f3a3705daf9
Author: Patrick Lower <devvortex@gmail.com>
Date:   Wed Apr 29 15:31:29 2015 -0400

    MMS (change 2 of 2): Update apnProfileID for MMS only apn.
    
    Depends on: http://review.cyanogenmod.org/#/c/96582/
    
    Change-Id: I3dfaddc6d4a0ee581f98e9290d4593b79cd3b2c6
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/96584/

commit b80262ae92bac56c7bc51608847aff17d14f1055
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 12:55:23 2015 -0700

    Revert: MMS (change 2 of 2): Update apnProfileID for MMS only apn.
    
    Depends on: http://review.cyanogenmod.org/#/c/96582/
    
    Change-Id: I3dfaddc6d4a0ee581f98e9290d4593b79cd3b2c6
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/96584/ (reverted from commit e2199ed78f186bf15f6445e2ea945f3a3705daf9)

commit e7f37ae69e24b79aa4b3ccf70b04c4041fd67544
Merge: b80262a b9bf02b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:35:03 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project hardware/qcom/media-caf/msm8994/
commit 9ab05267739628b900c78e178094f3a2fb0812b2
Author: Scott Mertz <scott@cyngn.com>
Date:   Wed Apr 29 10:54:13 2015 -0700

    vidc: add dependency on kernel headers
    
    Change-Id: Ie9f8ffc1b82e98f315d76cc3b786a2d03621cb7b

project kernel/samsung/trlte/
commit d8c4c105e4ae46a2a35b8f2436949ef09b8d51a6
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 00:53:53 2015 -0700

    msm cpu frequency limit (faux123)
    
    Change-Id: I043247aee52cfb78a4b6994787651981d530e27b

commit 6bbede27c04735cf2c3e9a5bb23e1102454c961e
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 20:10:52 2015 -0700

    readjust hardlimit
    
    Change-Id: I5fad4906c35f1d660d52e211247a9cf5d868e451

commit a28384a0831c08ef234fac1a5f28500614f6cbc7
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 11:25:24 2015 -0700

    Revert: Add variant detection
    
    (cherry picked from commit 6f8b4fc3e15b20e48667f9e7ecc8e580e5e87f0d) (reverted from commit 53a4e10f39d8522c0d0f1ce1a8ce3d5901f7bb3c)
    
    Change-Id: I9f0edc0c870a2f33d51aef4457917b19bd341d5f

commit 67cacfe15a847ae5c8de17344c36eb22f49655b5
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 15:06:39 2015 -0700

    Sweep2Wake & doubletap2wake : v1.7 & support for powersuspend [showp1984]
    
    4. Disable by default [UpInTheAir]
    
    3. Fix Sweep2Wake Early Suspend handling [LoungeKatt]
    LCD Notify was mixed in with the latest update and handled incorrectly.
    Removes LCD Notify and fixes Early Suspend.
    
    2. Update Sweep2Sleep [Dorimanx]
    
    1. Sweep2Wake: v1.5 & support for powersuspend [showp1984]
    
    fixed DT2W buidl error
    
    Change-Id: Idd7a174450f6f8724fb2a255da78cadb99c39559

commit bd9d9842471345bbed1173b29945a2582b25d80d
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 16:28:03 2015 -0700

    quick wakeup
    
    Change-Id: Ia6df25b3c0a1b55e5474d77e4c7e7b95703df930

commit 6105de0c4cb32106f6f587cc05af1eeb289d3cde
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 16:39:56 2015 -0700

    msm: mdss: Adding lcd notifier
    
    Change-Id: I3dc3c84397f165b000ffc6e1c6f1b9e75c77bcdc

commit 756ee8df601b07bbdfea0297bb9329daf155ef88
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 21:41:44 2015 -0700

    Revert: Intelliplug on by default (reverted from commit c38f7fa51d4fb7c8523031e88946c161c2a57deb)
    
    Change-Id: Ic2413f8653553cad0d3494f3126cf27153cd84e9

commit 2bdce6ab2f4b14103236229859c91701142ae1bf
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 22:16:15 2015 -0700

    disabled yank555 hardlimit
    
    Change-Id: Ie95ec983824c78c96b20e6a2d7dab1748c6a09d0

project packages/apps/AudioFX/
commit b2e8ba3988af3a617fe22180ac1ba7eb2ed7a5cc
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:50:51 2015 +0300

    Automatic translation import
    
    Change-Id: I454177ba7ad1a9998a3d51ead392a11715227854

project packages/apps/Bluetooth/
commit 55b636ceda90d5c7a0e9fd3ddbb3eba0f0447043
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:50:56 2015 +0300

    Automatic translation import
    
    Change-Id: I35504d3a4915d2369d1620d0d58953ade71c49a4

project packages/apps/BluetoothExt/
commit 499ae4e6a5bfff20f2b32a5152a666917a29c4c9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:02 2015 +0300

    Automatic translation import
    
    Change-Id: Ibabb1f02cb1aa7d1dbc84a4f1c6441d4ef9b0994

project packages/apps/CMFileManager/
commit bd68f575327b3a1fde2ce4be83c0f837355d9be1
Author: kai.cao <kai.cao@ck-telecom.com>
Date:   Wed Apr 29 15:42:14 2015 +0800

    [CMFileManager]Fix click two times when check the 'Skip media scan' in Secure storage
    
    Procedures
    
    1.Go to “File Manager”.
    2.Enter the secure directory and Press the menu button.
    3.Press the Properties item.
    4.Check the media scan.
    
    Pop "Failed to prevent media scanning" and should click again.
    
    Change-Id: I7990683e373c05fdfcee47bf5189820206bceba5

commit 4a6769ccfb0b8b856512c4eca5bcf7f14fccad09
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:38 2015 +0300

    Automatic translation import
    
    Change-Id: Idfda3b4193c7a08f921890ffa174ccb0d23204c1

project packages/apps/CMWallpapers/
commit b8672b780aef7300af07629bc58b50be5749ca48
Author: d34d <clark@cyngn.com>
Date:   Tue Apr 28 15:16:43 2015 -0700

    Add back no wallpaper option
    
    Change-Id: I66469489973af60dbb601324e1bcc89d22b063f3

commit 40367a7e9400a526dc8dad84fdac9be069b623ef
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:51 2015 +0300

    Automatic translation import
    
    Change-Id: I8fc6afa2581e4535b57c7b6cbb589af9e4550ae7

project packages/apps/Calculator/
commit d3c9ae2f1e85e4c0318726846b027d97ea1b2162
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Apr 28 16:14:18 2015 -0700

    Calculator: allow for negative numbers after operation characters
    
    Repro:
     - Enter the following eq: 10^-3
     - Observe that enter '-' after '^' causes replacement
    
    This patch allows the minus operator to appear after an operator
    *unless* it's two successive minus operators.
    
    Change-Id: I929530471e2287e97d2cacac91a61cea53bf7568
    (cherry picked from commit 85e7f93d7156e573d48c622bb40f3429704351b3)

commit df90b7b5607bf243b70cbaa38f98765e15358ab3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:06 2015 +0300

    Automatic translation import
    
    Change-Id: I2f3189a8b6e1d8544c924eca1b4e9a8c5aad6b4e

project packages/apps/Calendar/
commit 113041abc31987402341b4cfc0f499fd8d7811c4
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:14 2015 +0300

    Automatic translation import
    
    Change-Id: Ia2f1a08c62c801d6bcf2d8fb7b1af58e293c6d20

project packages/apps/Camera2/
commit 6403559e01c695db50b50d52a1623e5c28ff5a08
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:20 2015 +0300

    Automatic translation import
    
    Change-Id: I85cda76936f8317f427828a9b9f951205c1ced60

commit cc104444c49d2f418efa3e11b140afff184cd8a3
Merge: 6ab7ff4 6403559
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:38:51 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/CellBroadcastReceiver/
commit 0bcdeed48a14c0152f11a664ce3f6e5be59d24f3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:25 2015 +0300

    Automatic translation import
    
    Change-Id: I917ad2fd2d0a97cc95bd87555d9fe3b2cec0bc02

project packages/apps/Contacts/
commit 90326933c20e115c4b9118853b7d4062b32de0a5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:55 2015 +0300

    Automatic translation import
    
    Change-Id: I826aa3b7be9b14cab7480ef00f53558213b6e243

project packages/apps/ContactsCommon/
commit a942c97b9d2e4d88f2c0e8e5ea8f47b02d2681d7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:51:59 2015 +0300

    Automatic translation import
    
    Change-Id: I5ecc5bf919466a36d5a8699b17df9fd9919f994c

project packages/apps/DeskClock/
commit be06b1a2e01f9d5f0caf6cbd1dbd42f9805befae
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:03 2015 +0300

    Automatic translation import
    
    Change-Id: Ie08388de6681960f659eac36e9d121f0d9a7050f

project packages/apps/Dialer/
commit 0c1b9eaef7715981b11cfb816c1a50e716727672
Merge: 8951136 c2b9149
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 19:28:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.1' into cm-12.1

commit c2a0cde07dd316532f3998dfd8aba8e068f031f1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:08 2015 +0300

    Automatic translation import
    
    Change-Id: I302e5509b426798d2d6436313c8d5a6e75b9a969

commit 0c75852de30eecf2d4bd028f5a409432e85498e9
Merge: 0c1b9ea c2a0cde
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:40:08 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.1' into cm-12.1

project packages/apps/Eleven/
commit a02bc80dd6a52555b8dc0801acaf4893bbe295f9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:14 2015 +0300

    Automatic translation import
    
    Change-Id: Ib44ae71a0eaef8df5c473639746083c4800b67da

project packages/apps/Email/
commit a348e9a488871fa68f7f3829750c36a0b5a53d99
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Apr 20 04:16:04 2015 +0200

    email: custom notification lights
    
    Change-Id: I3aaed3c682ae33da925316a5b9a586796fe71229
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 0f4610bfccb3b5d0b93536b1f2bb344e8fe23dae
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Fri May 1 22:05:03 2015 +0200

    email: fix Account table creation
    
    Due to a bug in commit 44a064e5f16ddaac25f2acfc03c118f65bc48aec,
    AUTO_FETCH_ATTACHMENTS column could not be available in the Account table.
    Since cm12 and up doesn't use this column, we are leave as is it. In case
    the feature were added, then we need to create a new exception to ensure
    that the columns is re-added.
    
    Change-Id: I1803e343dde2e841fdc99b4489a74eb08b0a8352
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 8ca2f36efc37ee57af19c53cbb70b0078179cecf
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:21 2015 +0300

    Automatic translation import
    
    Change-Id: I1a364a4b794a8228155dc1dbb8758eed15ac4ea5

commit 41e69947f0b43b8569b29b2518dc7bc652cda7c0
Merge: 108dfdc 8ca2f36
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:40:33 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/InCallUI/
commit b3e301024b62373bb57e503f25d27e0d2fcc83c2
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 28 20:40:29 2015 +0100

    InCallUI: Add a controller for in-call proximity sensor (2/3)
    
    follow up to this patch
    https://github.com/Euphoria-OS/android_packages_apps_InCallUI/commit/9cc23a9201b7580b0cbb6018ba62b0b06b8f1651
    
    Change-Id: If3d581486c5776b1d030e1087bdf664be468115a

commit 068cee8dcad16d63bb000bef0534d40cd5309f0c
Author: Yorke Lee <yorkelee@google.com>
Date:   Mon Mar 30 12:31:19 2015 -0700

    Don't hide end call button until call is disconnected
    
    Currently, the end call button is hidden the moment the user
    initates a hangup. In the event that the call is not actually
    disconnected, the UI is stuck in a "Hanging up" state that is
    unresponsive
    
    For the majority of calls that disconnect correctly, there should
    be no user-perceptible difference in behavior. For calls that are
    not disconnected correctly, the end call button will remain showing
    so that hangup commands can continue to be sent that will eventually
    disconnect the call correctly.
    
    Bug: 19933863
    Change-Id: I2ff2018d7d229615f5f57c599f74954ec7492f6b

commit c3362b5b996d8d3a0066d61f1d1e33e21577117d
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:31 2015 +0300

    Automatic translation import
    
    Change-Id: I391f335df39c3ea13eacfb7b23f8704ed586da56

commit a26c222e4f546e0e7bfe6f034ab72c27d8613b97
Merge: 068cee8 c3362b5
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:41:42 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1
    
     longer uses CallCommandClient
    
    Patchset: add time delay preference
    
    Patchset: remove callback if audio mode changed before runnable
            had a chance to run
    
    Patchset: remove callback onStateChange
    
    Patchset: formatting
    Change-Id: I5ffaca0eb2e905abb36bbc298416742055acacb8
    
    Conflicts:
    	src/com/android/incallui/ProximitySensor.java
    
    Conflicts:
    	src/com/android/incallui/ProximitySensor.java

project packages/apps/KernelAdiutor/
commit ff7b88e3a45ad4186f5a019cfe0fb3dc1c7737a1
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 28 00:03:08 2015 +0200

    version 0.9.3.1.1 beta

commit 7ffd04ad66026d4b51c0bfbee1f9bceb20c78855
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 28 21:10:44 2015 +0200

    Fix gamma profiles not showing up
    and add a wakelock section in misc

commit 5da0f384d74bba5e64a08b4fd1820f81891841c0
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 28 21:20:21 2015 +0200

    version 0.9.3.1.2 beta

commit 6dcb4e63bb8fbe115b23d3ab5a543bd429f2d002
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Tue Apr 28 22:23:53 2015 +0200

    Bump version to 0.9.3.1.2
    
    Change-Id: I2c84d4abc4f31870b9285b43b001709fe51e16e2

project packages/apps/LockClock/
commit fafa209b5802162aa4b0062e587b68ff83b79083
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:37 2015 +0300

    Automatic translation import
    
    Change-Id: I2572d734c1d2e434384b8ea79e87201381e2dfa1

project packages/apps/Mms/
commit 183af12250aa0fb61f1b0aad749cd5efa8e667bf
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:41 2015 +0300

    Automatic translation import
    
    Change-Id: Iacd2af99191cc33de5c1eda93e7e8a7642e35e43

commit ed928b4b3502e4f2f66e0603b3676c27adb6bd57
Merge: 1f3ff02 183af12
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:43:04 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/PhoneCommon/
commit c703c7c5c08f64e7d17531ba1e302f9cce094876
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:48 2015 +0300

    Automatic translation import
    
    Change-Id: I28325cf53a1a68efac1e6ee3389936d188820043

project packages/apps/Settings/
commit 0f3e87bfefb6c73e9284028280659800f1a5a955
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Apr 28 01:49:05 2015 -0700

    Saberize > update to be inline with SaberMod
    
    Change-Id: Ic69016fb27fded392215f4f20c2fe6f24f065645
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Added SaberMod Android banner in About Phone
    
    Change-Id: Id23a1ac74b4a5eac0d2f57479780eb2d0e97de68
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	res/drawable-hdpi/smbanner.png
    	res/layout/smbanner_row.xml
    	res/xml/device_info_settings.xml
    	src/com/android/settings/DeviceInfoSettings.java

commit 50ce5f2eaf29632bb809a511725c3be1419cc776
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Tue Apr 28 03:17:31 2015 -0700

    Settings: TRDS 5.0 (4/4)
    
    patchset: add holodark resources
    
    patchset: fix up switch preference
    
    patchset: add to slim actions
    
    patchset: some tweaks and fixes
    
    patchset: Action instead of SlimActions
    
    patchset: fix icon
    
    patchset: remove holodark resources
    
    patchset: add darktheme resources
    
    patchset: light sensor is experimental
    
    patchset: themeenabler uses onpreferenceclicklistener instead
            of onpreferencechangelistener
    
    patchset: add reset dialog (to reset to default theme)
    Change-Id: I5b857c542d92b9fd253b3556f14c790226594c4f
    
    Conflicts:
    	res/values/cmr_arrays.xml
    	res/values/cmr_strings.xml
    	res/xml/dashboard_categories.xml

commit 56efa7ed4cb15e06bc107beed3d15e8b85c8616b
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Mon Feb 10 23:24:51 2014 +0100

    Settings: SlimPie give user ability to reduce trigger heights if IME keyboard shows (2/2)
    
    Add a user option to reduce left and right trigger of SlimPie if keyboard shows up
    (especially usefull for swipe keyboard which most keyboards are nowadays). Enabled
    by default user can disable it in settings
    
    PS:
    - fix category string
    
    Change-Id: Ia5ae621a5e63b2efd10180cfbe1876b14a63c866

commit 7487e9474d3792da242d32c9be457f2447adeb5b
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Tue Apr 28 13:47:21 2015 -0700

    SlimPIE: Configurable sensitivity [2/2]
    
    Change-Id: I7afc315bbf922f7f5ff3ba93cca38bfcd359f0ab
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>
    
    Conflicts:
    	res/values/cr_strings.xml

commit bdcd1b031465a9b9b14eb531d48b47f22187574f
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 03:28:08 2015 -0700

    Revert Settings: use correct default value for backlight brightness

commit 07efc1e7cb10b6909a1569f8efa7b018a79a34ed
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 14:08:14 2015 -0700

    add SeekBarPreferenceCHOS.java

commit 99e9d858ba635c65a3c71e7b44a107340cbff12e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 14:18:48 2015 -0700

    add icon for new changelog option

commit 6ffd0ef2da05a3fef76f87e1f7308a9be580142e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 14:25:54 2015 -0700

    reoganized slim trds

commit 87e1c5002176bbb6c6148a71c8ba06d39ccfe682
Author: Janson Kang <temasek71@gmail.com>
Date:   Wed Apr 29 21:55:12 2015 -0700

    Fix breathing sms/misscall/voicemail + add mobile check
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/status_bar_settings.xml

commit 1d99a053e21610a4f900481ece62016bb43955c2
Author: Utkarsh Gupta <utkarsh.eminem@gmail.com>
Date:   Wed Apr 1 00:00:00 2015 +0000

    [2/2] Battery light: 100% charged level

commit 3779f65aadefd97a8288859a27147304ba679774
Author: Utkarsh Gupta <utkarsh.eminem@gmail.com>
Date:   Wed Apr 1 00:00:00 2015 +0000

    Allow restricted profiles on phones

commit 7354ab876592d840eba37c3a3d355bc59295d3ae
Author: Utkarsh Gupta <utkarsh.eminem@gmail.com>
Date:   Wed Apr 1 00:00:00 2015 +0000

    Re-enable CPU governor & min/max freq settings

commit d23c677e4a50d8dfb0833c0c6417defe2d6f1e43
Author: Janson Kang <temasek71@gmail.com>
Date:   Wed Apr 29 15:03:27 2015 +0800

    Update PIE Control

commit f41f19f5bb79886ef6e1d8e0aefec5de9caa16a1
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Sun Mar 1 19:15:34 2015 +0000

    Display settings: show enabled/disabled summary for ambient display
    Change-Id: I97aee7aafd69f3e60d2c518aa514a7cd1dff9ecf
    
    Conflicts:
    	res/values/custom_strings.xml

commit 3a9299f4bc2a6279a06e247bceb7475ee3d6f0bc
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Apr 29 21:37:19 2015 -0700

    Display settings: remove ambient display screen when advanced mode is disabled
    
    now when advanced mode is disabled ambient display will be a simple switch preference
    
    Change-Id: Ia50897590b56a7d295255828da3d62e9535c0c60
    
    Conflicts:
    
    	res/xml/display.xml
    	src/com/android/settings/DisplaySettings.java
    
    Conflicts:
    	res/xml/display.xml

commit 02d9731e7d55eec9b6b202956931b02564f4a924
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 30 10:30:58 2015 -0700

    Optimize Settings png's
    
    Change-Id: I70b309c97e924b88267bca6b74e0ccbc3f172637
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	res/drawable-hdpi/ic_power_system.png
    	res/drawable-hdpi/ic_settings_cell_standby.png
    	res/drawable-hdpi/ic_settings_phone_idle.png
    	res/drawable-hdpi/ic_settings_voice_calls.png
    	res/drawable-hdpi/ic_sync_anim_holo.png
    	res/drawable-hdpi/ic_sync_error_holo.png
    	res/drawable-hdpi/ic_sync_grey_holo.png
    	res/drawable-hdpi/ic_wps_dark.png
    	res/drawable-hdpi/ic_wps_light.png
    	res/drawable-hdpi/nfc_payment_empty_state.png
    	res/drawable-mdpi/ic_bt_network_pan.png
    	res/drawable-mdpi/ic_power_system.png
    	res/drawable-mdpi/ic_settings_cell_standby.png
    	res/drawable-mdpi/ic_settings_phone_idle.png
    	res/drawable-mdpi/ic_settings_voice_calls.png
    	res/drawable-mdpi/ic_sync_anim_holo.png
    	res/drawable-mdpi/ic_sync_error_holo.png
    	res/drawable-mdpi/ic_sync_grey_holo.png
    	res/drawable-mdpi/ic_wps_dark.png
    	res/drawable-mdpi/ic_wps_light.png
    	res/drawable-mdpi/nfc_payment_empty_state.png
    	res/drawable-xhdpi/ic_bt_network_pan.png
    	res/drawable-xhdpi/ic_item_delete.png
    	res/drawable-xhdpi/ic_power_system.png
    	res/drawable-xhdpi/ic_settings_cell_standby.png
    	res/drawable-xhdpi/ic_settings_phone_idle.png
    	res/drawable-xhdpi/ic_settings_voice_calls.png
    	res/drawable-xhdpi/ic_sync_anim_holo.png
    	res/drawable-xhdpi/ic_sync_error_holo.png
    	res/drawable-xhdpi/ic_sync_grey_holo.png
    	res/drawable-xhdpi/ic_tab_selected_download.png
    	res/drawable-xhdpi/ic_tab_selected_running.png
    	res/drawable-xhdpi/ic_wps_dark.png
    	res/drawable-xhdpi/ic_wps_light.png
    	res/drawable-xhdpi/nfc_payment_empty_state.png
    	res/drawable-xxhdpi/ic_bt_network_pan.png
    	res/drawable-xxhdpi/ic_item_delete.png
    	res/drawable-xxhdpi/ic_power_system.png
    	res/drawable-xxhdpi/ic_settings_cell_standby.png
    	res/drawable-xxhdpi/ic_settings_phone_idle.png
    	res/drawable-xxhdpi/ic_settings_voice_calls.png
    	res/drawable-xxhdpi/ic_sync_anim_holo.png
    	res/drawable-xxhdpi/ic_sync_error_holo.png
    	res/drawable-xxhdpi/ic_sync_grey_holo.png
    	res/drawable-xxhdpi/ic_tab_selected_download.png
    	res/drawable-xxhdpi/ic_tab_selected_running.png
    	res/drawable-xxhdpi/ic_wps_dark.png
    	res/drawable-xxhdpi/ic_wps_light.png
    	res/drawable-xxhdpi/nfc_payment_empty_state.png
    	res/drawable-xxxhdpi/ic_bt_network_pan.png
    	res/drawable-xxxhdpi/ic_power_system.png
    	res/drawable-xxxhdpi/ic_settings_phone_idle.png
    	res/drawable-xxxhdpi/ic_sync_anim_holo.png
    	res/drawable-xxxhdpi/ic_sync_error_holo.png
    	res/drawable-xxxhdpi/ic_sync_grey_holo.png
    	res/drawable-xxxhdpi/ic_tab_selected_download.png
    	res/drawable-xxxhdpi/ic_tab_selected_running.png
    	res/drawable-xxxhdpi/nfc_payment_empty_state.png

commit 0b39c4336d5199dda88f460f1f026bb171201498
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 30 10:32:34 2015 -0700

    Remove extra kernel gcc version info (1/2)
    
    No longer needed with 9590f426e7986e64d68ae80b4ac5c6409f4c88b5
    
    Change-Id: Idd694e9616fa9875aa3911e58ec8a4e526423c0b
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	res/values-eu-rES/cm_plurals.xml

commit 9e0dcced98f3deaff0fb5d23a2895246703889d6
Author: Shaun Eaton <shaunsibu@gmail.com>
Date:   Mon Apr 27 22:53:25 2015 -0600

    Lets use Dark Material colors
    - TRDS will switch to use these colors.
    - We have permission from @nicholaschum to use these colors for our TRDS.
    - Add more white icons and remove the ones that we do not use.
    
    Change-Id: Ia3012e3f4ffddf8ff560822fca27fad62118c561

commit ee24d426a5d5cf2793f6ed95f9e40d72c1fa16df
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 30 11:46:22 2015 -0700

    remove leftover breathing sms/misscall/voicemail

commit e01b6b2f77c9b2e38b0ec5afcf15d9874b1b4562
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Apr 15 19:03:00 2015 +0100

    Settings: enable/disable doze through Profiles (2/2)
    
    * moved isDozeAvailable boolean to Utils so we can check for it in profiles
    
    Change-Id: I5a768098b4ed00b28931bee58a58efa8280262a1
    
    Conflicts:
    
    	src/com/android/settings/DisplaySettings.java
    	src/com/android/settings/Utils.java

commit 25b55e41b24bd73d1619813eec9bd71390b97a3d
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 30 14:51:21 2015 -0700

    Revert: Remove extra kernel gcc version info (1/2)
    
    No longer needed with 9590f426e7986e64d68ae80b4ac5c6409f4c88b5
    
    Change-Id: Idd694e9616fa9875aa3911e58ec8a4e526423c0b
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	res/values-eu-rES/cm_plurals.xml (reverted from commit 0b39c4336d5199dda88f460f1f026bb171201498)

commit f6fafbfd0b640d9fc7d58d97c194fd214764329a
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Apr 28 14:02:21 2015 -0700

    CryptKeeper: pattern unlock displays incorrect pw when correct
    
    fakeUnlockAttempt() gets called when the user inputs any pattern length
    < 4 which queues up the 'incorrect error' message. The message needs to
    be cleared before trying to actually check the password so it never goes
    through in case the password was correct.
    
    Change-Id: If78db332d3d696ba443d0be911fb5db504cb14cd
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 91f09fd9c2590455f886c411c7db83f9a97c8d26
Author: tobitege <tobiasteschner@googlemail.com>
Date:   Wed Apr 29 21:17:05 2015 +0200

    Fix NPE in slim shortcut if no icon was found
    
    Change-Id: If7adfdb82a8d014ab44ab74670b7a0e1655ecb9d

commit 1747be34b9a671e8c23a78655fb48e0c7a63bfcb
Author: rogersb11 <brettrogers11@gmail.com>
Date:   Fri May 1 17:57:49 2015 -0700

    Add back TRDS Tile 2/2
    
    Change-Id: I5c85f060f4bb219b74b18dadc91636813b0aa634
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit 9f829ebf99eaf6b848ec3c7762b077fa4a528b67
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 30 10:39:09 2015 -0700

    Settings: disable mobile network switch when SIM isn't ready
    
    Change-Id: I4676390760f0d6107e706fe75cd26f7bf603cad6
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit b0f0daa8044679a509657b96bcd7d368678bb071
Author: 0xD34D <clark@scheffsblend.com>
Date:   Fri May 1 17:55:38 2015 -0700

    Identicons: Add identicons to ChaOS Lab [2/3]
    
    PS2: fix build
    PS3: make all menu entries dependant on switch
    
    Change-Id: Ifcbc108ec7d0885e5001b761b29c0abb21626b71
    
    Conflicts:
    	AndroidManifest.xml
    	res/values/attrs.xml
    	res/values/cmr_arrays.xml
    	res/values/cyanide_strings.xml
    	res/xml/cyanide_settings.xml

commit 190d660cceb4c7152b7fefc0657a5d0c5cce9ac1
Author: Roman Birg <roman@cyngn.com>
Date:   Fri May 1 17:07:47 2015 -0700

    Settings: fix non lock pattern CryptKeeper crash
    
    Change-Id: Ib2d6c9a468bfe778d5cb927759f11b2b03c25ee6
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 9ff0f91a3d68691816c1c1f130f78a730a4bacec
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:52:52 2015 +0300

    Automatic translation import
    
    Change-Id: I9fd530907d8d5dc5595b0bd518c8d049d57a894d

commit c611a126cbfe5e17d03332cda67b9e359042b9a5
Author: LorDClockaN <davor@losinj.com>
Date:   Mon Apr 6 08:23:08 2015 +0200

    AdBlocker: We rule the device, not SELinux
    
    Change-Id: If7c7bdd296e3e9ad2cef91d651bec9851e5f0426

commit f109273acb8172b8c88ba95ba2f7a6486bc1d81c
Author: Evisceration <eviscerationls@gmail.com>
Date:   Sun May 3 23:06:27 2015 -0700

    (2/2) Settings: instant reboot action trigger
    
    Change-Id: I56969b52b5b875cc345f8e851c8ea88c343ed922
    
    Conflicts:
    	res/xml/power_menu_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml
    	res/xml/power_menu_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 5f6d9388283721bd9d90468254377552a245267d
Author: rogersb11 <brettrogers11@gmail.com>
Date:   Sun May 3 23:10:55 2015 -0700

    AppSideBar Tile 1/2
    
    Single click toggle, long click settings as per usual setup
    
    Conflicts:
    	AndroidManifest.xml
    	res/values/cm_strings.xml
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java
    
    Conflicts:
    	AndroidManifest.xml
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit c944ac5029ba9e091536ce1ffdbe5c8b3b234923
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 02:08:33 2015 -0700

    [Squash] Revert Settings: Ambient Display configurations
    
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
    	src/com/android/settings/DisplaySettings.java (reverted from commit 16c112170e1476630bc30621557906105dda1006)
    Update Ambient to PS23
    
    Change-Id: I1268e75ff3b84cdaacfee93634973837c6c6a1ab (reverted from commit 5ca78fee5d931711ce422d3bf3232a414e6b5c8c)
    Update Ambient to PS29
    
    Change-Id: Ia1080b736b89ac02e817d34c93da1a63e5049863 (reverted from commit b169f9b4f2f46e07804677baa89d105f5baccc25)
    Fix build aftger ambient patch update
    
    Change-Id: Id53ec1d6cffb2278b39a14240e0cf6dbdff051c0 (reverted from commit dd52e38d32ac2449d774093addbeedab21a860d3)
    Settings: use switch preference for Ambient Display
    
    Change-Id: I2dc12b83ac24ac7a120d2a8808c17b2425c118ef (reverted from commit 51bc07f8e1683740e3f09c1bfed25167c3425f9c)
    Display settings: show enabled/disabled summary for ambient display
    Change-Id: I97aee7aafd69f3e60d2c518aa514a7cd1dff9ecf
    
    Conflicts:
    	res/values/custom_strings.xml (reverted from commit f41f19f5bb79886ef6e1d8e0aefec5de9caa16a1)
    Display settings: remove ambient display screen when advanced mode is disabled
    
    now when advanced mode is disabled ambient display will be a simple switch preference
    
    Change-Id: Ia50897590b56a7d295255828da3d62e9535c0c60
    
    Conflicts:
    
    	res/xml/display.xml
    	src/com/android/settings/DisplaySettings.java
    
    Conflicts:
    	res/xml/display.xml (reverted from commit 3a9299f4bc2a6279a06e247bceb7475ee3d6f0bc)
    Settings: enable/disable doze through Profiles (2/2)
    
    * moved isDozeAvailable boolean to Utils so we can check for it in profiles
    
    Change-Id: I5a768098b4ed00b28931bee58a58efa8280262a1
    
    Conflicts:
    
    	src/com/android/settings/DisplaySettings.java
    	src/com/android/settings/Utils.java (reverted from commit e01b6b2f77c9b2e38b0ec5afcf15d9874b1b4562)

commit 86e59eee7ff6e7727771d72a35c9ea100c835348
Author: ZION959 <ziontran@gmail.com>
Date:   Sun May 3 18:08:30 2015 -0700

    Revert : QS: add Ambient display tile
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
    	res/values/cm_strings.xml (reverted from commit 88df6a1d5ae633c81f794f747a38b26825e55ee9)

commit 6c8ee493e62f45316f24c022dcb36c3e5cd103ae
Author: dankoman <dankoman30@gmail.com>
Date:   Sun May 3 21:55:57 2015 -0700

    [1/2] Settings: Slim doze options
    
    option to turn off TriggerSensors for doze pulse (pick-up/
            significant motion sensors)
    patchset: doze schedule preference
    patchset: notification trigger preference
    patchset: split pickup gesture sensor and significant
            motion sensor triggers into two preferences
    patchset: move doze options to own preference screen
    patchset: config booleans from systemui:
            This changes the conditions under which the TriggerSensor
            preferences (pickup gesture and significant motion sensor)
            are displayed. If the device is configured to use the sensor
            by default (according to the boolean resource in SystemUI's
            config.xml, or the device-specific overlay), the preference
            for that sensor will appear under doze options.
    patchset: doze brightness preference
    Change-Id: Id9b98403477deced056fdc30212f69e48e670e2b

commit cf0c10a25821e7e322f83c4fd75cccc1a61b458f
Author: 0xD34D <clark@scheffsblend.com>
Date:   Sun May 3 23:13:52 2015 -0700

    Settings: Gesture Lockscreen (2/2)
    Lets give this a go again.
    
    Changes needed for lollipop
    
    AICPfy
    
    Change-Id: Icf2f5a5cd3474ea325097437bc2956c10e2ae9d7
    
    Conflicts:
    	res/layout/smbanner_row.xml
    	res/values/cmr_strings.xml
    
    Conflicts:
    	res/values/cmr_attrs.xml

commit 5b779110ed41e5b1b31446c774e1a5505e75b5cd
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Thu Apr 30 16:07:07 2015 -0700

    Settings: fix bad MTP uncheck behavior
    
    Unchecking MTP will cause it to attempt to
    set MTP again which never fires the callback
    to re-enable the UI state.  So if the user unchecks it
    don't disable UI.
    
    Change-Id: I6d6f3f13cc91fe4df0126b1cf43e571ccb42d62c

commit 754406266facfa5f272893880b101cb09fe4c581
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Wed Apr 15 19:03:00 2015 +0100

    Settings: enable/disable doze through Profiles (2/2)
    
    * moved isDozeAvailable boolean to Utils so we can check for it in profiles
    
    Change-Id: I5a768098b4ed00b28931bee58a58efa8280262a1

project packages/apps/SlimLauncher/
commit 545bd8acc5ebeadcb14f7e3fda51b875ef8fa274
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Tue Oct 14 16:12:12 2014 -0700

    Moving the focus indicator instantly to the target position, instead
    of begining the next animation from the middle.
    
    Bug: 17958897
    Change-Id: Ie5a39b80ff9788edf368e0f4e23c07c2ed5b3d2c

commit d357d5884c55ad8bdcf4a5c9fde9fae3c119778d
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Tue Oct 14 16:42:54 2014 -0700

    Adding NPE check in InstallShortcutReceiver
    
    > Removing some unused methods
    
    Bug: 17971165
    Change-Id: I1bc5c764fd65b44c950a58371b60d2b53c221995
    
    Conflicts:
    	src/com/slim/slimlauncher/InstallShortcutReceiver.java

commit c0ed928b5dba9a3428b670a5e1e83c953c6022ff
Author: Geoff Mendal <mendal@google.com>
Date:   Wed Oct 15 10:46:05 2014 -0700

    Import translations. DO NOT MERGE
    
    Change-Id: Ied5954dcd88f900ae2f9e21b1ec0cdbe01cad06b
    Auto-generated-cl: translation import
    
    Conflicts:
    	res/values-ms-rMY/strings.xml

commit db34f57223d235b9f6b2766939bd6f5029a93f9f
Author: Adam Cohen <adamcohen@google.com>
Date:   Tue Oct 7 18:14:53 2014 -0700

    Use LauncherCallbacks model instead of method overrides
    
    -> When extending the Launcher Activity, instead of overriding
       public and protected methods, create a proper interface
    -> This helps define the interface when extending Launcher
       more formally and more clearly
    
    Change-Id: Ib38e8a376b2242d4078bf6856bb145f5b5f0da80
    
    Conflicts:
    	src/com/slim/slimlauncher/Launcher.java

commit 4de7ca7d870c52a77e7245d5732085d7480e98cb
Author: Helena Josol <helenajosol@google.com>
Date:   Thu Oct 9 17:04:09 2014 +0100

    Add more Launcher files to delete on Clear Launcher Data
    
    Bug: 12753154
    Change-Id: I00679bdc6eff70a1398122aaa955c08eabd556b1
    
    Conflicts:
    	src/com/android/launcher3/LauncherFiles.java
    	src/com/slim/slimlauncher/Launcher.java
    	src/com/slim/slimlauncher/LauncherAppState.java

commit 41b08e1d8428caf3f30088e2c60b93694d1ea91b
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Wed Oct 8 10:47:28 2014 -0700

    Showing widgets in a disabled state, when running in safe mode
    
    Bug: 15172107
    
    Change-Id: I7209836ca4ffacde7b7b232e230e9b9f1a0e54bb
    
    Conflicts:
    	src/com/slim/slimlauncher/Launcher.java

commit 1fad5f6bbb79cf95bab3d207c2f08ab31112e043
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 16 12:08:41 2014 -0700

    Not opening all apps again when AppInfo or Uninstall is selected
    
    Bug: 17460202
    Change-Id: Id67a9637324abceb5b446fff5999db2a0910401b
    
    Conflicts:
    	src/com/slim/slimlauncher/DeleteDropTarget.java

commit 3beca13868f89e47b13d43bf655dd9123319993a
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 16 12:18:37 2014 -0700

    Deleting workspace items from db which have an invalid placement
    
    Change-Id: I1d616e8cd533acd6ecd334d85e6468163f31f6a4
    
    Conflicts:
    	src/com/slim/slimlauncher/LauncherModel.java

commit 91682ebd5422f68c7767cd163e93ddbb85f11a29
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 16 14:07:29 2014 -0700

    Fixing some IconCache methods not  thread safe
    
    Bug: 17981568
    Change-Id: I0d49604c2e38bc9017cba527d87e24e8b086f1da
    
    Conflicts:
    	src/com/slim/slimlauncher/IconCache.java

commit c0c5b1c6323f7c16437dcf244ab334c1802b90d2
Author: Adam Cohen <adamcohen@google.com>
Date:   Thu Oct 16 09:49:52 2014 -0700

    Adding ability to list folder items in separate file
    
    -> remove all apps default layouts
    
    Bug 17569015
    
    Change-Id: I39b899b61d5b1cff2d7801d281dacfc804c403c5
    Conflicts:
    	res/xml/default_workspace_4x4_no_all_apps.xml
    	res/xml/default_workspace_5x5_no_all_apps.xml
    	res/xml/default_workspace_5x6_no_all_apps.xml

commit 3ad1b131e5eee559d8762db54659e107f5d31dab
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 16 16:03:21 2014 -0700

    Removing all traces of Market button and TabIndicator
    
    Change-Id: I9dc10d990321697723560986834ebeef3e0f1c0d
    Conflicts:
    	res/layout/tab_widget_indicator.xml

commit b2075788be152468eff651b86808a10dcb1bf8b2
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Wed Oct 1 15:33:41 2014 -0700

    Refactoring layout parsing code
    
    Change-Id: Iee5b2280cb1e841bcfe91fdcf523de6fa7f7f3b8
    
    Conflicts:
    	src/com/slim/slimlauncher/AutoInstallsLayout.java
    	src/com/slim/slimlauncher/LauncherProvider.java

commit 01fdc0d28686b6049b19e4da3cf988710aecc67c
Author: Nick Kralevich <nnk@google.com>
Date:   Sat Oct 18 06:57:06 2014 -0700

    fix build
    
    Bug: 18040469
    Change-Id: I24db4d3f4b7ee10ecf5a2c65035ce112271539fb

commit 47cb8e237f55e6332f081b49d857735ea3cd0ffb
Author: Nick Kralevich <nnk@google.com>
Date:   Sat Oct 18 08:14:09 2014 -0700

    fix build
    
    Bug: 18040469
    Change-Id: I2938c7b950470eeacfb20391f109ae44d95060c7

commit a956d490a619f0a212e153882e40dd0a2fd20c35
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Tue Oct 21 10:04:54 2014 -0700

    Removing AccessibleTabView and some other dead code.
    
    Change-Id: Ia122a6277f924e6077dbf15a4dc40b5042aa987d
    
    Conflicts:
    	src/com/slim/slimlauncher/AccessibleTabView.java

commit 86c9afd1fdcf08714228ea04d9a617316d91c251
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 23 11:09:18 2014 -0700

    Removing landscape string overrides
    
    Change-Id: Idbfc600dfb32b195726f1b035d18be92c26883fd

commit 37ce7fe8fdb54f3bb336e6daf0ef901596c49edb
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 23 11:38:15 2014 -0700

    Some resource fixes for drop target
    
    > Making it singleline with ellipsis everywhere
    > Decreasing the text size on smaller devices
    > Decreasing char limit for various labels
    
    Bug: 17563793
    Bug: 17938450
    Change-Id: I8ad1a156de0601d07419b2cc6418389bc2e24a4e
    
    Conflicts:
    	res/layout/drop_target_bar.xml
    	res/layout/search_drop_target_bar.xml
    	res/values/styles.xml

commit 5b21fc82539bc3aa143bd1fe2dc5d76e6505df22
Author: Adam Cohen <adamcohen@google.com>
Date:   Thu Oct 23 17:28:30 2014 -0700

    Allow LauncherOverlay to access and manage insets
    
    Change-Id: Ib9faf37eb22ad2a0b18c076978ec9f2fd8864c0c
    
    Conflicts:
    	res/layout-land/launcher.xml
    	res/layout-port/launcher.xml
    	res/layout-sw720dp/launcher.xml
    	res/layout/launcher_overlay_example.xml
    	res/layout/tab_widget_indicator.xml
    	src/com/android/launcher3/LauncherCallbacks.java
    	src/com/android/launcher3/LauncherExtension.java
    	src/com/slim/slimlauncher/DragLayer.java
    	src/com/slim/slimlauncher/Launcher.java

commit 75df5446b9eb8bc53fb6318633371668af93e293
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 24 12:20:20 2014 -0700

    Was seeing some duplicated icons in the migration flow
    
    -> The only delta between the two icons was slightly different flags
    -> No need to consider flags for the purposes of duplication
    
    Change-Id: I161f6ad6023d829e5ebbb15f1a9fbc9306795d80

commit b9ebeed5fd5fcdb8d15677d8e6da8f0f2ddb75f4
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 24 16:45:59 2014 -0700

    Add InsettableFrameLayout layout params to easily ignore insets
    
    Change-Id: I117fc34627e24ea5f909c3c87e9c2dbca46babb6
    
    Conflicts:
    	res/values/attrs.xml
    	res/values/styles.xml

commit 6f208c2898f0b071ddb5638dd97dbbedd15524bd
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 24 17:40:34 2014 -0700

    Fix edge case where LauncherOverlay scroll woudln't be reset
    
    -> If the Workspace has a single page and the user goes from overscrolling
       in one direction, and then the other, the LauncherOverlay scroll wouldn't
       be set to 0 until the scrolling settled
    
    Change-Id: I29ee9abdfa023ae3599d1590cdaebf457e2220fa
    
    Conflicts:
    	src/com/slim/slimlauncher/Workspace.java

commit 1fb9608a459fcc5a9adcc835cbbf0b9d0624fbb2
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 23 14:21:02 2014 -0700

    Loading internal default layout if partner layout fails to load
    
    Bug: 18033885
    Change-Id: I8399d0107cc3570c0e03d833601abf2cd194b3d3

commit 1c90fb3ecdb4a956eced0fe06cc520f3e432d66a
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 16 09:24:19 2014 -0700

    Updating backup restore logic
    
    > Adding DeviceProfile information in the backup
    > Removing SharedPreference backup
    > Adding helper methods to abort backup in the middle
    > Comparing keys against the backup journal during restore
    to avoid restoring corrupt/lost entries
    > Old backups are still compatible, but lost keys verification
    will be ignored in that case.
    
    Bug: 17937935
    Bug: 17951775
    Bug: 17260941
    Change-Id: Iad48646cfdd69abaff5c163b2055f3b8a9b39b19
    
    Conflicts:
    	src/com/android/launcher3/LauncherBackupAgentHelper.java
    	src/com/android/launcher3/LauncherBackupHelper.java
    	src/com/slim/slimlauncher/Launcher.java
    	src/com/slim/slimlauncher/LauncherAppState.java

commit 29f30089c321a9c7eb1aee27709cb53270d1abd0
Author: Adam Cohen <adamcohen@google.com>
Date:   Tue Oct 28 16:16:02 2014 -0700

    Make sure DragLayer layout params are of the correct type
    
    bug 18141419
    
    Change-Id: I50695a62cf9e1f25c054ac2c7197cd056d54cfae

commit 42fe4781b9810e87b4dd43f99ac64069b9923267
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Tue Oct 28 16:30:20 2014 -0700

    Fixing insets of launcher clings
    
    Change-Id: Idbf46680f96086c93d667c26dc9ed214eeaf835e
    
    Conflicts:
    	res/layout-land/longpress_cling.xml
    	res/layout-port/longpress_cling.xml
    	res/layout-sw600dp-port/longpress_cling.xml

commit 1904bc16b849be4661804b70feffc3fbce2a50a8
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 30 10:16:49 2014 -0700

    Moving methods which update internal sets on a separate thread
    
    Bug: 18152117
    Change-Id: I5fccd203b5fe65e79dcc5aead6cb1cb6c3b622fe

commit 6e4de03a69b9ec251a8cf3b07468290fd68a0118
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 31 11:48:25 2014 -0700

    Adding a couple memory optimizations to Launcher
    
    -> Always dispose of widget page views when leaving the activity.
       These pages hold onto many bitmaps.
    -> Clear database cache when leaving the activity.
    
    Bug: 17967108
    Change-Id: I10ebaaed14e7cd86f09a9afcabd73043705f21b8
    
    Conflicts:
    	src/com/slim/slimlauncher/AppsCustomizePagedView.java

commit 28a3cd9ac05bd2073a3844ad6636752a1e31504a
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 31 16:15:36 2014 -0700

    Overlay shouldn't show up above Intro screen
    
    bug: 18173340
    Change-Id: Icf738a55398023ab6bad5cced05b25e053dec0a2

commit 3719f1b0ccb30e0ee08fcc325f23bddf6cc3a277
Author: Adam Cohen <adamcohen@google.com>
Date:   Fri Oct 31 16:58:00 2014 -0700

    Fix folder hint text color. Likely a regression from upgrading the Activity theme
    
    Bug: 18204650
    Change-Id: I5e23df5f4f8f1f8ca7a22c8a62797e77c9a4a9e1

commit e68d8b43ed6ccc4706a5c144c24e0443144421ef
Author: Adam Cohen <adamcohen@google.com>
Date:   Mon Nov 3 16:13:45 2014 -0800

    Updating page indicator assets
    
    Bug: 17318376
    Change-Id: I4e73bf4892575bbb31f28d2cf1a4e476f8895dfa

commit a6054f4f8508ff17d75e59b61f222fd3ec426d40
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Wed Nov 5 10:34:43 2014 -0800

    Removing InstallWidgetReceiver related obsolete code.
    
    Change-Id: I61700b363f8af6434e750bcb5323e0ad4e5bf011
    
    Conflicts:
    	src/com/slim/slimlauncher/InstallWidgetReceiver.java

commit 2113224eb70d838b90eaf0c59db5542fc8484b0a
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Mon Nov 10 16:01:44 2014 -0800

    Proguard changing methods required for click feedback aniamtion
    
    Bug: 18323452
    Change-Id: Iac6d75a3c46c3a4c2a74af43bd1fca738235c2d5

commit 1bd65c5454b6caddccf7554fa14cd20bde9baac8
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Tue Nov 11 12:23:59 2014 -0800

    Removing some duplicate methods
    
    Change-Id: I8a1295ab74890984e8d8508aaa18fd79ac2a032d
    
    Conflicts:
    	src/com/slim/slimlauncher/LauncherAppState.java

commit 2474fd9491fb93da30ea1e69bd1acf4cbe123e10
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Mon Nov 10 18:05:31 2014 -0800

    Adding shortcuts corresponding to ManagedUsers automatically.
    
    Bug: 16188104
    Change-Id: Ic07578dd187263f59f3c431cbb78dea90d0c24f4
    
    Conflicts:
    	src/com/slim/slimlauncher/InstallShortcutReceiver.java
    	src/com/slim/slimlauncher/LauncherModel.java

commit dd13aac26cba839f1f8aeada074a104bb1d6dcf2
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Fri Nov 14 10:14:18 2014 -0800

    Fixing NullPointer Exception when user is deleted.
    
    Bug: 18388507
    Change-Id: I4176ea37a019c2a862e6b2875cc6b03ec9118571

commit 3f21e64f9926c6e2103cbeb42d6cc9b6a281abb6
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Fri Nov 14 11:59:57 2014 -0800

    Adding a few null checks.
      1) During migration, if launcher2 has deleted user data,
    migration oes not happen
      2) If Launcher3 does not has bind widget permission,
    QSB would be null.
    
    Bug: 18388507
    Change-Id: Ief81f6f77ce154e7b3ecd4b77caf24239401e738
    
    Conflicts:
    	src/com/slim/slimlauncher/Launcher.java
    	src/com/slim/slimlauncher/Workspace.java

commit a356ee08484ddec97a279aff57d436f4ad433ecd
Author: Adam Cohen <adamcohen@google.com>
Date:   Mon Nov 17 17:45:34 2014 -0800

    Add callback which got missed in refactor
    
    Bug 18418855
    
    Change-Id: Ia3a1cec76721bbbc118dd7389b5e960802a64b88

commit c41d36bd46d8de6b986190afc139cccf624bba38
Author: Adam Cohen <adamcohen@google.com>
Date:   Tue Nov 18 17:53:44 2014 -0800

    Prevent multiple workspace state animators from being started
    
    -> Probably an issue with the way we're wrapping ViewPropertyAnimator
       which can lead to us acting like it's valid to have multiple
       instances of a VPA. In reality I think this is very problematic.
    -> For now, we can just make sure the previous animation is canceled
       if it hasn't yet completed.
    
    Bug 18428886
    
    Change-Id: I097eec08ec68ed098e68866fb5eda72734c51b00

commit bef1ce4b50c828fb4a077a6548d46ffc6ca4648b
Author: Adam Cohen <adamcohen@google.com>
Date:   Wed Nov 19 16:03:20 2014 -0800

    Fix a couple regressions from resetting AppsCustomizeTabHost
    
    Bug 18409435
    Bug 18358080
    
    Change-Id: I07a071342b5c5e062ab2bb562b672d93ba0d5c2e
    
    Conflicts:
    	src/com/slim/slimlauncher/AppsCustomizePagedView.java

commit e4cf3eb031c033b19fc764b3c982a2f0c3902d8b
Author: Adam Cohen <adamcohen@google.com>
Date:   Thu Nov 20 14:27:27 2014 -0800

    Updating default page indicator asset
    
    Change-Id: If1be59c8c6590125c2347ba2928f61522f15f959

commit 6596fbe3e789270475697720716663cdc174ae65
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Nov 20 17:01:00 2014 -0800

    Disabling auto addition of managed profile shortcuts
    
    Bug: 16188104
    Change-Id: Ib6464c22140df6d60112eb35f5983718b3db6288

commit 39b08d15b7c55a294bfaeb375cc6342927f652c3
Author: Chris Wren <cwren@android.com>
Date:   Mon Nov 24 16:57:54 2014 -0500

    Don't try to create an app state instance during restore.
    
    Added a static utility function to get the DeviceProfile instead.
    
    Bug: 18504164
    Change-Id: Ia510a84f1c195e58acf3bf4d1f6a42c739fdd413
    
    Conflicts:
    	src/com/android/launcher3/LauncherBackupHelper.java
    	src/com/slim/slimlauncher/LauncherAppState.java

commit 7eaad376e0eb6b6922801c89bfc0a69be7562e6f
Author: Winson Chung <winsonc@google.com>
Date:   Mon Dec 1 15:05:17 2014 -0800

    Ignoring specific db exception to workaround Bug. 18554839.
    
    Change-Id: I80f2dd62297eea671f2d129ae22263e72e506ae4
    
    Conflicts:
    	src/com/slim/slimlauncher/WidgetPreviewLoader.java

commit e5cf48148ca349280a3dd0e4cc60fce877df0eb0
Author: Adam Cohen <adamcohen@google.com>
Date:   Tue Dec 2 15:24:52 2014 -0800

    Ensure that FirstFrameAnimatorHelper doesn't set play time when animation is complete
    
    Bug: 18567716
    
    Change-Id: I656e869b8553d650916c2abe6dc83282c8b6fd65

commit 0a94f287f9ceb7b8706e5c6e4cf208bc0cc16238
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Wed Dec 3 14:25:16 2014 +0530

    Fixing wrong package check when adding shortcuts
    
    Bug: 18571789,18535867
    Change-Id: I2544fa634879846d812b00f8649520400f66d29e

commit f3411f7cb73b986bb9df1fd2eda7a3cb589919e8
Author: Adam Cohen <adamcohen@google.com>
Date:   Thu Dec 4 10:34:57 2014 -0800

    Avoid db exception on L and above
    
    Bug 18554839
    
    Change-Id: I43f391b7cc376f697ce7b5b363e8be3aa85814b5

commit 41135322bcdf74cf915015ce356aca98e2db26da
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 16:20:44 2015 -0500

    Cleanup after merge

commit 39db00a376b5afe3a18dd63de98e057ca377ee66
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Thu Oct 2 15:58:31 2014 -0700

    Keeping icons in disabled state when SD-card is unmounted
    
    > changing shortcutInfo.isDisabled to be a flag based variable
    > on received OnPackageUnavailable, icons are disabled from desktop
    instead of being removed. Icons in all apps are removed
    
    Bug: 15852084
    Bug: 16238283
    Change-Id: I126d23c709682a917d4bbb84de71032593dce8f9
    
    Conflicts:
    	src/com/slim/slimlauncher/LauncherModel.java

commit 6f2cf2256ffd50e26e4be46bdde7c5fa5c3a2c15
Author: Sunny Goyal <sunnygoyal@google.com>
Date:   Mon Oct 6 16:23:56 2014 -0700

    Updating icons for sortcuts when the target app updates.
    
    Bug: 17398260
    Change-Id: I055abb971d1f72245e8616ac2ce07bcdf37cdd52
    
    Conflicts:
    	src/com/slim/slimlauncher/Launcher.java
    	src/com/slim/slimlauncher/LauncherModel.java
    	src/com/slim/slimlauncher/Utilities.java

commit a49e2c7b6bb85fa4062f0eb0617c307a8dd007b0
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 17:17:35 2015 -0500

    Updating ItemInfo objects in the worker thread
    
    > Launcher was making non-trivial updates to ItemInfo objects
    on UI thread. These updates were getting skipped when the
    Activity gets destroyed (possibly due to onConfigurationChange)
    > Unregistering SessionCallback on application onTerminate,
    rather than activity onDestroy
    
    Bug: 17941096
    Change-Id: Iad4a50871fe09470f26139b44a2e9886833032f1
    
    Conflicts:
    	src/com/slim/slimlauncher/LauncherAppState.java
    	src/com/slim/slimlauncher/LauncherModel.java

commit 77c67ab9874807a7a1fdbaa3096b3d00f2fec9b3
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 17:46:22 2015 -0500

    First pass of the Launcher Overlay interface / impl
    
    -> Added simple reference launcher extension
    -> Make launcher able to handle a null qsb
    
    Change-Id: Ib1575243cac800a335e95bbf00cdc394bb4741c3
    
    Conflicts:
    	res/layout-land/launcher.xml
    	res/layout-port/launcher.xml
    	res/layout-sw720dp/launcher.xml
    	src/com/slim/slimlauncher/Launcher.java
    	src/com/slim/slimlauncher/LauncherCallbacks.java
    	src/com/slim/slimlauncher/SearchDropTargetBar.java
    	src/com/slim/slimlauncher/Workspace.java
    
    Conflicts:
    	src/com/slim/slimlauncher/Launcher.java

commit 84fb5517d1cb5a6978c482af511fde484634bfed
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 17:47:03 2015 -0500

    More cleanup from merge
    
    Change-Id: Ie33208cb52ceef7678e306c1f94f34ff2730aa04

commit 7cabd7deaa2a1f61f2e96bab8395b0b8489d43e7
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 18:07:26 2015 -0500

    Fix all apps button disappearing
    
    Change-Id: Ibb3c29bdc60d0bf36d640fd70b0ceb9f02c241f8

commit 5ad22b4f98908e630405bccdfa0eb735e172055c
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Apr 28 18:26:12 2015 -0500

    Some fixes for overview mode
    
    Change-Id: I792d9723d84fcf45ba6dd2f5346add4fc63d41bb

commit 269703a423e44cce1dcf6f8bcc2731fa6a162d85
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Fri Jan 23 00:39:08 2015 -0600

    Fix drawer labels
    
    Change-Id: Ifbeaee592eaac84c3a29200f1b9c13adf9e86688

commit 4f747e334c50d31058072fcc9401d5a86aad6ce5
Author: Griffin Millender <griffinn.millender@gmail.com>
Date:   Tue Sep 30 20:55:30 2014 -0500

    Add button customisation
    
    Change-Id: I31151047da13c2cdcb495581b1674e1bfef05f48

project packages/apps/SoundRecorder/
commit 51ccfffa090cf85b27775726a4e811e349e9dba1
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Apr 30 12:05:24 2015 -0700

    SoundRecord: when responding to GET_CONTENT, assume exit after record
    
    Change-Id: I7ae3faf26d0d352a791a33720b5a73d7fab5eaa0

commit 615756091522128286e781df16f81896fd4fc77e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:53:13 2015 +0300

    Automatic translation import
    
    Change-Id: I78ae6bf37e33077b58d4d95274a6671a32f46b28

project packages/apps/Stk/
commit 656cd2757c0d91311485fdd95328c3b08719d6e5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:53:18 2015 +0300

    Automatic translation import
    
    Change-Id: Id345822de58eb483b0b65752fc1e0a69f47db7bd

project packages/apps/Terminal/
commit aa252f1b21e8f35e49c92b01d42da50d17e3a837
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:53:22 2015 +0300

    Automatic translation import
    
    Change-Id: I37ce3c2917606ca5ceeaebdac494fbc99d958203

project packages/apps/ThemeChooser/
commit 6951d6021d04b155f8506ae9984f84d0d23ac4f9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:53:26 2015 +0300

    Automatic translation import
    
    Change-Id: I6f888ee23ea03a48d94f9075b1ec6eedceb220e3

commit 7f00bbb3a5c892bad13ac0c2483e690137826133
Merge: 3c9f0e1 6951d60
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:44:54 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/TvSettings/
commit ab29d3f3f4356df0cd06d63fdb8dbf6a06126975
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 28 03:29:36 2015 -0400

    Developer Settings: Add setting for updating recovery
    
    When enabled, the recovery of the device will be updated with the
    version of the installed system.
    
    Change-Id: I552293af5bf179227e5ee1163b4653fa00f3261b

commit fa2e1904c4bb73d04b4921486289981442a2160e
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 28 19:42:06 2015 -0400

    Developer Settings: Add warning to request root access
    
    And ensure properties are reset when disabling adb root
    
    Change-Id: I9751725cbabe69f6497b18e92acd6387d6a9ce91

commit b42887916592364c1652eb91a6a4eb8571f7aed4
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Wed Apr 29 01:26:57 2015 -0400

    Developer Settings: ADB over network
    
    Change-Id: I70bc363ddf8810aa44d88c8f700df601d8b60f69

commit cd739aae458006d732dde2ecf23773f8d4eab986
Author: bmc08gt <brandon.mcansh@gmail.com>
Date:   Wed Apr 29 09:55:21 2015 +0200

    TvSettings: Create HomeActivity
    
    * Wrapper around the exisiting pref key that leads to leanback settings
    * Allow reset of default home screen (launcher)
    * Navigate to home settings (leanback settings)
    
    Change-Id: I1e6f1dccdd187eb5a30c87d628d4d878a5228506
    Signed-off-by: bmc08gt <brandon.mcansh@gmail.com>

commit bd65ad8dd892371eea8699d3d51d8fadc9a8771b
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Thu Apr 30 02:56:19 2015 -0400

    Developer Settings: Enable Local Terminal (2/2)
    
    Change-Id: I7926e14617eb7dcf8bc02a91a2244db040420052

commit 43008a4d1f88b0e7df825a4e0e5f90ef971ba02c
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Fri May 1 14:01:31 2015 -0400

    Developer Settings: Only show ADB Over network when debugging is enabled
    
    Also move to debugging category
    
    Change-Id: I81ce701c66e52f9e43927158a6d9c7282b3f3271

project packages/apps/UnifiedEmail/
commit 97762e5d3c2504ab0dc1d630bac4df18a0451177
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Mon Apr 20 04:17:22 2015 +0200

    unified-email: custom notification lights
    
    Change-Id: I34b4149afff1c6688cf5e032ff82fdb41227cdb9
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 3cdd22d0dfd08cbdd622f8bdb1e61d5094fe0aa7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:53:38 2015 +0300

    Automatic translation import
    
    Change-Id: I1b65c9813cca7b2ae75c76fb54c6d62c24fac038

commit 3aa1c3701303dab282bcca885bf33919c1502bcf
Merge: 865682e 3cdd22d
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:45:25 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/providers/ContactsProvider/
commit 3ef3a298baf1f71dce1ae9221371f8805fa510d0
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 17:22:09 2015 -0700

    Identicons: Add identicons to ChaOS Lab [3/3]
    
    When enabled, new contacts will be assigned a unique
    5x5 identicon as the contact photo instead of the boring
    default one.
    
    PS2:
    Use the new GithubIdenticon class for now.
    
    PS3:
    Make use of the IdenticonFactory
    
    PS4:
    Add proper annotations for ChaOS Lab.
    
    Change-Id: I8c166504571baf6acaacfb95eda33b13c14ffa61

project packages/providers/DownloadProvider/
commit 858a00597ebe1962bab3be77561fc0eeddcc7644
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:54:39 2015 +0300

    Automatic translation import
    
    Change-Id: I370caafc85cdcc0572c957f3c8d5fc227bd6909e

project packages/providers/ThemesProvider/
commit 5c81d895cf31a45246351e8cfcfa7132a33c9cdb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:54:44 2015 +0300

    Automatic translation import
    
    Change-Id: I852c9d9d813d32fd162f4984368b55263bfea51e

project packages/services/Mms/
commit c02c41560b150c85b04bbf9cbea32f647a69afff
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:54:49 2015 +0300

    Automatic translation import
    
    Change-Id: Id474011d23c1bf0fa1418eafef680bbd6807608f

project packages/services/Telecomm/
commit ccf6031a786ba968f669f125d972ad355552b961
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:54:52 2015 +0300

    Automatic translation import
    
    Change-Id: I91e9f59b0b1dd36ccfcadcee094a11dc5c0ed28e

commit fb2631f0e21df0d55fbc467b195f15ee16eaf453
Merge: e4b451a ccf6031
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:44:12 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/services/Telephony/
commit c3c55852de04fab7a813c9e6258320f9b8952126
Author: LuK1337 <priv.luk@gmail.com>
Date:   Wed Apr 29 13:31:53 2015 +0200

    msim: Fix FC on opening "calling accounts" in Dialer settings
    
    Variable sir seems to be null on some msim devices.
    
    Change-Id: Ia046e04da2edc0c06ed91a5878111f8e98f23b3b

commit a4c8700f51517afdee390ff7090cce38b47ecad9
Author: mengsun <msun@codeaurora.org>
Date:   Wed Dec 11 17:56:42 2013 +0800

    TeleService: Add a controller for in-call proximity sensor (3/3)
    
    Add the setting for enable proximity sensor or not when calling
    
    ps2: Enable via overlay
    
    Change-Id: I42bc05ae1c22443cca782ac1ae66d5d5bb4ac858
    
    Conflicts:
    	src/com/android/phone/CallFeaturesSetting.java

commit 13d7fb84da237e793cf9527f15e469dd612b6b9c
Author: Lin Ma <lma@cyngn.com>
Date:   Mon Mar 30 17:38:33 2015 -0700

    TeleService: pass phone ID to APN setting
    
    Conflicts:
    	src/com/android/phone/CdmaOptions.java
    
    Change-Id: I3df6c42bc97a68f9e58431e0585a957056912e37
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/96439/

commit 1a58b65756903c3f89af8f8afdb4c878645c69e7
Author: LuK1337 <priv.luk@gmail.com>
Date:   Wed Apr 29 13:31:53 2015 +0200

    msim: Fix FC on opening "calling accounts" in Dialer settings
    
    Variable sir seems to be null on some msim devices.
    
    Change-Id: Ia046e04da2edc0c06ed91a5878111f8e98f23b3b

commit 96e25bf7c4ccbd9f53b9159845c1d6c24c8f020a
Author: cretin45 <cretin45@gmail.com>
Date:   Thu Apr 23 12:25:12 2015 -0700

    TeleService: Remove HomeAsUp arrow for nested pref screens
    
    This brings the msim settings in line with single sim.
    
    Change-Id: I968efb7abcb8cfe85bff5593ac95794d6879a8b6

commit a6e104d3c0b828a9db9e9cdc97584b1f80c4b8a5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:54:57 2015 +0300

    Automatic translation import
    
    Change-Id: I206eaf2e5ce060a9b64f66622df993f7c323679a

commit bf38c64dd759e59741659fcd8ccb07cd06259c04
Merge: 96e25bf a6e104d
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 21:44:34 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1
    
    tion between NB AMR (the default) or HE-AAC for the encoding of call recording audio. Also changes the output format of the file appropriately (NB AMR now uses the NB_AMR output format and HE_AAC chooses the MPEG_4 output. File extensions are adjust accordingly as well).
    This was in reponse to people complaining the quality of call recording audio is poor. It's noticibly better using HE-AAC, but filesizes are larger.
    
    Change-Id: I31f4a57042cf9e221ea2292922f071c955170e1e
    
    PS: Imported from kitkat and made working for lollipop.
    
    Signed-off-by: BlackDragon <blackdragon.fusionteam@gmail.com>
    
    Conflicts:
    
    	res/values/cr_strings.xml
    	src/com/android/phone/CallFeaturesSetting.java
    
    Conflicts:
    	res/values/cmr_strings.xml
    	src/com/android/phone/CallFeaturesSetting.java

project packages/wallpapers/Galaxy4/
commit 2da4de9375bf3f45e658e314def00964fe97ed4a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:55:06 2015 +0300

    Automatic translation import
    
    Change-Id: Id6f2dd34ce930169ab08343e86a88bf27375e024

project packages/wallpapers/PhaseBeam/
commit 10e4dbe04de8633ea7d97898a0b0f39b6676300a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:55:09 2015 +0300

    Automatic translation import
    
    Change-Id: I436f5eef4b494986f7c1f96866a9595ecf4667b9

project packages/wallpapers/PhotoPhase/
commit 6caa42980095431987345f0dce8d5c025bc5c44a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat May 2 02:55:13 2015 +0300

    Automatic translation import
    
    Change-Id: I14c3c1fbb67fdb189f8f03275e239f5536953237

project system/core/
commit 3070e37c91b673b4833ec05d0f9b3341ef6d5347
Merge: a62d616 35493c4
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 19:20:27 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project vendor/cm/
commit b2c60c1bbf60c04947d09a511b1c8cfd5eaa07c3
Author: bmc08gt <brandon.mcansh@gmail.com>
Date:   Wed Apr 29 19:40:54 2015 +0200

    Bump CyanogenMod version in CONTRIBUTORS.mkdn
    
    Change-Id: I8fa4b8b53af6ec1333f05f42d908b3e28a7bf08b
    Signed-off-by: bmc08gt <brandon.mcansh@gmail.com>

commit 8688a958b7fc671710ebb3083248f946e28a41c5
Author: Brin Taylor <uberlaggydarwin@gmail.com>
Date:   Sat May 2 08:24:32 2015 +0930

    vendor: cm: yet more updates to contributors
    
    * u-ra sold his devices.
    * nard now does d2
    * unbreak the formatting (damn comma's)
    
    Change-Id: Ic2dfde51e419f95a72bff238d1542b17728f9ac7

project vendor/cmremix/
commit 9d835a583eca69e098adadab0e78e2b4b3e23ae8
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Mon Apr 27 16:05:30 2015 -0700

    Update changes from build
    
    Change-Id: I82e8efffee4589bb7dcd1add6545ae1e749859cc
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	config/cmremix_sm.mk
    	products/sm_hlte.mk

commit d387b02b5cb978cfde5e8f961ca5795502c24f2b
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Mon Apr 27 03:23:56 2015 -0600

    Remove flag -fprefetch-loop-arrays
    
    Change-Id: I4ab35836b460c20d75bcc2e08fdb6a194c1b9064
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 81558032eef8ae5aa151945cdc9246d73bea086a
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 28 02:33:37 2015 -0700

    sm.mk : disabled bunchs of violate strict aliasing modules for CM-12.1 Base

commit 9be9c8c6e43dd219a704da31e62df0f6b058a933
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Apr 28 13:36:53 2015 -0700

    Add a option to disable vectorization flags for bluetooth (1/2)
    
    Change-Id: I90f1e2489d16096401000b00d530805db470a32b
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	config/cmremix_sm.mk

commit 02a3112c45ba1d05642cc606d80eb716580abef1
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Apr 29 13:00:34 2015 -0600

    Fix bluetooth crashing when using -O3 optimizations
    
    Force -Os
    
    Change-Id: I497cbdd5f52dbd24b7acc1f1ffe165eff3d6e4dd
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 3a8b05a5be7311c239eb5108f69bc85e0d438788
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Apr 29 23:12:23 2015 -0600

    Remove extra kernel gcc version info writing to build.prop (2/2)
    
    No longer needed with
    https://gitlab.com/SaberMod/pa-android-packages-apps-settings/commit/9590f426e7986e64d68ae80b4ac5c6409f4c88b5
    
    Change-Id: Icc3722b2f453f74c9aadde7998cf0faab35f7230
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit b0e6ca7a43a1943ce35f32bfb3d56690580e773d
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 30 10:13:45 2015 -0700

    Add strict-aliasing for optimization options.
    
    Change-Id: I903132993e75cfce35cee8ba1d21f1f6725322f1
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	config/cmremix_sm.mk

commit 3f095d85423846ece708c82024d97ef02da071c1
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 30 10:15:58 2015 -0700

    Fix bluetooth for good! (1/2)
    
    Change-Id: Ia09b64351cb6b5a2353160252567f83e10d38690
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	config/cmremix_sm.mk

commit 4a531d59b781160753f1fed38231d912e857cf17
Author: ZION959 <ziontran@gmail.com>
Date:   Fri May 1 00:22:12 2015 -0700

    clean up

commit 4f3c8ae460f8637f28e51d5f17d3c40f4eb008f6
Author: ZION959 <ziontran@gmail.com>
Date:   Mon May 4 12:58:12 2015 -0700

    Revert: Remove extra kernel gcc version info writing to build.prop (2/2)
    
    No longer needed with
    https://gitlab.com/SaberMod/pa-android-packages-apps-settings/commit/9590f426e7986e64d68ae80b4ac5c6409f4c88b5
    
    Change-Id: Icc3722b2f453f74c9aadde7998cf0faab35f7230
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com> (reverted from commit 3a8b05a5be7311c239eb5108f69bc85e0d438788)

project vendor/samsung/
commit ea5f4eec1ca017bb68aa44ece8bda5b460674f7d
Author: Dave Daynard <nardholio@gmail.com>
Date:   Tue Apr 28 21:00:02 2015 -0400

    d2gsm: Use rilblobs from AT&T NJ1 release
    
    Change-Id: I390995911423d7c28995e9d4ebfa76f171d11922

commit 446757d8460406a6a486fc85fedd1351425337a2
Author: Dave Daynard <nardholio@gmail.com>
Date:   Tue Apr 28 21:14:16 2015 -0400

    d2-common: update camera firmware
    
    Change-Id: I462cc98c9e3e735adc3c9005dcd165ef1bfb3250

commit d33393e2226c6e4b042b8cc62db1549e1460b2a2
Merge: 44cb70e 446757d
Author: Shareef Ali <shareefalis@cyanogenmod.org>
Date:   Tue Apr 28 21:21:13 2015 -0400

    Merge pull request #611 from nardholio/cm-12.1
    
    update d2 blobs

commit 0be23a84935f289632356c25f7bb5812b1d655bd
Author: Dave Daynard <nardholio@gmail.com>
Date:   Wed Apr 29 19:12:59 2015 -0400

    Revert "d2gsm: Use rilblobs from AT&T NJ1 release"
    
    This reverts commit ea5f4eec1ca017bb68aa44ece8bda5b460674f7d.

commit 9302518c8cea767f70018d66700b1b1a2673ba19
Merge: d33393e 0be23a8
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Wed Apr 29 18:20:53 2015 -0500

    Merge pull request #612 from nardholio/cm-12.1
    
    Revert "d2gsm: Use rilblobs from AT&T NJ1 release"

commit cffa4d4fbc4fa4c23230adc7f110a8564b4d67da
Author: Tony Layher <layhertony@gmail.com>
Date:   Sat May 2 17:51:19 2015 -0400

    trlte: update camera HAL
    
    Change-Id: Icb98078726cbffc6d5e392ff7e3729df42a00314

commit 88fffde3547bd4cacfafbf13619f815e0d908a9d
Merge: 9302518 cffa4d4
Author: ciwrl <ciwrl05@gmail.com>
Date:   Sat May 2 14:54:57 2015 -0700

    Merge pull request #613 from slayher/cm-12.1
    
    trlte: update camera HAL
