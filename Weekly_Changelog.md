
project bionic/
commit d0e6a2759af7c0264ba49f480d001ca6be5e4944
Merge: 9c38646 0e825a7
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:53:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project build/
commit 65183542835ff3fbdc36f468f993dfb102522cab
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 01:21:25 2015 -0700

    build: ignore recovery size (JustArchi)

commit c144ff9eee538ac6f46c443ad3776e4f530e1bde
Author: Łukasz Domeradzki <JustArchi@JustArchi.net>
Date:   Mon Mar 9 21:04:10 2015 +0100

    Build: Allow board to specify additional flags

commit a7bacfbf3968b3800eeb520963337d8d4202d01c
Author: Łukasz Domeradzki <JustArchi@JustArchi.net>
Date:   Sun Mar 15 21:38:54 2015 -0700

    [1/2] ArchiDroid Optimization
    
    port to CMRemix (Thanks JustArchi)

commit bbd17818153811e4225864fda15d957f6ec52c12
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 23:10:57 2015 -0700

    more tests

commit cd2284d42598e71e35cdd71ee3c283705721c730
Author: MaDc0w <MaDc0w@pac-rom.com>
Date:   Fri Mar 20 00:29:11 2015 -0700

    build: Rainbow unicorn puke [1/2]
    
    Change-Id: I393dd013194d73b293b361a42d42fa171ceee837
    
    Conflicts:
    	core/Makefile
    	envsetup.sh

commit d0e74143cf26859e1ffca9668e08e992f1a26b62
Author: JoseGalRe <josegalre@gmail.com>
Date:   Fri Mar 20 00:31:49 2015 -0700

    build: move chromium call...
    
    Change-Id: Ia91e750470f4af67487bf3e52d208bedc3a585dd
    
    Conflicts:
    	core/Makefile

commit 96a213ed1c87018a0b2dd3b77013ab6313b8da84
Author: Lokesh Chamane <lokesh.c703@gmail.com>
Date:   Sun Mar 8 16:29:37 2015 -0400

    build: Prebuilt Chromium files check
    
    Change-Id: Ic12f1d2559417f74af787e635d1ab882d07d9d00
    Signed-off-by: Lokesh Chamane <lokesh.c703@gmail.com>

project cmRemiX/
commit 7aed5d1c13129920018e80e2e3562a81dff59ff7
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 11:51:18 2015 -0700

    track opt_net_wifi

commit 89bd5a728ade13a0ac728778da3effe8bf961cff
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 14:51:55 2015 -0700

    update qcom clang path

project device/qcom/common/
commit 4ed36a9a7391dc20ec4f1ee2ac8794c0b9ec3c9d
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:47:59 2015 -0500

    power-8226: Add support for system performance profiles.
    
    Change-Id: I2f5002ffa0b1c63486056023a3cc6137559bcebd

commit 5a31d99fe1ce79056cf26972b698eeca4cddf33f
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:51:16 2015 -0500

    power-8226: Various updates to Power HAL
    
    Change-Id: If266f0a95a85bfc8dc8458ce7d71e569fa715c2f

commit c534f6e5c5621fe21cec6ebe7e2d3a896c80418e
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:52:35 2015 -0500

    power-8226: Add support for POWER_HINT_LOW_POWER
    
    Change-Id: Id25095ed549a84c07167f87f62f4e8add9a4cfec

commit 94ed698a08bcf78a7692de459c067be540b32603
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:54:12 2015 -0500

    power-8226: Remove the HMP boost hint
    
    Change-Id: I134c2656d806978ef683f70980be27d2bc60eb51

commit 63f475188ee463f8806ae9fc268333aab310d8af
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:55:01 2015 -0500

    power-8226: Increase the boost a bit
    
    * eliminate a lot of jank. We're racing with input boost here.
    
    Change-Id: Ibce4ec734b4a9df82277b8e79425a87454b58dcd

commit 28310b2b130ea26372e066c85e868c70f332c5a2
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 19:56:13 2015 -0500

    power-8226: Remove unnecessary hint
    
    * This has the unfortunate side effect of actually *enabling* KSM,
      which we don't really need on this hardware.
    
    Change-Id: Idc3960fcb60169c2429d74309de50e52083664da

project device/samsung/hlte-common/
commit ff4324997d11580b2bfd6ad35590908491542edc
Merge: e12a8f7 76aaf52
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 01:46:56 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0
    
    6a60b71028a981d0885b
    
    Conflicts:
    	rootdir/etc/fstab.qcom
    
    Conflicts:
    	rootdir/etc/fstab.qcom

project device/samsung/qcom-common/
commit 4633830a2691185e18e93a64629599bc4d05d877
Author: Matt Filetto <matt.filetto@gmail.com>
Date:   Wed Nov 26 03:00:00 2014 -0800

    mms: add overlay for Claro PR carrier
    
    * Set correct UAProf and max image size configs
    
    Change-Id: Icd13e1afbed4e13c644d49a5a7b09215cbf58b94

project device/samsung/trlte-common/
commit a8b7f6d616845ef469a1367eb1c9c9b27058747a
Author: Tony Layher <layhertony@gmail.com>
Date:   Mon Mar 16 22:50:48 2015 -0400

    trlte-common: Use low latency for primary
    
    Change-Id: I8938139b886eb1ff83500dbdc73441fda2d11e14

project device/samsung/trltexx/
commit 695e9a0b50d33fe3dad7c8e41980fceab21b144a
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Thu Mar 5 15:30:08 2015 -0400

    add support 910G
    
    Change-Id: I7e43f0814da00866d3f100af2d5f1f341c988715

commit e86bc1f567f19f2c37e90d781f7487864659cbf7
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Mon Mar 16 19:36:02 2015 -0400

    fix string
    
    Change-Id: Id81f5647343e21d9bc2f73c0b79a494b670da717

commit e7efc5bd406dc8170c8eeb4b4cc05d87851a5af6
Merge: 19e7f54 e86bc1f
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Tue Mar 17 01:10:54 2015 +0000

    Merge changes Id81f5647,I7e43f081 into cm-12.0
    
    * changes:
      fix string
      add support 910G

project external/bluetooth/bluedroid/
commit 0c288384e612e0201995f6524a8924d000ec9a46
Author: Andre Eisenbach <eisenbach@google.com>
Date:   Mon Jan 26 13:49:36 2015 -0800

    DO NOT MERGE Change pairing_cb to assume temporary pairing by default
    
    When pairing takes place, the pairing_cb.is_temp flag indicates whether
    a pairing is temporary or permanent. Link keys are not stored for
    temporary pairings. Since this is a "positive" flag, resetting the
    pairing_cb control block (ex. memset to 0), it will assume persistent
    pairing by default. Under certain circumstances, this can lead to a link
    key being stored for temporarily secured connection.
    
    This patch reverses the flag to be a "negative" flag. Renamed to
    "persistent_bond", the default 0 meaning is now used to indicate a
    temporary bond. If the lag is not properly set now, it will default to a
    temporary bond and will not save the link key erronously.
    
    Bug: 18345373
    Change-Id: I06b1ba9331a70ebc29f4437bf836164658dec5ae

commit 64f8d7fb105f999b7e60ca0cc8328350c24f4f09
Author: Nitin Srivastava <nitinsr@codeaurora.org>
Date:   Fri Nov 28 10:21:15 2014 +0530

    Bluetooth: Update call state before opening SCO.
    
    This change makes sure to update the current
    call state before opening SCO connection when
    incoming call is answered. Some car kits are
    strict in checking this sequence and go in
    bad state if not done this way.
    
    Change-Id: I90aa899b89c7ea5efc57281d26ce65f5e291e63b
    CRs-Fixed: 763881

commit 1d82011c84cdb5e948eb1871267cd0801d32b856
Author: venkata Jagadeesh <vjagad@codeaurora.org>
Date:   Tue Jan 13 16:56:33 2015 +0530

    Bluetooth: GAP: Don't send auth req from connection complete
    
    Restrict the auth req immediately from connection complete as
    some remote IOT SOCs going to bad state if auth req and remote
    features req are going simultaneously from DUT.
    
    Change-Id: I947773404bd905f9ee155c4e31bdad5f08da24ee
    CRs-Fixed: 783203

commit b20e9c3f741a67ad1248af0dae2b041b2c591109
Author: Ayan Ghosh <abghosh@codeaurora.org>
Date:   Wed Jan 21 15:11:48 2015 +0530

    Free Browse packet
    
    Free Borwse packet in AVRC layer once the same is
    copied to BTA for further processing.
    
    CRs-Fixed: 785286
    Change-Id: I8037a649cff5a1e527c28ba36999a1bed34d315a

commit 5e99e49bb0c62169ac7a1f6a30ff16fa9fa38507
Author: Nitin Shivpure <nshivpur@codeaurora.org>
Date:   Thu Jan 15 20:15:07 2015 +0530

    Bluetooth: Use correct sniff configuration for PAN & HS
    
    - Using correct sniff table entry for PANU & NAP role.
    - Using correct sniff table entry for HS role.
    
    Change-Id: I95c302dd46cdcc63058c9cb3de17fdfd6ffe8d2e
    CRs-Fixed: 788993

project external/dhcpcd/
commit e499680f0832d6f959a3d5290085d61cce0f6907
Author: Erik Kline <ek@google.com>
Date:   Sat Nov 15 04:24:40 2014 +0900

    Fun with buffer overrruns.
    
    In get_option(): don't read past the end of the option buffer.
    
    Also add a small unittest to verify sane behaviour for the above.
    The dhcpcd code is not easily refactored into a library, nor is it
    entirely possible to include some header files directly since some
    structures use C++ reserved keywords ("new") for variable names.
    
    In print_option(): use of snprintf() returns the length that
    /would/ have been written.  Add checks that the output buffer
    is not overrun when printing.
    
    Bug: 18356137
    Bug: 18356135
    Change-Id: I0f907b8a952208749226ba034a416d773e068f8a

project external/flac/
commit 47c292e8e05dfde61724ddcd119ff779d73607ed
Author: Robert Shih <robertshih@google.com>
Date:   Mon Jan 5 17:35:54 2015 -0800

    libFLAC: merge master from Xiph
    
    remote: https://git.xiph.org/flac.git
    commit: 775eb93
    
    Bug: 18872897
    Bug: 18910747
    Change-Id: I6e450e44c96b97c3323e428b9e6d420422f24a4e
    (cherry picked from commit 31e4f3166a91a2ebb34f643787122a638d9f1471)

project external/okhttp/
commit 24aad7677073f7c2116b105e53ba2eaa05917209
Author: Alex Klyubin <klyubin@google.com>
Date:   Tue Nov 18 17:45:01 2014 -0800

    Fix a bug in OkHostnameVerifier wildcard handling.
    
    Wildcard domain name patterns of the form *.remainder are supposed to
    match domain names that exactly match the remainder. Due to a bug,
    the match was not exact but rather a prefix match: domain names
    starting with the remainder would match too.
    
    This CL fixes the issue.
    
    Bug: 18432707
    Change-Id: I2639ff51cabcbd395d4f30a9c69f9895738e0acf

project external/skia/
commit 2e87b697d21be8446c70888a1ac16733ee7bcd35
Author: Wei Wang <wangw@codeaurora.org>
Date:   Mon Mar 2 10:20:59 2015 -0800

    Bring back NEON optimized blitter S32_Opaque_D32_filter_DX
    
    disable Clamp_S32_Opaque_D32_filter_DX_shaderproc_neon
    for non-decal case
    
    Change-Id: I426c3fed55c2a7f6d9e024b0af266da0c2690abc

project external/sqlite/
commit fc4f2d6ce8eae9539fb8245473abf8468a442653
Author: arter97 <qkrwngud825@gmail.com>
Date:   Fri Mar 13 17:44:38 2015 +0900

    Upgrade to SQLite 3.8.8.3
    
    Downloaded from http://www.sqlite.org/2015/sqlite-amalgamation-3080803.zip
    
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

project frameworks/av/
commit 4bd7b86d9ecfb111bdff262d769f20125990842a
Merge: ba94bd7 649b5fb
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:53:07 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

commit 08328f15856b06d1f4227cff39b3568227445826
Author: Eric Laurent <elaurent@google.com>
Date:   Wed Nov 5 12:15:36 2014 -0800

    IAudioPolicyService: bound array size in queryDefaultPreProcessing
    
    Bug: 18226810.
    Change-Id: Ib8e2bfe835a8681aac50bf23161db14e50c9a124
    (cherry picked from commit 74adca9ad30b7f8a70d40c5237bade0d16c4ea58)

commit 23423d36ec40c84294fc972d51ff612eb5919a62
Author: Eric Laurent <elaurent@google.com>
Date:   Tue Oct 28 15:46:45 2014 -0700

    audio policy: validate stream type received from binder calls.
    
    Bug: 18001784.
    Bug: 18002005.
    Change-Id: I8efa674dceff5a6e10251b1c7a55e9bb2d532395

commit ba32742fcd2a4a1e6b5bf25aec605eedde540ce3
Author: Eric Laurent <elaurent@google.com>
Date:   Fri Feb 6 10:44:24 2015 -0800

    audio policy service: fix possible memory overflow
    
    Add limit on number of audio ports and patches requested by
    listaudioPorts() and listAudioPatches().
    
    Bug: 19261727.
    Change-Id: I21dfdf11cf805734cc3b7b2a85762c5598f60580
    (cherry picked from commit 1d670b11313250442455a22f1056ad649d607fb2)

commit da31859f7ce22580a88f67145618f8caa0edf888
Author: Mike Lockwood <lockwood@google.com>
Date:   Wed Nov 12 14:20:06 2014 -0800

    MTP: add strict bounds checking for all incoming packets
    
    Previously we did not sanity check incoming MTP packets,
    which could result in crashes due to reading off the edge of a packet.
    Now all MTP packet getter functions return a boolean result
    (true for OK, false for reading off the edge of the packet)
    and we now return errors for malformed packets.
    
    Bug: 18113092
    Change-Id: I8be3df2c36fe730ad64e7ea9a5ee856ad815b904

commit f4d983a88a57a023dafdbd483a95b269a707ccf5
Author: Mike Lockwood <lockwood@google.com>
Date:   Wed Dec 17 12:22:36 2014 -0800

    Fix bounds checking for GetPartialObject command
    
    GetPartialObject has only 3 arguments, whereas the 64 bit version takes 4.
    
    Bug: 18786282
    Change-Id: Ica67fdf9569372b89d379c8b0f3e0a64dacf150a

commit 130f0c4cd4138ffd179541642820be1639f43b1a
Author: Marco Nelissen <marcone@google.com>
Date:   Fri Jan 23 10:55:25 2015 -0800

    Fix MTP delete
    
    Bug: 18836972
    Change-Id: I55335abc6181ba3a861773cd13ee3a72a179a926

commit 1baf67ab3fb4f0f36ef1aa7b71b6bf28efd250d2
Merge: 4bd7b86 130f0c4
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 09:00:06 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

commit c498eab8dfe6ce639896b28eb397e7315048a9cc
Author: Arne Coucheron <arco68@gmail.com>
Date:   Mon Mar 16 05:37:50 2015 +0100

    Revert "soundpool: reuse channel for same sample if available"
    
     * Causing issues with touch tones. Randomly loosing them
       altogether, and skipping tones when typing fast on the keyboard.
    
    This reverts commit 1abd0c511a4509074097707945681154900b50de.
    
    Change-Id: Ib1c02f1b30750dc1600371656541b41947e889ab

commit cf8c5de74aecfa3dbec40dd8cefafbe17655c0c8
Merge: 1baf67a c498eab
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 20 20:57:41 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

project frameworks/base/
commit 76231c40afb2dc7ada16f16fbbfb5b10c3519b3e
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Mar 12 09:23:00 2015 +0100

    Preference: allow to get list of preferences from preference group
    
    Change-Id: Ifecaeb43c0a9beb79869e812ce41fafc789ba434
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit 72591ee2cdd76137a65b818d04c17a9121dc0e7b
Author: Steve Kondik <steve@cyngn.com>
Date:   Fri Mar 13 14:12:06 2015 -0700

    Revert "Bluetooth: Change userhandle to current from ALL"
    
     * Fixes death spiral when switching users.
    
    This reverts commit fbc6c35295775f600f1b12d062a9656a998c1978.
    
    Change-Id: Ie944f965f4a128d539668e4e288fbac7246a8f9d

commit c98e08cd02f8be7fb7a883258ad0936c904a4850
Author: Steve Kondik <steve@cyngn.com>
Date:   Fri Mar 13 15:31:50 2015 -0700

    livedisplay: Fix issues when using multiple users
    
    Change-Id: Id0732b23aa324e92c6d0aaa17e64e3c76cd89450

commit 99e8aea70806f3976d725d27e76d8d140c67cf77
Author: Daniel Broms <daniel.broms@sonymobile.com>
Date:   Mon Sep 29 15:32:03 2014 +0200

    Handle NULL keys and NULL values in MediaDrm JNI HashMap
    
    If getKeyRequest() of MediaDrm was called with a HashMap containing
    NULL keys or NULL values then the mediaserver crashed.
    
    This modification adds NULL checks and throw
    IllegalArgumentException as expected.
    
    Change-Id: Ide82efe0f6bd28c8ac3f9aa048d9794f2ccc8fac

commit ebf94ad6c80d3512fa307c4a9e64f7d39a731d15
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 13 16:40:49 2015 -0700

    Themes: Change themeChange config value to 0x300000
    
    This value is ActivityInfo.CONFIG_THEME_RESOURCE and
    ActivityInfo.CONFIG_THEME_FONT ORed together.  Any future theme
    config flags that are added should be ORed with this value so that
    any app that declares themeChange as a configuration change it will
    handle will not be restarted when only one theme change flag is
    set.
    
    Change-Id: I620ab62a54f97c20e03369adf01ba817fada51de
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/91317/

commit ef0f03d7ce53aaefc715e4cd13cf67f2b6f9d720
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:09 2015 +0200

    Automatic translation import
    
    Change-Id: I0c07961ed75079f1b525cb1f6c59f6e542248e1e

commit a6e487d6e8e891f1cc3815877099c12124915fef
Author: chickenfactory <micah.chickenfactory@gmail.com>
Date:   Sat Mar 14 15:00:00 2015 -1000

    fix link of ringer and notif volume [1/2]

commit ca7bf9b9f730fa0f84e43430d135dda9d935f3e2
Author: Steve Kondik <steve@cyngn.com>
Date:   Sun Mar 15 12:44:53 2015 -0700

    livedisplay: Updated icon from Asher
    
    Change-Id: I093eb6925b939fa37f0d67d2a42b24fa2494b98c

commit a44b9e701356161609afe3d4ac4e15b8bf0552ba
Author: Bo Huang <bo.b.huang@intel.com>
Date:   Fri Oct 17 17:15:32 2014 +0800

    ADB not detected when run "adb root" with userdebug version.
    
    Reproduced step:
    1. Mtp/Ptp is enabled;
    2. Connect DUT to PC via USB cable.
    3. Input 'adb reboot' to reboot DUT.
    4. Wait a moment and run "adb root"
    5. Input "adb devices"
    
    [Expected Result]
    listing all the devices connected in adb.
    
    [Actual Result]
    adb devices not found.
    
    Rootcause analysis:
    The cause is that MtpReceiver missed some USB disconnection event
    (ACTION_USB_STATE with value USB_CONFIGURED=false). Then MtpService was
    start twice but no stop method called.
    
    When DUT is power up, there were a lot of sticky broadcast in message queue. Regarding USB_STATE intent, the latest one can replace older one.
    While issue happened, almost 23 messages was in front of queue. Finally, Mtpreceiver got last one with connected: true configured: true.
    12-31 19:00:43.870 553 588 V ActivityManager: Enqueueing ordered broadcast BroadcastRecord
    {3cd49633 u-1 android.hardware.usb.action.USB_STATE}: prev had 23
    12-31 19:00:43.870 553 588 V BroadcastQueue: ***** DROPPING ORDERED [background]: Intent { act=android.hardware.usb.action.USB_STATE flg=0x20000010 (has extras) }
    12-31 19:00:43.870 553 588 D UsbDeviceManager: after broadcasting Intent { act=android.hardware.usb.action.USB_STATE flg=0x20000000 (has extras) } connected: true configured: true)
    
    Change-Id: Id074518416836936840319ddad476b2d40efeff9
    Signed-off-by: Chen, Yu Y <yu.y.chen@intel.com>
    Signed-off-by: Bo Huang <bo.b.huang@intel.com>

commit 6f961a161f8b1704d9e7491ebdfcdef49f904d6a
Author: ferro_chang <ferro_chang@htc.com>
Date:   Mon Mar 9 18:03:36 2015 +0800

    To call TypedArray.recycle() when we are done with the array.
    
    Change-Id: I6d672ce6c4e6521d82ef873ce69076b1f1cded56

commit db433661681050b2043bcaa8ae79bc80f98e373b
Author: tsubus <tsubus@ilwt.org>
Date:   Sat Mar 14 23:47:03 2015 +0100

    Do not start music app when headset is unplugged
    
    Change-Id: Ic56ba6c30a72deaf119da40e65ca83a9dcc35c43

commit d561841a619ddc7653ab40dce4750571f1cad583
Author: Gianmarco Reverberi <gianmarco.reverberi@gmail.com>
Date:   Mon Mar 16 20:02:15 2015 +0100

    SystemUpdateService: enable service but lock its receivers [1/2]
    
    Added a check for ensure that disabled components are not
    re-enabled at runtime
    
    Added code for forcing enable of previously disabled components
    
    Change-Id: Icfcfa26ccb85028d32edbb5cdb3dd7cdae85b720
    
    Patchset: 4
    http://review.cyanogenmod.org/#/c/91579/

commit f934749989f5b273c966680cd9d6d5205a222797
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:10:23 2015 -0700

    Frameworks/base: Fix missing cast
    
    Without a cast, the division is integer division.
    
    Change-Id: I050e53778de8b1591a0be16ebbee8eed70eb1528

commit 3dac67c7c984a7f053760d75b645258ce909d8bc
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:19:43 2015 -0700

    Frameworks/base: Fix always-false equals
    
    Rect != Insets.
    
    Change-Id: I3d4ff890608e446b51f09a1b633af742f0c069d4

commit 6f947a64993c28d317853883d46a06998ad48954
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:38:59 2015 -0700

    Frameworks/base: Fix a hashCode implementation
    
    Equals uses Arrays.equals. That means two responses are equal if
    the content of the data arrays is equal. By convention, the hash
    code of those objects should agree. In that case one cannot use
    hashCode on the array (which is the identity hash code).
    
    Change-Id: Icce8e2e71e9142421f5dac8a0ee8a211623fb704

commit 4ca0904393f450856104dc4446b0f8f7aba924b8
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:07:19 2015 -0700

    Frameworks/base: Fix null-pointer check
    
    Change-Id: I715a21c313e909ae654e0c1aa67bdf7bcd89de76

commit ddb5d4fa8bc0777dba7fb09dd24c03e28ba0ce6f
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:39:21 2015 -0700

    Frameworks/base: Use equals for Integer comparison
    
    Integer == is dangerous, as equal objects may not be identical
    objects. In fact, MediaFormat.setInteger was creating a new object
    every time.
    
    Change MediaFormat.setInteger and setLong to use valueOf, which
    may reuse returned objects.
    
    Change-Id: Iedcc6003adbf05c0c870aa4b3ada7f181a5b870e

commit 60495a5af954116c99d10d6ecb44c28fa216381b
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:57:30 2015 -0700

    Frameworks/base: Check before foreach in Script
    
    According to the if below, ains == null is potentially valid. But
    the foreach loop would throw a NullPointerException.
    
    Change-Id: I4460fb1357eaa3abfe0ab9a21effb608f474ab51
    
    Conflicts:
    	rs/java/android/renderscript/Script.java

commit 761a83bf8ac051016b4d593e074796b9ebc4b63c
Author: jinchul.kim <jinchul.kim@lge.com>
Date:   Fri Mar 13 15:27:42 2015 +0900

    keep mDefaultDisplayMetrics from concurrent modification.
    
    getDisplayMetricsLocked can be invoked concurrently, it can cause
    concurrent issues like ArrayIndexOutOfBoundsException.
    
    Change-Id: I816eb4b276e7872c8a1964b6389a6f1238f51e48
    Signed-off-by: Jinchul Kim <jinchul.kim@lge.com>

commit 19ca7cec800b2a404ff625f0ecbba6f23c1a4a09
Author: Utkarsh Gupta <utkarsh.eminem@gmail.com>
Date:   Mon Mar 16 17:21:39 2015 +0530

    Lockscreen visualizer: Disable out animation
    
    Change-Id: Ic9766f1b06093caebec575aea689a018498a3aa8

commit 19b0b4ac3d4cd6e1fa11cb8c352356853c1fd12a
Author: LorDClockaN <davor@losinj.com>
Date:   Mon Mar 16 15:20:29 2015 +0100

    Fix SystemUI FC on theme change (recreateStatusbar())
    
    Heads Up view was getting removed while it wasn't
    attached to window manager
    
    Also remove extra ;
    
    Change-Id: Idd439cb3eb387db05ad30c5129a75fb90a21e289

commit a44a01ba97009299278bfe6f1938409a887a4720
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 16 16:47:24 2015 -0700

    SystemUI: CellularTile support multi-sim
    
    Change-Id: I6f2ee24e512260f90036376ef7763c87f048922d

commit 5d379fb39170e138513833df8d1591dbe62c7b99
Author: PrimeDirective <activethrasher00@gmail.com>
Date:   Mon Aug 5 14:24:43 2013 -0400

    fix cursor leaks in F_B
    
    my previous commit was submitted before i was finished.  Here is an updated version.
    
    Change-Id: I3e371e0cc192c3be01402ee2c2884157e469c3f2
    PS2: missing bracket

commit 74a00f52276be6b1d2c64bd4262a98547c1c4147
Author: nuclearmistake <nuclearmistake@gmail.com>
Date:   Thu Mar 12 09:14:18 2015 -0400

    LEARN TO COMPUTER FFS... IT'S WHITESPACE, NOT ROCKET SURGERY.
    
    Change-Id: Ib54d9cdd3f617ba3cbca3a43f38fb262a3bbee40

commit a29ec462877304dd705750f179c5c9377a01a196
Author: BigBrother1984 <stevewatersy@gmail.com>
Date:   Tue Sep 3 02:40:35 2013 -0400

    ZygoteInit: increase GC threshold amount when preloading to postpone GC
    
    Patch Set 2: Hardcode it better to 1MB.
    
    Change-Id: I61890f056b9ef347af9334a0050a0f3fbe8c04fb

commit 945aa746494a8ef1e6f269257248f23b508f5cfc
Author: Martin Wallgren <martin.wallgren@sonymobile.com>
Date:   Wed Aug 20 14:58:58 2014 +0200

    Prevent resource leak in YuvToJpegEncoder
    
    SkWStream is never deleted before going out of scope
    
    Change-Id: I522b8040e2d2f5fdeac6dbe2adbd8ae840971d2e

commit ec11aebe5908ffef40644218bd24ec4d0e40fccd
Author: Bernhard Rosenkränzer <Bernhard.Rosenkranzer@linaro.org>
Date:   Wed Nov 12 14:45:58 2014 +0100

    Fix unused variables.
    
    The return value of jniRegisterNativeMethods is checked only in
    LOG_FATAL_IF, which defines to nothing in the LOG_NDEBUG
    case.
    
    Fake a use of the 'res' variable to shut off warnings when LOG_NDEBUG.
    
    Change-Id: I8263610f327c56897f76796fe1fbc2b325b0559f
    Signed-off-by: Bernhard Rosenkränzer <Bernhard.Rosenkranzer@linaro.org>

commit c10f843695fe112202924eae5be7503f277de4a4
Author: Lajos Molnar <lajos@google.com>
Date:   Thu Nov 20 16:16:55 2014 -0800

    media: fix isSupportedFormat for integer frame rate
    
    Bug: 18473065
    Change-Id: I670cc043d3cb117c26921cb639ff9eecc8f14b0a

commit be4c50ec782736a2043cb5d4895d421140372d4c
Author: Karol Wrótniak <karol.wrotniak@droidsonroids.pl>
Date:   Thu Nov 27 21:29:15 2014 +0100

    Fix PhoneStateListener constructor javadoc.
    
    Removed sentence in visible javadoc of #PhoneStateListener() which
    was useless because it referred to another hidden constructor.
    
    Change-Id: I14a956ac29881000e48bf31e0090e9e1f93bf6e3

commit d04c056c11866907e40a5fba4abc4b52a5335e75
Author: Elliott Hughes <enh@google.com>
Date:   Mon Dec 8 20:47:11 2014 -0800

    Fix typo.
    
    Bug: https://code.google.com/p/android/issues/detail?id=78422
    Change-Id: I0dfbb74334e126062660831a4e01817dde068b56

commit 554da9ad2c7de06d23935ae9594e59add8dc2640
Author: minho.choo <minho.choo@lge.com>
Date:   Fri Dec 12 16:13:55 2014 +0900

    Fix bugs regarding delay the dispatching of non-wakeup alarms
    
    checkAllowNonWakeupDelayLocked() method determines that delay the dispatching of non-wakeup alarms.
    (there are no wakeup alarms and the screen is off, it can delay until the future.)
    
    if there is any pending non-wakeup alarms, non-wakeup alarm delivery time is bigger than nowELAPSED.
    but, checkAllowNonWakeupDelayLocked() returns false and non-wakeup alarm is not delay until future.
    
    i think it is necessary to reverse the inequality symbol on "mNextNonWakeupDeliveryTime > nowELAPSED"
    if it isn't, Could you let me know when we get ¡°stuck in a loop¡± in the comment of checkAllowNonWakeupDelayLocked () method?
    
    Change-Id: I7e972064547f4d0a9b4175dbd4cf735b4837abfd
    Signed-off-by: Minho Choo <minho.choo@lge.com>

commit 0ce71842cc7f4b2e31616c2e7a38252f6003029b
Author: Paul Lawrence <paullawrence@google.com>
Date:   Tue Jan 6 13:11:23 2015 -0800

    Fix crash caused by toHex returning exception
    
    toHex was changed to throw an exception in
    I4986a8e806d9066129f696ab9f2e80655424e723, but its caller was not adjusted
    accordingly, causing a crash whenever an unencrypted device was booted.
    
    Bug: 18886749
    Change-Id: If0505f617001cf5e0d99cf14c8b09e6a6a377167

commit cf7366fbac3af0109e959eee935d89952724876c
Author: Neil Fuller <nfuller@google.com>
Date:   Fri Jan 9 11:43:42 2015 +0000

    Fix HttpResponseCacheTest in anticipation of an OkHttp upgrade.
    
    OkHttp recently changed the behavior of their caching with
    commit e74e3f3bf744ef7f4d8ee724a7cf2347e486cfab - it is now
    neccessary to close the inputstream (or disconnect the
    HttpURLConnection) for a response to be cached.
    
    This change is (effectively) a no-op prior to the upgrade.
    
    The behavior is undefined as to whether closing the
    input stream is required for caching. OkHttp's new behavior
    is consistent with other HttpURLConnection implementations
    tried.
    
    Change-Id: Iaf57371651296ac84850971ef60a9338cead57c0

commit 71703ae1785743c93a8dd2468bda674424f4951e
Author: Jason Sams <jsams@google.com>
Date:   Wed Jan 21 12:55:14 2015 -0800

    Fix default compute thread priority
    
    bug 16651474
    
    Compute inherited graphics default thread priority of Display.  This
    was not intended.
    
    Change-Id: I0dd9a230ce8ceba64e971b024cbe518927cd2550

commit 13a24368d04a12bb9b5df602b304da05426389c2
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Tue Mar 17 19:20:00 2015 -0700

    (1/2) Base: custom power key chord actions and delay
    
    port it to CMRemix
    
     * introduces nameless utilities and a logger class
     * introduces an action processor
     * remove qcom screenshot logging
     * allows to define actions when using power + volume down/up
     * power + volume down defaults to screenshot
     * power + volume up defaults to screen record
     * allows to define the delay when the chord action should get triggered
    
    Change-Id: I82d0d10d528b4ea2b1d34ac370ca63728d3c469b
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	core/java/com/android/internal/statusbar/IStatusBar.aidl
    	core/java/com/android/internal/statusbar/IStatusBarService.aidl
    	packages/SystemUI/res/drawable/floating_action_button.xml
    	packages/SystemUI/res/values/cmremix_attrs.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/BaseStatusBar.java
    	packages/SystemUI/src/com/android/systemui/statusbar/CommandQueue.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit b220075884217f8e92e8b5aacd8af2913c7a665e
Author: Tom Marshall <tdm@cyngn.com>
Date:   Wed Aug 13 14:24:40 2014 -0700

    Factory reset: Allow passing wipe_media to recovery
    
    - Add plumbing pieces in target services
    
    Change-Id: I3b6e224064055b2eef8c2909c7d36f9a76014d70

commit 224a736e02d460f2a75293a7a2fe18f5fa4debd2
Author: Sravanthi Palakonda <srapal@codeaurora.org>
Date:   Thu Dec 4 19:24:01 2014 +0530

    wifi:Provide UI with SIM info for EAP-SIM authentication
    
    User Interface requires the SIM information (viz. number / type
    of SIM's supported on the device), using which the respective
    authentication option is provisioned to the user. This commit
    provides the same by querying the information through the API
    exposed by the Wi-Fi framework which further interacts with
    the supplicant.This commit, defines a new class for the
    SIM information which is populated based on the information
    obtained on the query.
    
    CRs-Fixed: 775942
    Change-Id: Ifd2208e6f47f8248df084896744c67c8a5eb31ff
    
    Patchset: 4
    http://review.cyanogenmod.org/#/c/89421/

commit 9ff18f1c6fc86d6603fead068e7c6010364982b4
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 13 21:12:54 2015 -0700

    Themes: Switch themes when user changes
    
    This patch grabs the theme config for the new user and then
    creates a ThemeChangeRequest from that config.  This request is
    then processed and applied for the new user.
    
    Secondary users will not be able to change themes at this time.
    This patch helps pave the way for that ability and provides a better
    user experience when switching users.
    
    Change-Id: I6d7e2ab312b8e3e5c099d1e9e2e62892bead10da

commit 4331132a9b7b8b1b33e1ac6c36ecf43fc096e3c8
Author: Eric Laurent <elaurent@google.com>
Date:   Wed Nov 5 12:18:05 2014 -0800

    AudioEffect JNI: use new max preprocessing constant
    
    Bug: 18226810.
    Change-Id: Ica5677da247268306b34dfce38f25394586817fd
    (cherry picked from commit b27a8a5bcc40054f6d775d070bc2de6eb996d1c2)

commit da7eba465eb6a2d80b0ccac48921af00467e7335
Author: Adam Lesinski <adamlesinski@google.com>
Date:   Fri Nov 7 11:26:14 2014 -0800

    Fix ParceledListSlice to enforce the same concrete types among its elements.
    
    Bug:17671747
    Change-Id: I896f75738e5b464ccb6c03290f139cc2fa72f966

commit 7a633bc706cc86135ccbbf3865bf243879b55ae4
Author: Jon Larimer <jlarimer@google.com>
Date:   Thu Jan 29 15:54:43 2015 -0500

    Fix build breakage in older branches by avoiding <> notation
    
    Change-Id: I5e3d523dac1f364f52f0d2cab479c1705d667e5a

commit f7d55cd95a1a3f01efa827d683e75dfa2e03f41d
Author: Leon Scroggins III <scroggo@google.com>
Date:   Tue Jan 27 11:12:02 2015 -0500

    Handle bad ninepatch data.
    
    Changes proposed by Ben Hawkes of Google Project Zero.
    
    NinePatchPeeker.cpp:
    Instead of asserting, return false for bad data.
    
    ResourceTypes.h:
    Store ninepatch values as unsigned.
    
    BUG:19151999
    Change-Id: Ibe35e7569f632c6bb8a34a7701e26bb6ed547ec2

commit 47821265a381e288f51ce80e8debeaf52c78b568
Author: Matt Garnes <matt@cyngn.com>
Date:   Thu Mar 12 16:11:14 2015 -0700

    Properly clean up when setting new InputFilter.
    
    In f1b93471565c43e57e9e199596d51f7caaec8ebd, the single InputFilter that
    is set in InputManagerService was replaced with a chain of filters that
    are all listening for InputEvents.
    
    The original field mInputFilter was replaced in this patch but not
    removed. When a new InputFilter is added, we check that this unused
    field mInputFilter != null before doing necessary teardown of the previous
    filter. Since this is always null, this causes the previous filter to
    not be disconnected when a new one is set with setInputFilter().
    
    If the user toggles "Magnification Gestures" on and off twice in Accessibility
    Settings, this will send the old and new InputFilters into a loop
    sending and receiving touch events, locking up the device completely
    until reboot.
    
    Remove all references to the unused mInputFilter field.
    
    Change-Id: I6ef67a664f1e783f3f0402b7c2a0984499a4b614

commit 3081976876a7a34d891c55abacd0eca69183928c
Author: Leon Scroggins III <scroggo@google.com>
Date:   Mon Feb 9 15:42:19 2015 -0500

    Check that bitmap's size does not exceed 32 bits. DO NOT MERGE
    
    BUG:19270126
    Change-Id: I075d1cefcd3208305a72b4fa629a262e92eb60ea

commit 2a5e9e7802d5e9241f9ef601f722c415bc4dc615
Author: Craig Mautner <cmautner@google.com>
Date:   Tue Feb 17 10:17:21 2015 -0800

    Do not make ActivityContainer available to apps. DO NOT MERGE
    
    A security leak was discovered whereby a malicious app could get the
    IActivityContainer object from one app and use it to inject events
    into another app. This fix removes the availability of the
    IActivityContainer and replaces its one use with a method for
    returning the information the IActivityContainer was used for.
    
    Fixes bug 19394591.
    
    Change-Id: Ib3cec25b25130cd8e098892c057742cfd575cfdd

commit 470e4347afcbaae888e335d33f40f02451dbff4b
Author: Mike Lockwood <lockwood@google.com>
Date:   Thu Nov 13 09:40:42 2014 -0800

    MTP: Update JNI for new packet getters
    
    Bug:18113092
    Change-Id: I137a926b3c29993124e3eaec23b1cf1b4f2b52dd

commit feb80307e9cba6c187fc82ade172277cb61f7ce3
Author: Jeff Sharkey <jsharkey@android.com>
Date:   Wed Nov 26 13:38:26 2014 -0800

    Sanitize display names, keep extensions intact.
    
    When creating or renaming files on external storage, sanitize the
    requested display names to be valid FAT filenames.  This also fixes
    a handful of directory traversal bugs.
    
    Also relax logic around generating display names to allow any
    extension which maps to the requested MIME type.  Tests to verify.
    
    Bug: 18512473, 18504132
    Change-Id: I89e632019ee145f53d9d9d2050932f8939a756af

commit 7ce33be3b02a4a11dcb1573da25c191c037b3365
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 20:17:07 2015 -0700

    Frameworks/base: Force long computation
    
    Ensure that an int-based computation is carried out as long.
    
    Change-Id: I23b10a95600674e8a5a65c0ea349afdc6aa152ae

commit 45edc234f587983df6c4ca295fdf6d9fee0a4dca
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 18:04:41 2015 -0700

    Frameworks/base: Fix a comparison
    
    Change-Id: I80d62869920e77110c95f20369ec2631c75f6ed4

commit 669fa9d413e3f8d949a3ce03995350d110f5f966
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:21:25 2015 -0700

    Frameworks/base: Fix trivial equals implementation
    
    The comparator's equal implementation doesn't satisfy the constraints
    of an equals method, namely being reflexive. Use the standard Object
    implementation instead.
    
    Bug: 19797138
    Change-Id: I74f888e99533e1945aab7ab10fe8ee3ded6388f4

commit 48a915cf2018929c0fa83aa4198939259fed7c8b
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 20:32:22 2015 -0700

    Frameworks/base: Use || instead of |
    
    Nothing wrong with | in this case, but || is canonical.
    
    Bug: 19797138
    Change-Id: I5f145736a5470f7cde06efce9a217d86eda2135f

commit 6b196aea28fb699c9c1c023e517da5bb39bcd5a0
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 13:59:50 2015 -0700

    Frameworks/base: Fix precedence bug
    
    Explicit cast has higher precedence than shift.
    
    Bug: 19797138
    Change-Id: Ifcf569bf774fbf65ee50c078f736ad167bcc6b8c

commit 057e3f41a97419c2e52eb562d27479be00e7d4ea
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:43:31 2015 -0700

    Frameworks/base: Fix format string in Camera
    
    One cannot print a boolean with %d. That will result in an exception.
    
    Bug: 19797138
    Change-Id: I86c42ea834cebebaecff8463637cc9de14d1fc88

commit 0ebbe1467678c10fd8dc5f1bf0391064c1a4cbda
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 18:55:33 2015 -0700

    Frameworks/base: Make IDENTITY_MATRIX final
    
    Bug: 19797138
    Change-Id: I127f24b7060a0c4dab401ce8e3057d362c6d6b06

commit b751b7ee8be9073f944781d8501eeb45c9efcd77
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:49:15 2015 -0700

    Frameworks/base: Fix format string in Geofence
    
    %p is not a valid conversion in format strings. It is also superfluous,
    as it is already known that location is null.
    
    Bug: 19797138
    Change-Id: I5784e28b05b4ca9aac57e0fc9da4a7f01d9b3247

commit 9b2edccdc49c827bc6a255bb4f7c4d3cd62aed3a
Author: Jason Sams <jsams@google.com>
Date:   Tue Mar 17 16:36:55 2015 -0700

    Avoid duplicate surface creation.
    
    Change-Id: I43104c8b48dd26681735940e6b2e1ba902af2020

commit 6c45856da8c159e1a23441db00e591ba63bf9d4c
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 16:08:43 2015 -0700

    Frameworks/base: Fix visibility flag in Editor
    
    Fix double check.
    
    Bug: 19797138
    Change-Id: I95e694f384f1f25d6cf3b6a1669052940385e41d

commit 69ead566e923f0a58e260c162c434f0ded58566d
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 19:10:14 2015 -0700

    Frameworks/base: Remove duplicate check in Mesh
    
    Bug: 19797138
    Change-Id: I0b11c4ff63a8031d5e58a06ac13f91ae0bbac5dc

commit 94f691dbe1a3b4e97bfe2d6357e01392b85cd185
Author: Andreas Gampe <agampe@google.com>
Date:   Tue Mar 17 21:07:21 2015 -0700

    Frameworks/base: Fix potential NPE in InputMethod
    
    Don't read the size of an unchecked list.
    
    Bug: 19797138
    Change-Id: I9d8c087aff7bc9cc1e8aae9a0b489e23b5442765

commit 0ce2eaad138a51b1e0d497e724f23f68cc45c8da
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 18 10:48:02 2015 -0700

    Themes: Always clone the new theme if non-null
    
    The new theme was only being cloned when shouldUpdateStatusbar()
    returned true.  This causes the navigation bar to not be themed
    when no components changed that required the status bar to be
    recreated.  This patch always clones the new theme so that the
    proper navigation bar resources can be loaded.
    
    Change-Id: I8d70c54d3bfcd91141ce40f513744e260fe87639
    REF: THEMES-573

commit 4dddb8d5bab453538f41dd82fdd01acfcf1f5279
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 17 13:22:32 2015 -0700

    improve lock screen wallpaper behavior
    
     - Fix lockscreen wallpaper not being reloaded on user switch.
       There was an issue where the wrong user id was being queried for the
       keyguard wallpaper. Always use the current user id.
    
     - Also clean up a left-over call for some regular wallpaper
       migration logic that the lock screen wallpaper
    
     - Add method for removing references to the current lock screen
       wallpaper, which we call from systemui when switching users.
    
     - Only apply the lock screen wallpaper if there is no media metadata
       to show. There were some cases when it would still appear even when
       music was playing.
    
    Change-Id: I610a38ac11a19638298ca9490b3c87b7ab6106f2
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit fde34f5b688238c19612ee91e53b8b8012dae5b2
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 19 20:39:23 2015 +0100

    systemui: don't start-stop visualizer directly after a power save event
    
    Change-Id: Ie8643aa84d20a8a8a94c5be13332ac09ce8611d6
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 4df7300840c5e5f32ffb18626de1105509c764bc
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 13 15:30:19 2015 -0700

    SystemUI: load current user's qs tiles
    
    Change-Id: I29cd37d0daba3f25e8b7d07eb62df0ad344c9a80
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 6a21479c0d92b530efb25110e3b9d544d944c075
Author: Andy Mast <andy@cyngn.com>
Date:   Thu Mar 19 17:48:11 2015 -0700

    Avoid boot looping when theme provider is unavailable
    
    Was reported to happen when the device is encrypted.
    
    Change-Id: I0e8da0270180038211bc469792bd5089aff49e96
    (cherry picked from commit 98df5ddef08d7f1308c81a071118bbef432fe5ad)

commit d7947f147e69a5dd82b662f0c963e1263330cfc1
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
    (cherry picked from commit c67bc8b6390e972294d136bb1e921db6b6c2d251)

commit e77e3069e74edc7464f9d8b0940ec58a814b70be
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 20 15:25:23 2015 -0700

    Themes: Perform mapping when not from overlay
    
    This will resolve an issue where an unthemed style references
    itself as the parent i.e. Real Racing 3.
    
    Change-Id: I1aaf5567a44ee0e5ddfad1e8c0e5ab7bc8c1e5bf
    REF: TOMATL-382

commit 44f71d1d46d91d42ed627e6da059d5fdc4e24696
Author: Andy Mast <andy@cyngn.com>
Date:   Fri Mar 20 20:47:55 2015 -0700

    Clear Theme in System UI
    
    When SystemUI first starts an android theme object is created
    which contains references to the currently applied CM theme.
    
    When the theme is changed to system, the theme remains in memory
    with old references to the prior applied theme. (See mPackages in ResTable::Theme)
    
    This patch introduces a recreate theme method into Context so that
    SystemUI can recreate its own theme object.
    
    Change-Id: I086a76afa6f456a69c0390573bc8af2eafa4fb4e
    (cherry picked from commit b85fb98038325ee7e6e48a7ca962bcdcb3e176e0)
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 0ea055bf89570933d2b46eacc016c68631fb372e
Author: Scott Mertz <scott@cyngn.com>
Date:   Fri Mar 20 18:52:15 2015 -0700

    Don't start theme service on core only boot
    
    Change-Id: I8a8a142d2dab8d913951848989b5e3e5ec683f65
    (cherry picked from commit b92c2ccfb44d2d1a1a6fd48da108736db3fbaaa2)

commit 43a8a49915783e52698b4f46ebb3ed3b19198a30
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 20 20:50:36 2015 -0700

    SystemUI: survive notification update spam
    
    When handling a very high number of incoming notification updates, SystemUI can
    choke up at updateNotifications() in PhoneStatusBar. Funnel
    updateNotification() calls through the StatusBar's handler and don't
    stack them up.
    
    Change-Id: I806d1fd8eac73c4af0820319d127423ae6467f60
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 18fcd5b5d101840e5e5347edc1ff83b7a2da911f
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 19:22:13 2015 -0700

    Revert "GlobalActions: Use circular user avatars"

commit fedce597fff326710d621d6f59d0c6390bc9952a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Mar 21 19:24:34 2015 -0700

    GlobalActions: Use circular user avatars
    
    * Use circular & smaller avatars, logic copied from SystemUI
    * Improve current user indication (thanks to maxwen)
    
    Change-Id: Id0ab6271a5249d873c836f75f62862d0a3633c75
    
    Conflicts:
    	core/res/res/values/dimens.xml
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/GlobalActions.java

commit 6a24259463997013f62571e5b4e4dfee1e2cbeac
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 20 22:22:22 2015 -0700

    Themes: Don't break API in MockContext
    
    recreateTheme() needs to have @hide otherwise checkapi fails.
    
    Change-Id: I90a8620724a5ca8a52bce4bd91bd5534812479b1

commit 57f209c0f903a099ef04d9acddec592f508f4d09
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 20 22:32:46 2015 -0700

    Revert "Themes: Don't break API in MockContext"
    
    This reverts commit 1b564750a2adced74bec150b770d546c5f2dc51f.
    
    Change-Id: I2b22ad846402237338cb9f5791553ce6219ff722

commit fe77638e3390664966643a91c5fba0c76038febb
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 20 22:33:23 2015 -0700

    Themes: Properly hide recreateTheme
    
    Change-Id: Ifa23515cfbf8eaf16d2bbe26374cbdcf65929dff

commit ad11104687a465455b794aa3096b30b8787b6012
Author: Scott Mertz <scott@cyngn.com>
Date:   Sat Mar 21 12:16:25 2015 -0700

    PackageManager: don't attempt to get theme on core boot
    
    Change-Id: Id4b12279a52e53c236c61074c5d92bcb44f59a64

project frameworks/native/
commit f58a148de7ca986efb73e3e3b2a5350d699c7f0a
Author: Michael Lentine <mlentine@google.com>
Date:   Wed Feb 18 10:14:18 2015 -0800

    Update maxNumber to be smaller.
    
    There shouldn't be more than 4096 fds (probably signficantly smaller) and
    there shouldn't be more than 4096 ints.
    
    Bug: 18076253
    
    Change-Id: I3a3e50ee3078a4710e9737114e65afc923ed0573

commit deb38f7ef066c026809e80affe301d6cdaa77959
Merge: 88a5ca9 f58a148
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 09:00:39 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project frameworks/opt/net/wifi/
commit 6655e0006ba965530225c72cb8da0acea60e70b0
Author: Nalla Kartheek <karthe@codeaurora.org>
Date:   Thu Feb 5 13:52:47 2015 +0530

    WiFi: Correct CMD_PNO_PERIODIC_SCAN command value
    
    In WifiStateMachine CMD_PNO_PERIODIC_SCAN and CMD_ROAM_WATCHDOG_TIMER
    constants are assigned same value, due to which one of the operation fails.
    Assign correct command value to CMD_PNO_PERIODIC_SCAN.
    
    Change-Id: I478948d1a2c0308df4de9f0e15d0dd32a16e4a40
    CRs-Fixed: 791409

commit 66462008b4c00afb0b908d23246801e15abdacd8
Author: Sravanthi Palakonda <srapal@codeaurora.org>
Date:   Thu Dec 4 19:16:52 2014 +0530

    wifi:Provide UI with SIM info for EAP-SIM authentication
    
    User Interface requires the SIM information (viz. number / type
    of SIM's supported on the device), using which the respective
    authentication option is provisioned to the user. This commit
    queries the same by invoking a command exposed by the
    wpa_supplicant. It is the wpa_supplicant that gets this
    information.
    
    CRs-Fixed: 775942
    Change-Id: I93c6a5450c806d8fade0103ef96eca986c925eba

commit 5a16c4cee79f3f28e9387b668290068ecffaba27
Author: Sravanthi Palakonda <srapal@codeaurora.org>
Date:   Mon Feb 23 13:36:15 2015 +0530

    wifi: Handle error cases when EAP-SIM info is NULL/Unsupported
    
    To get the SIM information,UI queries framework through the
    API exposed by the Wi-Fi framework which further interacts with
    the supplicant.If the supplicant times out or does not support
    the EAP-SIM functionality ,it either returns null or the string
    "unsupported".This throws an error while parsing at WifiEapSimInfo.
    This commit handles the error cases by catching the exception.
    
    Change-Id: Ie7b20dc32016d0396e68971415a835c40cf37989
    CRs-Fixed: 796265

project frameworks/opt/telephony/
commit 5f8247ab7d9627afb7e57e1d012882e6974bf56c
Author: Dave Kessler <activethrasher00@gmail.com>
Date:   Fri Mar 20 16:26:28 2015 -0400

    IccSmsInterfaceManager: Disable debug logging
    
    Change-Id: I0ddfb6afc280b0739db17f6ffb80ca6976fae66b

commit 7063661c0a3cf8eaa5e788af313259b2af3fd023
Merge: a46b529 5f8247a
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 20 21:01:24 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project hardware/qcom/display-caf/msm8916/
commit b01ae24693ba7076410ecb8cfb93f3908f84fe7c
Author: Baldev Sahu <bsahu@codeaurora.org>
Date:   Thu Nov 13 17:58:18 2014 +0530

    hwc: Add secure display attribute
    
    - External displays can be secure or non-secure based on HDCP
    - Propogate this to the SF with the getDisplayConfig
    - Non-virtual displays(pri and hdmi) are considered to be secure
    - For WFD using V4L2 archiecture, read the HDCP status from the
      sysfs and update accordingly
    
    Change-Id: I7ac273aeb845c4762dc0690c7b88841c911c044b

project hardware/samsung/
commit 29472681221cd610b2e04d32498201dda41c1bd3
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Thu Jan 1 19:00:04 2015 +0100

    libril: Add support for xmm7260 modem.
    
    Change-Id: Ia3749bd4c43a2e233e722462dd6423fe8c692177
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

commit 6b9cd5f8b49db8d5dab0e7042a1bc7ab333bbe4b
Author: Andreas Schneider <asn@cryptomilk.org>
Date:   Fri Jan 23 22:41:22 2015 +0100

    librilsec-client: Add support for xmm7260 modem
    
    Change-Id: If287527a26a1f5c79ec493ad2cd1cd7152ba27db
    Signed-off-by: Andreas Schneider <asn@cryptomilk.org>

project kernel/samsung/trlte/
commit c8d5efd511351770a048aa9a5a9f021524920141
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 00:39:00 2015 -0700

    intelli-thermal v2: initial adaptation (faux123)
    
    Intellithermal 2.0 is based on the latest Qualcomm thermal driver
    adapted for
    in-kernel use and control.  Newer MSM8974+ chipsets should use this
    driver
    going forward

commit 1d66d65cf12ba0849221e1cfeb86e62a862389ba
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 11:36:09 2015 -0700

    Revert: Lower GPU voltage constraint
    
    Signed-off-by: flar2 <asegaert@gmail.com> (reverted from commit 564caaaa8c213fc6fdf49483dd5c115db93b733c)

commit 2a6d6900e306bff7539287261681d12960b96518
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Tue Nov 4 13:17:14 2014 -0500

    cpufreq: Initial setup for new gov [Umbrella Core] (TwistedUmbella)

commit 39dcc80d4e1fd2173fe1d1dcf29c0f7055387ec7
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 20:19:00 2015 -0700

    ElementalX governor (flar2)
    
    elementalx governor: disable cpuboost

commit ebb561a0ace9a68f7679ce89f99cb499b77b8ad1
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Tue Dec 30 20:41:58 2014 +0100

    include: linux: add Sysfs_helpers: Allow negative values

commit 0e7cfd9972bfa861f615b1efaaf14aa2b11e0ae1
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 19:32:35 2015 -0700

    update shamu interactive governor

commit 200f532857eca5d3923d4d5b7e4f5188d37b4a4e
Author: franciscofranco <franciscofranco.1990@gmail.com>
Date:   Mon Dec 29 01:57:37 2014 +0000

    msm: thermal: add a module param to change the thermal throttle temperature point to userspace
    
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 18ea5321e43032832508c50617051997a0cd840d
Author: myfluxi <linflux@arcor.de>
Date:   Wed Jan 1 11:31:16 2014 +0100

    msm: kgsl: Report correct GPU frequency in sysfs
    
    Change-Id: I1aac90d0554b9de0511ffb78042177a5a23855ce
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit e9e86d14cc887ec3f3b993f699b90642788a5dff
Author: myfluxi <linflux@arcor.de>
Date:   Wed Jan 8 01:25:14 2014 +0100

    PM: devfreq: Use high priority workqueue
    
    It does not make sense to run kgsl on high and devfreq on regular
    priority.
    
    Change-Id: Ie5e6c9353a4e1324a6a49278e5ad3638462f551c
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 862bec2c60b0466cff83213d2e68e8e0ca252e09
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 11:48:48 2015 -0700

    block: cgroups, kconfig, build bits for BFQ-v7r6-3.10.8+
    
    Update Kconfig.iosched and do the related Makefile changes to include
    kernel configuration options for BFQ. Also add the bfqio controller
    to the cgroups subsystem.
    
    Signed-off-by: Paolo Valente <paolo.valente@unimore.it>
    Signed-off-by: Arianna Avanzini <avanzini.arianna@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 113d1bb6a8e2cd40cbfc97469d66b0dda1bf8f52
Author: Paolo Valente <paolo.valente@unimore.it>
Date:   Thu May 9 19:10:02 2013 +0200

    block: introduce the BFQ-v7r6 I/O sched for 3.10.8+
    
    Add the BFQ-v7r6 I/O scheduler to 3.10.8+.
    The general structure is borrowed from CFQ, as much of the code for
    handling I/O contexts Over time, several useful features have been
    ported from CFQ as well (details in the changelog in README.BFQ). A
    (bfq_)queue is associated to each task doing I/O on a device, and each
    time a scheduling decision has to be made a queue is selected and served
    until it expires.
    
        - Slices are given in the service domain: tasks are assigned
          budgets, measured in number of sectors. Once got the disk, a task
          must however consume its assigned budget within a configurable
          maximum time (by default, the maximum possible value of the
          budgets is automatically computed to comply with this timeout).
          This allows the desired latency vs "throughput boosting" tradeoff
          to be set.
    
        - Budgets are scheduled according to a variant of WF2Q+, implemented
          using an augmented rb-tree to take eligibility into account while
          preserving an O(log N) overall complexity.
    
        - A low-latency tunable is provided; if enabled, both interactive
          and soft real-time applications are guaranteed a very low latency.
    
        - Latency guarantees are preserved also in the presence of NCQ.
    
        - Also with flash-based devices, a high throughput is achieved
          while still preserving latency guarantees.
    
        - BFQ features Early Queue Merge (EQM), a sort of fusion of the
          cooperating-queue-merging and the preemption mechanisms present
          in CFQ. EQM is in fact a unified mechanism that tries to get a
          sequential read pattern, and hence a high throughput, with any
          set of processes performing interleaved I/O over a contiguous
          sequence of sectors.
    
        - BFQ supports full hierarchical scheduling, exporting a cgroups
          interface.  Since each node has a full scheduler, each group can
          be assigned its own weight.
    
        - If the cgroups interface is not used, only I/O priorities can be
          assigned to processes, with ioprio values mapped to weights
          with the relation weight = IOPRIO_BE_NR - ioprio.
    
        - ioprio classes are served in strict priority order, i.e., lower
          priority queues are not served as long as there are higher
          priority queues.  Among queues in the same class the bandwidth is
          distributed in proportion to the weight of each queue. A very
          thin extra bandwidth is however guaranteed to the Idle class, to
          prevent it from starving.
    
    Signed-off-by: Paolo Valente <paolo.valente@unimore.it>
    Signed-off-by: Arianna Avanzini <avanzini.arianna@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 07deb51e523d1fcd3bb8ac6d4d924b4fef763cba
Author: Mauro Andreolini <mauro.andreolini@unimore.it>
Date:   Sun Oct 19 03:10:48 2014 +0200

    block, bfq: add Early Queue Merge (EQM) to BFQ-v7r6 for 3.10.8+
    
    A set of processes may happen  to  perform interleaved reads, i.e.,requests
    whose union would give rise to a  sequential read  pattern.  There are two
    typical  cases: in the first  case,   processes  read  fixed-size chunks of
    data at a fixed distance from each other, while in the second case processes
    may read variable-size chunks at  variable distances. The latter case occurs
    for  example with  QEMU, which splits the  I/O generated  by the  guest into
    multiple chunks,  and lets these chunks  be served by a  pool of cooperating
    processes,  iteratively  assigning  the  next  chunk of  I/O  to  the first
    available  process. CFQ  uses actual  queue merging  for the  first type of
    rocesses, whereas it  uses preemption to get a sequential  read pattern out
    of the read requests  performed by the second type of  processes. In the end
    it uses  two different  mechanisms to  achieve the  same goal: boosting the
    throughput with interleaved I/O.
    
    This patch introduces  Early Queue Merge (EQM), a unified mechanism to get a
    sequential  read pattern  with both  types of  processes. The  main idea is
    checking newly arrived requests against the next request of the active queue
    both in case of actual request insert and in case of request merge. By doing
    so, both the types of processes can be handled by just merging their queues.
    EQM is  then simpler and  more compact than the  pair of mechanisms used in
    CFQ.
    
    Finally, EQM  also preserves the  typical low-latency properties of BFQ, by
    properly restoring the weight-raising state of  a queue when it gets back to
    a non-merged state.
    
    Signed-off-by: Mauro Andreolini <mauro.andreolini@unimore.it>
    Signed-off-by: Arianna Avanzini <avanzini.arianna@gmail.com>
    Signed-off-by: Paolo Valente <paolo.valente@unimore.it>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 6e1387209167fa87d8e2b86927bfb99325e303cf
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 20:56:07 2015 -0700

    Added sio, fifo, vr and zen I/O schedulers

commit a0c3170614a0265a41d08cb8497b7634d181f1fc
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 18:27:12 2015 -0700

    base CMRemix v1.2

commit f8ef7d230d80b7b51fb49a5dec1f46a87d29b3c8
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 00:41:49 2015 -0700

    add MDNIE Lite Control
    
    Credits to Yank555.lu and StarKissed

commit 0650ba495a76555adfd8a9c2a5076121be8c166b
Author: Junxiao Bi <junxiao.bi@oracle.com>
Date:   Wed Sep 11 14:23:04 2013 -0700

    writeback: fix race that cause writeback hung
    
    There is a race between mark inode dirty and writeback thread, see the
    following scenario.  In this case, writeback thread will not run though
    there is dirty_io.
    
    __mark_inode_dirty()                                          bdi_writeback_workfn()
    	...                                                       	...
    	spin_lock(&inode->i_lock);
    	...
    	if (bdi_cap_writeback_dirty(bdi)) {
    	    <<< assume wb has dirty_io, so wakeup_bdi is false.
    	    <<< the following inode_dirty also have wakeup_bdi false.
    	    if (!wb_has_dirty_io(&bdi->wb))
    		    wakeup_bdi = true;
    	}
    	spin_unlock(&inode->i_lock);
    	                                                            <<< assume last dirty_io is removed here.
    	                                                            pages_written = wb_do_writeback(wb);
    	                                                            ...
    	                                                            <<< work_list empty and wb has no dirty_io,
    	                                                            <<< delayed_work will not be queued.
    	                                                            if (!list_empty(&bdi->work_list) ||
    	                                                                (wb_has_dirty_io(wb) && dirty_writeback_interval))
    	                                                                queue_delayed_work(bdi_wq, &wb->dwork,
    	                                                                    msecs_to_jiffies(dirty_writeback_interval * 10));
    	spin_lock(&bdi->wb.list_lock);
    	inode->dirtied_when = jiffies;
    	<<< new dirty_io is added.
    	list_move(&inode->i_wb_list, &bdi->wb.b_dirty);
    	spin_unlock(&bdi->wb.list_lock);
    
    	<<< though there is dirty_io, but wakeup_bdi is false,
    	<<< so writeback thread will not be waked up and
    	<<< the new dirty_io will not be flushed.
    	if (wakeup_bdi)
    	    bdi_wakeup_thread_delayed(bdi);
    
    Writeback will run until there is a new flush work queued.  This may cause
    a lot of dirty pages stay in memory for a long time.
    
    Signed-off-by: Junxiao Bi <junxiao.bi@oracle.com>
    Reviewed-by: Jan Kara <jack@suse.cz>
    Cc: Fengguang Wu <fengguang.wu@intel.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit a89fbd44b2ab560f838629fdc4b0fc172aa7c19d
Author: Namjae Jeon <namjae.jeon@samsung.com>
Date:   Wed Jan 2 20:00:40 2013 -0600

    writeback: fix writeback cache thrashing
    
    Consider Process A: huge I/O on sda
            doing heavy write operation - dirty memory becomes more
            than dirty_background_ratio
            on HDD - flusher thread flush-8:0
    
    Consider Process B: small I/O on sdb
            doing while [1]; read 1024K + rewrite 1024K + sleep 2sec
            on Flash device - flusher thread flush-8:16
    
    As Process A is a heavy dirtier, dirty memory becomes more
    than dirty_background_thresh. Due to this, below check becomes
    true(checking global_page_state in over_bground_thresh)
    for all bdi devices(even for very small dirtied bdi - sdb):
    
    In this case, even small cached data on 'sdb' is forced to flush
    and writeback cache thrashing happens.
    
    When we added debug prints inside above 'if' condition and ran
    above Process A(heavy dirtier on bdi with flush-8:0) and
    Process B(1024K frequent read/rewrite on bdi with flush-8:16)
    we got below prints:
    
    [Test setup: ARM dual core CPU, 512 MB RAM]
    
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  56064 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  56704 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 84720 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 94720 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   384 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   960 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =    64 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 92160 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   256 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   768 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =    64 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   256 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   320 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =     0 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 92032 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 91968 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   192 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =  1024 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =    64 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   192 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   576 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =     0 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 84352 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   192 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =   512 KB
    [over_bground_thresh]: wakeup flush-8:16 : BDI_RECLAIMABLE =     0 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 92608 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE = 92544 KB
    
    As mentioned in above log, when global dirty memory > global background_thresh
    small cached data is also forced to flush by flush-8:16.
    If removing global background_thresh checking code, we can reduce cache
    thrashing of frequently used small data.
    And It will be great if we can reserve a portion of writeback cache using
    min_ratio.
    
    After applying patch:
    $ echo 5 > /sys/block/sdb/bdi/min_ratio
    $ cat /sys/block/sdb/bdi/min_ratio
    5
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  56064 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  56704 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  84160 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  96960 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  94080 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  93120 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  93120 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  91520 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  89600 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  93696 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  93696 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  72960 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  90624 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  90624 KB
    [over_bground_thresh]: wakeup flush-8:0 : BDI_RECLAIMABLE =  90688 KB
    
    As mentioned in the above logs, once cache is reserved for Process B,
    and patch is applied there is less writeback cache thrashing on sdb
    by frequent forced writeback by flush-8:16 in over_bground_thresh.
    
    After all, small cached data will be flushed by periodic writeback
    once every dirty_writeback_interval.
    
    Suggested-by: Wanpeng Li <liwanp@linux.vnet.ibm.com>
    Signed-off-by: Namjae Jeon <namjae.jeon@samsung.com>
    Signed-off-by: Vivek Trivedi <t.vivek@samsung.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 1873dc48a40d04bc1c49b6f2718cd0fb34c57bd3
Author: Fengguang Wu <fengguang.wu@intel.com>
Date:   Wed Sep 11 14:21:47 2013 -0700

    readahead: make context readahead more conservative
    
    This helps performance on moderately dense random reads on SSD.
    
    Transaction-Per-Second numbers provided by Taobao:
    
    		QPS	case
    		-------------------------------------------------------
    		7536	disable context readahead totally
    w/ patch:	7129	slower size rampup and start RA on the 3rd read
    		6717	slower size rampup
    w/o patch:	5581	unmodified context readahead
    
    Before, readahead will be started whenever reading page N+1 when it happen
    to read N recently.  After patch, we'll only start readahead when *three*
    random reads happen to access pages N, N+1, N+2.  The probability of this
    happening is extremely low for pure random reads, unless they are very
    dense, which actually deserves some readahead.
    
    Also start with a smaller readahead window.  The impact to interleaved
    sequential reads should be small, because for a long run stream, the the
    small readahead window rampup phase is negletable.
    
    The context readahead actually benefits clustered random reads on HDD
    whose seek cost is pretty high.  However as SSD is increasingly used for
    random read workloads it's better for the context readahead to concentrate
    on interleaved sequential reads.
    
    Another SSD rand read test from Miao
    
            # file size:        2GB
            # read IO amount: 625MB
            sysbench --test=fileio          \
                    --max-requests=10000    \
                    --num-threads=1         \
                    --file-num=1            \
                    --file-block-size=64K   \
                    --file-test-mode=rndrd  \
                    --file-fsync-freq=0     \
                    --file-fsync-end=off    run
    
    shows the performance of btrfs grows up from 69MB/s to 121MB/s, ext4 from
    104MB/s to 121MB/s.
    
    Signed-off-by: Wu Fengguang <fengguang.wu@intel.com>
    Tested-by: Tao Ma <tm@tao.ma>
    Tested-by: Miao Xie <miaox@cn.fujitsu.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 9bf1d3934fa5e2d56933c6f06402c94d81cfb9b1
Author: Jan Kara <jack@suse.cz>
Date:   Fri Jun 28 21:32:27 2013 +0200

    block: Reserve only one queue tag for sync IO if only 3 tags are available
    
    In case a device has three tags available we still reserve two of them
    for sync IO. That leaves only a single tag for async IO such as
    writeback from flusher thread which results in poor performance.
    
    Allow async IO to consume two tags in case queue has three tag availabe
    to get a decent async write performance.
    
    This patch improves streaming write performance on a machine with such disk
    from ~21 MB/s to ~52 MB/s. Also postmark throughput in presence of
    streaming writer improves from 8 to 12 transactions per second so sync
    IO doesn't seem to be harmed in presence of heavy async writer.
    
    Signed-off-by: Jan Kara <jack@suse.cz>
    Signed-off-by: Jens Axboe <axboe@kernel.dk>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 3bfa101af8905a934c5a39caa6ba45b8e1cb9487
Author: flar2 <asegaert@gmail.com>
Date:   Thu Mar 12 22:44:16 2015 -0400

    fix compilation warnings

commit 965005fde72d694a29ce9a15e8c821da09eab64b
Author: Mel Gorman <mgorman@suse.de>
Date:   Wed May 11 16:29:33 2011 +0100

    mm: slub: Default slub_max_order to 0
    
    To avoid locking and per-cpu overhead, SLUB optimisically uses
    high-order allocations up to order-3 by default and falls back to
    lower allocations if they fail. While care is taken that the caller
    and kswapd take no unusual steps in response to this, there are
    further consequences like shrinkers who have to free more objects to
    release any memory. There is anecdotal evidence that significant time
    is being spent looping in shrinkers with insufficient progress being
    made (https://lkml.org/lkml/2011/4/28/361) and keeping kswapd awake.
    
    SLUB is now the default allocator and some bug reports have been
    pinned down to SLUB using high orders during operations like
    copying large amounts of data. SLUBs use of high-orders benefits
    applications that are sized to memory appropriately but this does not
    necessarily apply to large file servers or desktops.  This patch
    causes SLUB to use order-0 pages like SLAB does by default.
    There is further evidence that this keeps kswapd's usage lower
    (https://lkml.org/lkml/2011/5/10/383).
    
    Signed-off-by: Mel Gorman <mgorman@suse.de>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 3edcff647cd905e29fc0019c3406547071c468b8
Author: Xiaocheng Li <lix@codeaurora.org>
Date:   Mon Oct 13 09:55:27 2014 +0530

    msm: thermal: Keep core_control_mask coincident with boot_cpu_mask
    
    Update core_control_mask according to boot_cpu_mask to make sure
    the hotplug activities in thermal driver can only happen among the
    CPUs under boot_cpu_mask.
    
    Change-Id: Ic8bd319b94b234e913d89b65736ff287706db7c1
    Signed-off-by: Xiaocheng Li <lix@codeaurora.org>

commit 09cb076bc7a18b80903dba94cd1339d76a03b701
Author: Shiju Mathew <shijum@codeaurora.org>
Date:   Tue Nov 11 18:47:02 2014 -0500

    msm: thermal: Proceed thermal late init only if probe is successful
    
    Skip thermal late init if thermal probe has not
    completed since all the tasks in late init depend
    on successful completion of thermal probe.
    
    Change-Id: Iab763b80d2c878dd57a2401c92799c2534b349d2
    Signed-off-by: Shiju Mathew <shijum@codeaurora.org>

commit 86d9410a66fe371316e20ff620ca603d082793ed
Author: Shiju Mathew <shijum@codeaurora.org>
Date:   Tue Nov 18 20:14:42 2014 -0500

    msm: thermal: Add RT priority to kernel thermal threads
    
    Add RT priority to KTM frequency mitigation thread. This
    is required since we have seen cases where this thread
    is not scheduled fast enough during high temperature rampup
    that lead to thermal runaway. So this change would make sure
    the thermal frequency mitigation thread gets high priority
    and mitigate core as soon as a temperature threshold is triggered.
    
    Change-Id: Ie8a6fd80fb8e9bdb894a26a8bf7abd159a3f3bce
    Signed-off-by: Shiju Mathew <shijum@codeaurora.org>
    
    Conflicts:
    	drivers/thermal/msm_thermal.c

commit c68eea7477baf3ca2dbfe8853ec7b82fc165cb45
Author: Shiju Mathew <shijum@codeaurora.org>
Date:   Tue Dec 16 20:29:49 2014 -0500

    msm: thermal: Add RT priority to kernel hotplug thread
    
    Add RT priority to KTM hotplug mitigation thread. This
    is required since we have seen cases where the thread
    is not scheduled fast enough during high temperature rampup
    that lead to thermal runaway. So this change would make sure
    the thermal hotplug mitigation thread gets high priority
    and mitigate core as soon as a temperature threshold is triggered.
    
    Change-Id: I72ecf69ede0444fe74fd9c4eaf40a12e8734326c
    Signed-off-by: Shiju Mathew <shijum@codeaurora.org>

commit e7b1ac02008858453c9db1d4fd4e3f1fcbbac6a7
Author: Dipen Parmar <dipenp@codeaurora.org>
Date:   Tue Mar 18 21:28:05 2014 +0530

    thermal: tsens: Add NULL pointer check for id
    
    Add NULL pointer check for id value to avoid the
    NULL pointer dereference when of_match_node function
    can return NULL for non-matching node.
    
    Change-Id: If01290f11c44631249b0740271b2d51a3654b54a
    Signed-off-by: Dipen Parmar <dipenp@codeaurora.org>
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>

commit 1daf9158736a026872d1a12504c627f288765580
Author: Siddartha Mohanadoss <smohanad@codeaurora.org>
Date:   Mon Dec 8 16:40:09 2014 -0800

    thermal: tsens: Fix TSENS Upper/Lower IRQ type
    
    Update TSENS IRQ to level trigger instead of using
    edge trigger interrupt.
    
    When a sensors temperature threshold is crossed the
    controller asserts a level trigger. This level goes
    low when the Upper/Lower status threshold is masked.
    However, if another sensor threshold is crossed while we
    are in the middle of servicing the previous sensors
    threshold crossing in the workqueue the new sensors
    threshold crossing will be missed as the interrupt level
    remains high. Fix it by registering the interrupt as a
    level interrupt, disable the interrupt in the
    handler and enable it while we exit from the workqueue.
    
    CRs-Fixed: 768227
    Change-Id: I7b3f38afd8acb2903f85dcc23e1bfe70d7d9059a
    Signed-off-by: Siddartha Mohanadoss <smohanad@codeaurora.org>
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>

commit 3ade4075007c03663927e2ef0d6110f0217d930d
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 00:45:24 2015 -0700

    cmremix v1.3

commit 330e005cbcc4484e76d09c5634c00e0445a764c1
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 00:53:53 2015 -0700

    msm cpu frequency limit (faux123)

commit 7d03b9ff3329ca9f0b66747d8a66913be0f9c008
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 01:34:07 2015 -0700

    revert: msm cpu frequency limit (faux123) (reverted from commit 330e005cbcc4484e76d09c5634c00e0445a764c1)

project libcore/
commit fe42e966789ef23b7ab7fe111c943c44285db0db
Author: Alex Klyubin <klyubin@google.com>
Date:   Tue Nov 18 17:37:20 2014 -0800

    Fix a bug in DefaultHostnameVerifier wildcard handling.
    
    Wildcard domain name patterns of the form *.remainder are supposed to
    match domain names that exactly match the remainder. Due to a bug,
    the match was not exact but rather a prefix match: domain names
    starting with the remainder would match too.
    
    This CL fixes the issue.
    
    Bug: 18432707
    Change-Id: Ic2fccbfeac4f5d6e71b49ecbd36c248214baebad

project packages/apps/Bluetooth/
commit 57262f776b6b7bf3453d96c4b7b555bfc3fb45a0
Author: Matthew Xie <mattx@google.com>
Date:   Thu Oct 23 12:53:40 2014 -0700

    updateshare confirm logic missed cases like CONFIRMATION_DENIED, TIMEOUT. fix it
    
    bug 17770561
    Change-Id: I34fb018d9787b4deef8592c71f5539778e76e325
    (cherry picked from commit 70743aa46fa95bd252acea614bfde8cc65e03890)

commit 0cb71bf79ed4b70bc6b254950a1683d72b7e1ed5
Author: Matthew Xie <mattx@google.com>
Date:   Mon Nov 17 09:50:54 2014 -0800

    Check previous user confirmation before auto-confirm put request
    
    Also correct a confirm status change check in updateShare.
    Bug: 17770561, 18343032
    
    Change-Id: I8e7d10e73604c0bf1c88801a1caef7d579fbd1eb

commit c905e5a564a1f055f655724e2efb2765c2c098e3
Author: Andre Eisenbach <eisenbach@google.com>
Date:   Sun Dec 14 12:22:31 2014 -0800

    Prevent duplicate OPP permission request dialogs
    
    When multiple files are sent in a single OPP session, the user should be
    prompted to accept/reject only once.
    
    Bug: 17770561
    Change-Id: I438116915883c5fdc2d743f13456006f66511c0f

project packages/apps/CMFileManager/
commit 05ddc9cd818b41b8673b848b2a48982f48738277
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 13 09:25:48 2015 -0700

    CMFileManager: protect code path for access mSdBookmarks
    
    FATAL EXCEPTION: main
    
    AndroidRuntime: Process: com.cyanogenmod.filemanager, PID: 2587
    
    AndroidRuntime: java.lang.NullPointerException: Attempt to invoke interface method 'java.util.Iterator java.util.List.iterator()' on a null object reference
    
    AndroidRuntime: 	at com.cyanogenmod.filemanager.activities.NavigationActivity.applyInitialDir(NavigationActivity.java:1626)
    
    AndroidRuntime: 	at com.cyanogenmod.filemanager.activities.NavigationActivity$15.run(NavigationActivity.java:1521)
    
    AndroidRuntime: 	at android.os.Handler.handleCallback(Handler.java:739)
    
    Change-Id: I2aec4fd6a5b8fcd31cd128f8f46cc9f88bca191e

commit 336c3849084b0a3f35500215d9ad4d94fcb63d89
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Tue Mar 17 06:12:46 2015 -0700

    CMFileManager: Fix back press events of SearchActivity
    
    epro:
    - SearchActivity to audio file
    - Open audio file with small player (e.g. Play Music)
    - Press back
    - Observe: audio player closes and CMFM SearchActivity up one directory(NavigationActivity)
    
    Change-Id: I4ab1faa1d061eea97050b89e96c1bdf1df66db3f

commit 03e534f48063b633af1e96201a8223285da8a877
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 19 11:45:53 2015 +0100

    cmfm: fix edit home bookmark icon
    
    Change-Id: I0da0a0b01f49d24edab30a72decd240996b5ccfe
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit b62df7af6326e628c0a57948a324aad97fb8fe28
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 19 12:15:56 2015 +0100

    cmfm: force colorControlNormal to white
    
    This fixed the color of actionbar controls (like search widget)
    
    Change-Id: I7a78cc7cd6bee262224b1d881b645aaef504be29
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 2185846e4a2927563263c15a7a09061d0f7624a7
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 19 12:45:54 2015 +0100

    cmfm: delete obsolete themes resources
    
    Change-Id: I3fc24f739b16ab6104a4349f0c8efe0eff790fbd
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit df97de0cff704f0bfbd70fffe0f3cee346dbfa15
Author: Rohit Yengisetty <rohit@cyngn.com>
Date:   Thu Mar 5 16:35:21 2015 -0800

    CM File Manager - Gracefully handle renaming on case-insensitive filesystems
    
    Add edge case handling to move/copy commands wherein something is being
    renamed to a different-cased version of itself.
    
    Ex : renaming 'mydocuments' to 'MyDocuments'
    
    https://jira.cyanogenmod.org/browse/BACON-3074
    
    Change-Id: Id90de5fd083e341371f250c0194f200388cf4941

commit fb259f02fa378706b90d98d1e2ae76641ea97a5f
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 17 16:42:32 2015 -0700

    CMFileManager: set compute folder statistics to true by default
    
    Change-Id: Iaf22257a9227722029956094ae06ccf0df524541
    (cherry picked from commit 19862d7c51143136c25d03b741156a0fda68c768)

commit da04013334cb17a23245f33872b10238f82e4382
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Mar 19 17:13:51 2015 -0700

    CMFileManager: set search item icon to fixed width and centerCrop
    
    Change-Id: If89a55a8d1212774709176ae9af7df6f761f9005

project packages/apps/Calculator/
commit 6447be0b3c251525f3625f16838500b2e6a4a602
Author: Matt Garnes <matt@cyngn.com>
Date:   Wed Mar 11 17:24:40 2015 -0700

    Limit history expressions to a single line.
    
    Due to the AOSP bug reported here:
    https://code.google.com/p/android/issues/detail?id=33868
    
    TextViews using android:ellipsize="start" must also specify
    android:singleLine="true" or the app will crash if the length of the
    text goes beyond one line.
    
    Repro steps of the original bug:
    1. Input "3-Sin(3*9/(2+9))"
    2. Tap "=".
    3. Observe that Calculator crashes.
    
    Add android:singleLine="true" to avoid this crash.
    
    Change-Id: Ieb59f0c43674bf8bfeadb9a7fdf0f859f7d281dc

project packages/apps/Calendar/
commit 8d3bd6c49994cb27cb65e8622cc1db2aa4a1cf15
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 13 16:53:39 2015 -0700

    Calendar: support ACTION_VIEW instead of ACTION_SEND
    
    Change-Id: I9b7608a9161b1370a4ee4ab520c0e0e9a0fd9c9c

project packages/apps/Camera2/
commit 982bcc197bc6c035c2efc283a033d6bab5cf86d7
Merge: b656f91 1d98281
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:08:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/Contacts/
commit e98c8a501ab325b15e94a8e5a62b2c40a75b1634
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Mar 18 15:44:29 2015 -0700

    Contacts: Add checkableimageview to sim import picker
    
    Repro:
     - Open contacts, and select Import/Export from overflow menu
     - Import from SIM card
     - Select contact(s)
     - Observe: there's element in the list view to show checked state
    
    Change-Id: Ic5f3a390ea4501cfbef0252cdf6bd50e93b260eb

project packages/apps/Dialer/
commit 0ad236d3698b530f4f24cb08aeb2d77286761bfe
Merge: b7cad7e c44882c
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:08:43 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

commit 1b3a02238dbff81c8331deabb8b362b8c2280d03
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Mar 16 09:15:26 2015 +0100

    Move smart dialer initialization to onStart().
    
    The SmartDialCursorLoader expects the SmartDialPrefix map to be
    initialized when it's created. As
    - the loader is initialized in SmartDialSearchFragment's onStart and
    - the fragment's onStart is called asynchronously after the activity's
      onStart and
    - the map initialization happens in
      SmartDialPrefix.initializeNanpSettings() and
    - the above method is currently called in the activity's onResume()
    
    we have a race condition between the activity's onResume() and the
    fragment's onStart() (at least when processing a dial intent, which is
    what causes the dialpad fragment to be immediately shown).
    
    Fix that race condition by moving the initialization into the activity's
    onStart() and running it before calling the super method to ensure it
    happens before fragments are started.
    
    JIRA:NIGHTLIES-760
    Change-Id: I9767cbba3b177fdd5b1de86914cb1e40d20835ab

commit 158fc5f6c7b586651db2a94e2bdbb52d3364fae5
Author: Sven Dubbeld <sven.dubbeld1@gmail.com>
Date:   Fri Mar 13 13:28:05 2015 +0100

    Added Reverse Lookup Gebeld (NL)
    
    Change-Id: Icc69b9aac2f50f54ab2a97365297620ccd547177

commit 26eee263bdca3040e1f612857beb44fcdb96f66e
Author: Danny Baumann <dannybaumann@web.de>
Date:   Mon Mar 16 09:15:26 2015 +0100

    Move smart dialer initialization to onStart().
    
    The SmartDialCursorLoader expects the SmartDialPrefix map to be
    initialized when it's created. As
    - the loader is initialized in SmartDialSearchFragment's onStart and
    - the fragment's onStart is called asynchronously after the activity's
      onStart and
    - the map initialization happens in
      SmartDialPrefix.initializeNanpSettings() and
    - the above method is currently called in the activity's onResume()
    
    we have a race condition between the activity's onResume() and the
    fragment's onStart() (at least when processing a dial intent, which is
    what causes the dialpad fragment to be immediately shown).
    
    Fix that race condition by moving the initialization into the activity's
    onStart() and running it before calling the super method to ensure it
    happens before fragments are started.
    
    JIRA:NIGHTLIES-760
    Change-Id: I9767cbba3b177fdd5b1de86914cb1e40d20835ab

commit 70f4be0da06a5efc8a7740de6fd4494c631530f3
Author: Sven Dubbeld <sven.dubbeld1@gmail.com>
Date:   Fri Mar 13 13:28:05 2015 +0100

    Added Reverse Lookup Gebeld (NL)
    
    Change-Id: Icc69b9aac2f50f54ab2a97365297620ccd547177

commit 8fccd14502606d549fb0113c3c7b53abb4d8d4ed
Merge: 70f4be0 158fc5f
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 21:30:20 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0
    
    6240a0b38d6824
    
    Conflicts:
    	res/values/cm_arrays.xml
    	src/com/android/dialer/lookup/LookupSettings.java
    	src/com/android/dialer/lookup/ReverseLookup.java

project packages/apps/Eleven/
commit 89c155ccef538edb4382e790b4d1913662925b18
Author: Mikalacki Sava <mikalackis@gmail.com>
Date:   Wed Mar 4 16:18:14 2015 +0100

    Eleven: Show/Hide album art on lockscreen
    
    Added preference option to show/hide album art on lockscreen.
    
    Change-Id: Iea2173288fc279f15abe6675a0ffd582e35ad321

commit 1e2c7ab42f4743610d6a6b30412b26b4235f6192
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Mar 19 01:48:19 2015 +0200

    Eleven: Checkboxes to switches
    
    Change-Id: I41439cc69147db49b08cace87ba3513d34dbac6c

commit e039904bfd75f73709efecfa03627e66313edab7
Author: Mikalacki Sava <mikalackis@gmail.com>
Date:   Thu Mar 19 14:17:20 2015 +0100

    Eleven: fixed broken spacing
    
    Change-Id: I98c9feec97caadd5414ce9fea59d6312db80c56c

project packages/apps/Gallery2/
commit d9001389537cca3481258144a543b9f3cb887bac
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sun Feb 8 06:49:41 2015 +0000

    Moar materialize changes
    
    Change-Id: I2a4987c1220dfb772289c6638648702d26600aa7

project packages/apps/InCallUI/
commit e8c68fc828310532faf6b1921723bfacd1364c55
Merge: e4ef21b f815c10
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:09:32 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 2a181b8c391e7414ffd349eb23b2e374c02cba4c
Author: Linus Lee <llee@cyngn.com>
Date:   Mon Mar 16 19:57:53 2015 -0700

    InCallUI: Adjust dimens for hdpi
    
    The Speaker and the pause button the call gets cut
    off in hdpi - adjust the dimens to make it fix
    
    Change-Id: I8cfdeaf4c21d1fc4f1beeb09fb211f8079981d2b

commit e7d96027a89ab1d103b0a6394fbb59bb9c431c78
Merge: e8c68fc 2a181b8
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 09:12:05 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/Mms/
commit 593c82412cb8dff694b2367f92f656fe458fea31
Merge: a983fbb 2dae5c2
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:10:04 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

commit 98b5989ab45d1c12f5a8ba3eb1006b80d12280a5
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 13 16:54:27 2015 -0700

    Mms: open VCal files instead of trying to send them
    
    Change-Id: I6046a1c29afe41d7e92cb9ac9dd82fe6c9075112

commit a6e39f99d9773d260183ce87dc7d4e14d7bb70a8
Merge: 593c824 98b5989
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 09:12:50 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

project packages/apps/Nfc/
commit 44ee38a2ec9a6f437075fc112a3965784c4d9a55
Author: Martijn Coenen <maco@google.com>
Date:   Mon Jan 26 13:04:25 2015 -0800

    Material Beam icon.
    
    Bug: 17459786
    Change-Id: Id5799cf31a5235d623d548c05c6b8a86107ee5e7

project packages/apps/OmniSwitch/
commit 05f56dac7931b1885a6f4d1e280c314fcd9e8f97
Merge: 7f2ff21 d50ea73
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 22:27:47 2015 -0700

    Merge remote-tracking branch 'upstream/android-5.0' into cm-12.0

project packages/apps/PhoneCommon/
commit a3ac20d162bd67c9140b2afcc41cf35266105f1d
Author: Linus Lee <llee@cyngn.com>
Date:   Mon Mar 16 18:18:22 2015 -0700

    PhoneCommon: Adjust dimens for hdpi
    
    The spacing for the dial pad is too small, so
    create some more space by decreasing the whitespace
    between the dial pad at the top bar
    
    Change-Id: I2775ce417b53f7a69abeb3b8919169024a7714dd

project packages/apps/Settings/
commit 0715fe7863842ff6a318604a09443e91c867e485
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Mar 14 23:26:31 2015 -0700

    Automatic translation import
    
    Change-Id: Ie9f171ed938af04d9012582a39a99ea9cc393ca7
    
    Conflicts:
    	res/values-af/cm_strings.xml
    	res/values-fr/cm_plurals.xml
    	res/values-ko/cm_strings.xml
    	res/values-uk/cm_strings.xml

commit 27e9f89f289ba333f43f88995a38de2a7916519c
Author: chickenfactory <micah.chickenfactory@gmail.com>
Date:   Sat Mar 14 15:03:44 2015 -1000

    fix link of ringer and notif volume [2/2]

commit 88b0deb28f3f80198084d02c2378654d4ffacf0a
Author: Dave Kover <dkover@cyngn.com>
Date:   Sat Mar 14 17:18:32 2015 -0700

    Themes: Allow switchbar text color to be themeable
    
    Better exposing the color of the switch bar text so that a theme
    can handle this assignment separately without having to touch
    framework theme colors.
    
    Change-Id: I81e3430e188f1ee0a22e92aea50878980f9cc61f

commit 5ecbc4f95dddb69361e9a329dd0ade0f9851e4e6
Author: alviteri <davidteri91@gmail.com>
Date:   Mon Mar 16 00:45:50 2015 -0700

    KEY DISABLE: Switch to new cmHardware
    
    This update the following commit: 68eed6a4974b310e458cd1f246acf49a1b5e8f5f

commit 37b96b71fde88111df7e2a9ffd3a8c6fb8c09797
Author: Janson Kang <temasek71@gmail.com>
Date:   Mon Mar 16 11:55:44 2015 +0800

    Fix Settings FC in non-Advanced mode (Buttons Setting)

commit 6560d979c26207b39afd190d89828f2f9857b700
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Tue Mar 17 21:21:59 2015 -0700

    Settings: Support EAP-SIM and EAP-AKA
    
    When adding a network, add EAP-SIM and EAP-AKA authentication methods
    in EAP method. These two methods need SIM card support. 3G SIM card
    supports "SIM" and "AKA".2G SIM card only supports "SIM".
    
    CRs-Fixed: 763183
    
    Change-Id: I6e2faa3c262197010f5982c64a4fc4677ff2dd3c
    
    Conflicts:
    	res/values/bools.xml

commit b095beb8265ccca300c54f114b7fb40886c153e9
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 17 17:35:03 2015 -0700

    Protected Apps: remove incorrect header title
    
    Change-Id: If6c7755b5004d563b0c817b43d8eb67571d8e01b

commit d00ad2705a46aaaf73169a77013494a8c1296d7f
Author: Ricardo Cerqueira <cyanogenmod@cerqueira.org>
Date:   Thu Aug 7 00:55:40 2014 +0100

    Factory reset: Always show the "delete media" checkbox
    
    CM is usually installed with recoveries that preserve datamedia,
    including our own, so the assumption that deleting data will also
    clear personal media is wrong. Always show the checkbox that was
    originally limited to removable media to let the user do a full
    reset
    
    Change-Id: I2764c9509cc9ec50a1be979d748341037660a5da

commit 9fec16fd9ea7d0e4477d8f844c4cd86f3f6f396f
Author: Evisceration <eviscerationls@gmail.com>
Date:   Tue Mar 17 20:49:48 2015 -0700

    (2/2) Settings: custom power key chord actions and delay
    
    Change-Id: I343cd80f50bb9dbc938c3386fd8500cda6881033
    
    Conflicts:
    	res/values/custom_strings.xml
    	src/com/android/settings/ButtonSettings.java

commit 2456da643d0461acf46b0884b7ea7b9ac787a05f
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 17 13:57:17 2015 -0700

    Settings: hide write to NFC in Wifi menu when appropriate
    
    Hide this context menu option when the device does not have NFC.
    
    Change-Id: Ib48b758437dafa654b1e6c243b0662271f7de0ae
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 134c3a7e2b3b76c61eadf9798a322e96f7c97a63
Author: Fyodor Kupolov <fkupolov@google.com>
Date:   Tue Nov 18 15:08:12 2014 -0800

    Added a check if a custom activity can be started
    
    AppRestrictionsFragment starts an activity using an intent provided by the
    receiver. A check was added to prevent an app from starting an activity that
    it does not own.
    
    Bug: 14441412
    Change-Id: Ia6820b1daf3783d605b92976c78cb522b17dc8f2

commit d0b698ee04bb8d9b2827f8a84335224970736579
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Jan 5 13:32:20 2015 -0800

    Settings: add switches for dashboard items
    
    Change-Id: Ibff81510270745807a4b133457d60d47dd629df6
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 77e9c1531be5d2d495a14b78d5a558666f4b8d9a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 20 20:56:59 2015 -0700

    Allow launching display rotation & lock screen settings externally
    
    Change-Id: I69168fea2a43cfa7f2b8474042c35720f4431040
    
    Conflicts:
    	AndroidManifest.xml
    	src/com/android/settings/Settings.java
    	src/com/android/settings/SettingsActivity.java

commit 80bd3ab5ae4a659cd2e2c05d2e9582dddcaa9ff6
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 20 16:54:58 2015 -0700

    Settings: add dashboard switch view for sw600dp
    
    Change-Id: I19797bc2b05539700ab4f3e8bf960fc37047d448
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 75b002bb2e7c67763fb989fff448cfac9113dd9f
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 02:27:06 2015 -0700

    Rework Ad Blocker Update dialog @Miccia94
    
    Add title
    Proper OK button
    
    Change-Id: I2dd37dabd66ec0129d579a746ea6a5c247933e29
    HFM: Add whitelist to HFM
    
    * also fix not being able to switch off the ad disabler
    
    AICPfy
    CheckBox to Switch
    Move settings to main Extras menu
    
    Change-Id: Ifa8adf2313f0c0932882c3ac6cd4bda7e8b250de

commit 61464b2ac0072a4239332b59587f8bfd246d31ce
Author: Cristian Giordano <steel89ita@gmail.com>
Date:   Sat Mar 21 20:21:57 2015 -0700

    Settings: Read CMRemix Center menu
    
    @fusionjack: Remove menu if CMRemix Center is not available
    
    Change-Id: I7af4659a45ec69e47d60b869df4ccce85b943345
    
    Conflicts:
    	res/values/slim_strings.xml
    	res/xml/dashboard_categories.xml

project packages/apps/SlimCenter/
commit db60d06e6b17d49a409487501b46773e1e06912b
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 12:45:33 2015 -0700

    cmRemiX >>> CMRemix

commit f2cc60c10d4e4a7a778ab816b4fd2f724604f55a
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Tue Mar 17 21:20:24 2015 +0100

    Don't check update if update interval is disabled
    
    Change-Id: Ie2fe75837f07f5ce42bb0b7085502387d5c18948

commit 6d905cc586cbff7ada5801bb42fb2c0a2f457052
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 21 19:44:45 2015 -0700

    fixed CMRemix label

project packages/apps/ThemeChooser/
commit 5e1a5f4bc0180a1f4511fd7af2dc2502b549d4e3
Merge: df1b5e2 979a19a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:13:30 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

project packages/inputmethods/LatinIME/
commit 559c5fd84a815e5a9b93c28f076d809db2f55b1b
Author: Sergey Zozulya <s.viper.z@gmail.com>
Date:   Mon Mar 16 18:47:07 2015 +0300

    Fix suggestions text padding (AOSP Keyboard)
    
    Use paddingLeft and paddingRight (as Google Keyboard does) instead of
    paddingStart and paddingEnd to fix text padding in suggestions bar
    
    Before - http://goo.gl/ZjN06c
    After - http://goo.gl/s8f7gr
    
    Change-Id: Ia9f7bac8864c7410fd0b720f54a473f972bdc569

commit 3909e40c68fddbfd3426f1f16f81e7a690c7bd38
Author: Tadashi G. Takaoka <takaoka@google.com>
Date:   Wed Nov 19 13:45:21 2014 +0900

    (DO NOT MERGE) Fix Greek accented upper case letters
    
    Cherry-picked 6fc92899d82f4d3cb30f7bb2c57133154f0babd2 from
    ub-latinimegoogle-edamame-mr1-release.
    
    Bug: 18418991
    Change-Id: Id4dff41ba488635ff9af899be6d4f84ab00a96c8

project packages/providers/TelephonyProvider/
commit bda9e4d340743d1a68d01bec29a44cba756b8ee1
Author: Amith Yamasani <yamasani@google.com>
Date:   Thu Nov 6 09:01:20 2014 -0800

    Make TelephonyProvider a singleton across users
    
    Messaging apps need to access it from secondary users
    
    Bug: 18194892
    Change-Id: Ia7401c287f4b920ac4de5102f33ded22bbf0f5b9

project packages/providers/ThemesProvider/
commit a6afd7e22df46a004d78ad2ed9ec3f1ab2c674b3
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 18 14:07:24 2015 -0700

    Fix icons with filters not being generated
    
    If a theme has composed icons that only use color filters, they
    would not get generated.  This patch resolves that issue.
    
    Change-Id: If9076eca8cce1a85beed54ce30f0dfb8bbcd3188
    REF: CHOOSER-63

project packages/services/Telecomm/
commit 1952939241128b05a19fb44818aed7326482874f
Merge: e44d04d 4e6de9d
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:12:48 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/services/Telephony/
commit dcf923350a299f97e7622e070657e27d08ef29ba
Merge: bc21c0f 98c026a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:13:10 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project prebuilts/clang/linux-x86/host/llvm-Snapdragon_LLVM_for_Android_3.5/
commit 409d9c6ea5def3e3eb926291a80f012243bbcfdd
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 14:33:34 2015 -0700

    itnitial Snapdragon LLVM Compiler for Android v3.5 - Linux64

project system/core/
commit 7466283affe6989c1c462346f3d109e78a2345f4
Merge: 80ec2d9 5d31618
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:57:43 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project vendor/cm/
commit 2b999181c8a7963b81a419366be2e022717f0601
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Mon Mar 16 11:27:10 2015 -0700

    Fix default Alarm tone
    
    Hassium was deleted as a duplicate of Helium. Fix this value.
    
    Change-Id: I27e60c05ebe82d5ba400d84f5466308012a102d6

commit 23c48f6f4f8d3f3377fb74d289178c72bc812da9
Author: percy-g2 <gahlotpercy@gmail.com>
Date:   Fri Mar 13 21:00:05 2015 +0100

    vendor:cm: Add Moto E contributors
    
    Change-Id: I5e560a306b62b172c6ea7855c48a54dbc6193ac4

commit 6ed255db27798763db384cf6683784592e7458a7
Author: Howard M. Harte <hharte@cyngn.com>
Date:   Sat Mar 14 09:02:22 2015 -0700

    Add additional APNs for US Cellular
    
    Change-Id: Ia3e5ccc244ff6b95de1f079571c12591375b847b

commit b62da1e2e1a5b42b8c2bc37ddbb63119b9f8a57d
Author: Byun Jae Myeong <byon0716@gmail.com>
Date:   Sun Mar 15 01:59:12 2015 +0900

    apn: Add LG U+ LTE APN
    
    Change-Id: I5bb329e9b2d5eb76a47db8c0ea2fdd0b853c29e5
    Signed-off-by: Byun Jae Myeong <byon0716@gmail.com>

commit 8df987a37181343070055e66c487aa290f2e2f28
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Mon Mar 16 18:23:44 2015 -0700

    Add USMobile (MVNO) apn
    
    Change-Id: I5cf33256a04e96567d87042e10ed80034a40ec41

commit dc699fb190a7249053c4f2fd280f9dc8a3096fe6
Author: Emerson Pinter <dev@pinter.com.br>
Date:   Thu Feb 12 19:20:19 2015 -0200

    sepolicy: Permissions for userinit
    
    Change-Id: Icaf9d191841a6214925729e40d84a61a2ebf2296

commit eb600fe87cc4874ac4cc8cd90e132a27c381678c
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Wed Mar 18 14:16:28 2015 -0700

    Add new Maxis combined APN
    
    Change-Id: I1981d43e0fffb5ce0d468117490c30cfe0d50055

commit 9c2413bc19fb89a722f3bc251833059d9b19674f
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Thu Mar 19 11:44:59 2015 -0700

    Update Telenor HU APN
    
    Change-Id: I96fc55f7f30fb6203e8729e4cd7c40203adf3420

commit 768292df1d7ae1c975885e683a034cc336bf55c8
Author: Gianmarco Reverberi <gianmarco.reverberi@gmail.com>
Date:   Tue Mar 10 20:16:06 2015 +0100

    SystemUpdateService: enable service but lock its receivers [2/2]
    
    Added SecretCodeReceiver to locked components
    
    Added list of components that need to be forced enabled
    (because they've been previously disabled)
    
    Change-Id: I7cc0efc1830b45bc5384ff421b829e0be0d955d8

project vendor/cmremix/
commit ca0d4766c548de579f4d23f05effa734421ab19b
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 19:02:51 2015 -0700

    CMRemix v12.0

commit f8f80a67d012b194c85972d269a7a6075593cf3c
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 02:59:50 2015 -0700

    remove uneeded mm-dash dependencies and fixed trltexx dependencies

commit 3c427d73d9ba4d43c762d53a844c5c25845f994f
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 19:02:51 2015 -0700

    vendor: ignore recovery size & no recovery for hlte varients

commit c07d56b97d41c0ec59f826147fecb850647c3389
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 02:58:06 2015 -0700

    [2/2] ArchiDroid Optimization
    
    CMREMIX_OPTIMIZATIONS := true

commit 7c65205800833f5c7e09a1c5eda02723d4d2348d
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 02:33:33 2015 -0700

    add extra changelog for Kernel Building

commit ea15c9af8a86aa2b12288aba2dabc59d27eb4b5e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 20:07:42 2015 -0700

    vendor: add CMRemix Weekly_Changelog

commit 4da61eeeec7c288ebbeb019cdf802d46d51f3b00
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 00:51:03 2015 -0700

    disabled cmremix optimization for now

commit e7107d9f8a72cff8c8a0a368826130d4838dbc9b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 20 22:25:37 2015 -0700

    add ANSI color scheme script for CMRemix-ROM

project vendor/samsung/
commit bbdbc2ff202a005a1b5f525f9bc6de3dc7d27a6f
Merge: c0dc795 198ec0c
Author: Arne Coucheron <arco68@gmail.com>
Date:   Sun Mar 15 05:59:26 2015 +0100

    Merge pull request #595 from arco/cm-12.0
    
    Partial revert "serrano: Update blobs"

commit 62a3db74e01e41be7297a92fcf518c49da1601f3
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Sun Mar 15 06:14:03 2015 -0400

    mondrianwifi: Update drm/wv blobs to oppo/msm8974-common
    
    Change-Id: I761f1bf34254293f36f2c67d6024b2f15d9b9e78

commit ba5a78b6fb59548cead84001f9f821503306ba01
Merge: bbdbc2f 62a3db7
Author: Shareef Ali <shareefalis@cyanogenmod.org>
Date:   Sun Mar 15 12:04:43 2015 -0400

    Merge pull request #597 from crpalmer/mondrianwifi-drm
    
    mondrianwifi: Update drm/wv blobs to oppo/msm8974-common

commit 230f491727513ba640cb22c3f21c3d2707234515
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Sun Mar 15 20:12:07 2015 -0400

    mondrianwifi: Update adreno blobs to oppo/msm8974-common
    
    Change-Id: Iec7a5e67af1c0f0b2e25eba80b1c6a7b2118aa41

commit c36d013b647fb2fa86e863c5a304189ecde9ab04
Merge: ba5a78b 230f491
Author: Dan Pasanen <dan.pasanen@gmail.com>
Date:   Sun Mar 15 20:02:10 2015 -0500

    Merge pull request #599 from crpalmer/cm-12.0-adreno
    
    mondrianwifi: Update adreno blobs to oppo/msm8974-common
