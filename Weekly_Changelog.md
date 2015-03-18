
project bionic/
commit d0e6a2759af7c0264ba49f480d001ca6be5e4944
Merge: 9c38646 0e825a7
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:53:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project bootable/recovery-twrp/
commit 910491c881669dd837c0efcf07af8aacb44c5dcc
Author: that <github@that.at>
Date:   Wed Mar 4 22:39:34 2015 +0100

    gui: type safe resources part 2
    
    - separate collections for fonts, images, animations
    - no more ugly casts
    - fix crash if main ui.xml did not define any resources but include did
    - don't stop loading resources if one "type" attribute is missing
    
    Change-Id: I70c1c9ca66ca65d9fba1ba3eded34f3d8a07488e

commit e628d646b4aebd894ce1148ec13f68e70c598715
Author: that <github@that.at>
Date:   Wed Mar 4 23:05:00 2015 +0100

    gui: allow specifying resource type in element name
    
    e.g. '<image ...>' instead of '<resource type="image" ...>'
    
    Change-Id: I5ce04ae0845351c8a4640d12e36f1aaf32e1ebc9

commit 474cacf22fbbcd4825bb7a4ae63d1dfa55992433
Author: that <github@that.at>
Date:   Thu Mar 5 20:25:39 2015 +0100

    gui: support string resources
    
    storing strings in a map (for fast lookup) in resource manager
    
    To define a string resource in <resources>:
    <string name="foo">Hello</string>
    
    To use a string, e.g.:
    <text>%@foo%</text>
    
    Not yet done: language-specific resources (should be solved not only for
    strings, but for all kinds of resources - e.g. for localized images)
    
    Change-Id: I3ba5cf5298c09e0d28a83973e9662f179271b33f

commit 90e1e2dcf5ad89c795b77e9091f0cbee4f807fc9
Author: Vojtech Bocek <vbocek@gmail.com>
Date:   Fri Mar 6 00:28:21 2015 +0100

    Properly disable GGL_TEXTURE_2D after using it in minuitwrp
    
    Change-Id: Ib100ccf3c8f6c622beb40b37ba3f61aad69d7d93
    Signed-off-by: Vojtech Bocek <vbocek@gmail.com>

commit b5f747cc60011b78fd97e6a116cf19dde6b6b6ab
Author: Vojtech Bocek <vbocek@gmail.com>
Date:   Thu Mar 5 20:02:57 2015 +0100

    Implement gr_line() and gr_render_circle()
    
    Change-Id: I63c8dcfa276bbeb550ca051a3a1a0646a2d07dc6
    Signed-off-by: Vojtech Bocek <vbocek@gmail.com>

commit 76d32024c05e0585158f3266edb0e75017ca7f04
Author: Vojtech Bocek <vbocek@gmail.com>
Date:   Sun Mar 8 16:32:41 2015 +0100

    Mount pstore filesystem while in recovery
    
    * pstore filesystem is evolution of ram_console and contains
      kmsg from previous boot (previously in /proc/last_kmsg).
    * Lollipop init.rc does this. If device doesn't have
      pstore fs, it will simply be ignored
    
    Change-Id: Id3bf8763ccde54f87fde5cdf2db511649c376aa4
    Signed-off-by: Vojtech Bocek <vbocek@gmail.com>

commit ba2b25a9010303e6ed7aec9cf1345a551d495389
Author: Matt Mower <mowerm@gmail.com>
Date:   Thu Feb 19 13:19:47 2015 -0600

    toolbox: Cleanup Makefile
    
    * Do not split the makefile in two to support pre-lollipop trees. Go
      through and mark sections with PLATFORM_SDK_VERSION.
    * setenforce: Correct the handling to prevent build warnings -- if
      busybox provides this tool, then still allow it to be built, but do
      not write a symlink.
    * Correct indentation throughout
    * Remove dead code (LOCAL_STATIC_LIBRARIES)
    
    Change-Id: I1b13a0e0be78ea862f7d418d683407ff79d17e4f

commit c5dee9ce81a212cb88f45991071e999fa656f2cd
Merge: 37a1f6a ba2b25a
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 20:46:06 2015 -0700

    Merge remote-tracking branch 'upstream/android-5.0' into cm-12.0

project build/
commit a7532d7e8fedd4d98f7970117b6916730216dac2
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Tue Mar 10 18:58:23 2015 -0700

    build: Update install tools packaging for target-files support
    
    Modifies "build: ota: Support for install tools in /tmp/install" to
    support signing steps being split from build steps.
    
    Package install files into target-files INSTALL path
    Read from target-files for OTA package creation
    
    Change-Id: I64f919c2a757b5474f6cc5f82bd6c33c2a8b558a

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

project cmRemiX/
commit 31e49df9e9d02826cdb1772b58a89bc456a901c8
Merge: 9891cbb ddc4820
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:25:18 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0
    
    Conflicts:
    	default.xml

project device/samsung/hlte-common/
commit 4c4741e0ad0206f7457f7ea0fbe1be981d1933c2
Author: Christer <christer.bjor@gmail.com>
Date:   Tue Mar 10 14:36:35 2015 +0100

    hlte-common: remove bogus MMS overlay.
    
    * This is already taken care of in samsung_qcom-common and is cuasing
    data drops with some carriers after receiving an MMS as well as not
    sending messages over 160 characters on some carriers.
    
    Change-Id: I9f26bc33ed99515f15c881f697917d8c0c3c3cb6

commit 76aaf5245962a528b906ca3371bff1acf22567ef
Author: Christer <christer.bjor@gmail.com>
Date:   Tue Mar 10 14:33:36 2015 +0100

    hlte-common: Removed deprecated Torch config
    
    Change-Id: I12ebee5ae441e44db1830759e8e3c9b1e10a7863

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
commit 5a9bccf5295acaf3824a67fbc274552f6679f0f0
Merge: 16ff27a 1e86927
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:52:04 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit a8b7f6d616845ef469a1367eb1c9c9b27058747a
Author: Tony Layher <layhertony@gmail.com>
Date:   Mon Mar 16 22:50:48 2015 -0400

    trlte-common: Use low latency for primary
    
    Change-Id: I8938139b886eb1ff83500dbdc73441fda2d11e14

project device/samsung/trltexx/
commit 80ec0a28dc0c0f91a1062d7cd4173d7f5b3e1ef6
Author: gekkehenkie11 <allard_addink@hotmail.com>
Date:   Thu Mar 5 15:30:08 2015 -0400

    add support 910G
    
    Change-Id: I7e43f0814da00866d3f100af2d5f1f341c988715

project external/whispersystems/WhisperPush/
commit d3d65686b29bf0d971c272ba2c616e567575c745
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:33 2015 +0200

    Automatic translation import
    
    Change-Id: Iadb061cd812b5ac3af76d16a2ba0e6853f98e0d2

project frameworks/av/
commit 29c4a56d4dedb21f0dc5235b335dbff273456011
Author: Wei Jia <wjia@google.com>
Date:   Tue Dec 2 09:41:21 2014 -0800

    StreamingSource: check mTSParser before dereferencing it.
    
    Bug: 18532335
    Change-Id: I7819d8d359fe75ea4c827138e9aaa2454ccfe3b1

commit 84d61128fbc72aabc22a7f803cd31cff4e73c159
Author: Li Sun <sunli@codeaurora.org>
Date:   Mon Feb 16 11:10:05 2015 +0800

    httplive: avoid zero byte read request
    
    - In LiveSession, check whether maxBytesToRead is zero, if yes
      ignore it because zero byte read request is meaningless.
    
    - In PlaylistFetcher, check whether the read bytes is less than
      the requested block size, if yes, finish fetching the current
      segment file because it means fetching file already meets EOS.
    
    Change-Id: I150d4b147090dbd48d804ebd96ea909e5b6fdbcb

commit 4728e99e8490770439a9425c74308c58bfc737e1
Author: Satya Krishna Pindiproli <satyak@codeaurora.org>
Date:   Wed Oct 22 12:53:35 2014 +0530

    libstagefright: Handle FLAC clips with very small block sizes
    
    - Clips with very small block sizes play with frequent glitches.
    - As per the current design, the parser gives data in frames and
      as the size of each frame after decoding is very small, the framework
      does not receive PCM at the rate at which it expects resulting in
      glitches.
    - Fix is to buffer data in the decoder and to read from parser only
      when needed.
    
    CRs-Fixed: 676591
    Change-Id: I0c79735ac16c0a9a821fbcadc172038a3145941a

commit 1aedb67544e8a7ced54a1e6f7b7cbdfccc16faa3
Author: Satya Krishna Pindiproli <satyak@codeaurora.org>
Date:   Wed Feb 11 19:50:48 2015 +0530

    libstagefright: Reset flac decoder eos during flush
    
    - The CTS test case testDecodeFlac fails when the reset mode
      is RESET_MODE_EOS_FLUSH.
    - In this mode, after input and output eos are set, there is a seek to 0
      but bit-stream is not fetched from the parser resulting in an
      assert that causes the CTS failure.
    - Ensure that the decoder eos is reset in flushDecoder so that bit-stream
      is fetched from the parser.
    - Also fix indentation issues for log messages.
    
    CRs-Fixed: 793060
    Change-Id: I5fc86a7b04f009e91231fa4b20b32da1dac6a9ca

commit 7404a5798ad1bd946664ca556404d5d44213a080
Author: Santhosh Behara <santhoshbehara@codeaurora.org>
Date:   Mon Feb 16 18:44:37 2015 +0530

    httplive: HLS enhancements
    
    - Use the property persist.sys.media.hls-custom to have all
      the customizations enabled in HLS stack.
    
    - Start playback from first segment, in VOD if the
      playback happens at variant corresponding to actual
      bandwidth.
    
    - Increase the duration to buffer to 25sec before
      pausing the PlayListFetcher.
    
    Change-Id: I8a676c77db54205521bf6db7a69e0766da3220c5

commit 1abd0c511a4509074097707945681154900b50de
Author: Dhananjay Kumar <dhakumar@codeaurora.org>
Date:   Wed Dec 31 20:10:33 2014 +0530

    soundpool: reuse channel for same sample if available
    
    Reuse channel for same sample if the channel completed
    current playback and is not reallocated to another sample,
    i.e. not stolen by other sample.
    
    CRs-Fixed: 769440
    Change-Id: Ibe7ee318c7dc11f3c4fd3a2f57d861318b10973b

commit 6a054d6b999d252ed87b4224f3aa13e69e3c56e0
Author: Pavan Chikkala <pavanc@codeaurora.org>
Date:   Wed Feb 18 17:31:13 2015 +0530

    libstagefright: Add check for bits avail to read
    
    - If number of bits available to read from ABitReader
      is zero,do not call getBits.
    
    Change-Id: I4b7332b03ed6ee1d7b6711e5b4c5dce396151b03
    CRs-Fixed: 777657

commit 8b91c593e00b70ba8157da8479d6bde635b44513
Author: Steve Kondik <steve@cyngn.com>
Date:   Wed Mar 11 21:51:45 2015 +0100

    stagefright: Correct ifdeffage of some QC codecs
    
    Change-Id: Ie8cc7287967b84e09941283559ca542efd928d91

commit ba94bd7a60b96e4e565b05f6d0b7e64f055dd659
Merge: aae6dae 29c4a56
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 20:27:51 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

commit 33ade411b74fd0bbef24a8ee73c8938432a40831
Author: Divya Narayanan Poojary <dnaray@codeaurora.org>
Date:   Tue Feb 17 11:19:01 2015 +0530

    audiopolicy: Do not route VoIP call to HDMI
    
    getDeviceForStrategy is returning AUDIO_DEVICE_OUT_AUX_DIGITAL
    even  when setForceUse is called with FORCE_NONE(earpiece)
    during VOIP call. Actual Intention is to route audio for phone
    strategy to AUX device even after setForceUse is called with
    FORCE_NONE when not in voice call. It is supposed to exclude
    VOIP call too
    
    Added isInCall check so that it returns EARPIECE when
    setForceUse is called with FORCE_NONE
    
    CRs-Fixed: 793649
    
    Change-Id: I88d515c351f066305f9eed240b1fe5f60ef34f85

commit 649b5fbafeeabc90ac0a69a176ba696f155f2282
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Mar 14 22:31:38 2015 +0200

    libmedia: Tone down logging
    
    * Originally added in 8c6297e4a78a97cac2c9c4b855828dc06c356686
    
    Change-Id: Ieca88e86fff3540a46112c8f9bcf8c9ce92bcb7c

commit 4bd7b86d9ecfb111bdff262d769f20125990842a
Merge: ba94bd7 649b5fb
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:53:07 2015 -0700

    Merge remote-tracking branch 'Upstream/cm-12.0' into cm-12.0

project frameworks/base/
commit 4d28b087acca198e2b2a253cfe3552d98d94b3a3
Author: arter97 <qkrwngud825@gmail.com>
Date:   Tue Mar 10 19:54:03 2015 +0900

    Revert "Fix memory leak in system_server when screen on/off"
    
    This reverts commit bee24ba9431c1f1619f046c7753502a9817dd31e.

commit f9ab65e4b26781af734faa9d8669f5d07f4a38a3
Author: Michael Wright <michaelwr@google.com>
Date:   Thu Jan 8 14:30:47 2015 -0800

    Clean up graphics resources.
    
    Release SurfaceTexture after use in ColorFade and delete GL resources
    in ImageWallpaper.
    
    Bug: 17871993
    Change-Id: I05bda03657ca502ba35b7187b6f361018f7ef687
    Signed-off-by: arter97 <qkrwngud825@gmail.com>

commit ef725f84374816e91d0c3df4f34a660867bf331b
Author: d34d <clark@cyngn.com>
Date:   Tue Mar 10 16:45:59 2015 -0700

    SysUI: Clip to outline in ActivatableNotificationView
    
    This will ensure the entire notification is clipped to the background
    drawable.  If that drawable is a shape, such as a rounded rectangle
    then the entire notification should be clipped to that.
    
    Change-Id: I0a59712618223f28325126e2f0b96b4cfe000fbe
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/91042/

commit 54f264602084ed9618769cae46411a3fee693c82
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 10 17:21:27 2015 -0700

    SystemUI: allow lock screen visualizer to be disabled
    
    Change-Id: I36a81071ad0d8f898b17a5e72ebea48672e62b9c
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java

commit 031329c86e448bc566c263739b989a724c408409
Author: Steve Kondik <steve@cyngn.com>
Date:   Wed Mar 11 01:25:55 2015 +0000

    media: Scan Monkey Audio files
    
     * We've had APE codec support forever, but we weren't
       actually recognizing it at the framework level.
     * Fixit.
    
    Change-Id: Icbbf591a63b8e7066c24f2d01065b9a6979b8cb0

commit dffcf45f1a7e5f527101deee5576d9f6d77ea94c
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Mar 10 17:46:53 2015 +0100

    FWB: Dotted circle battery (1/2)
    
    thx to Griffin Millender
    
    Change-Id: I6ba0ebfd7f8e10c39d43c282b48ffca61461e78d

commit 7287771dd11ef9494d09e86a499b0631985a97c5
Author: Steve Kondik <steve@cyngn.com>
Date:   Mon Mar 9 00:34:55 2015 +0100

    livedisplay: Add "off" state and fix issues with QS tile
    
     * It was previously assumed that "day" was the default setting that
       would be used the same as "off" would, but this is confusing and
       also doesn't allow for a custom day temperature.
     * Add a new state for "off" to simplify this, and handle it
       appropriately. We won't show "day" in the QS tile if both "off" and
       "day" are set to 6500K.
     * Also fix bugs in the QS tile.
    
    Change-Id: Ie8e6ebdd83c9275fb7707844b8f054dcbff48a0b

commit 2a79a7651cd4c72553f8fc596a352e8976d31efc
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Mar 9 21:04:08 2015 +0000

    Revert "systemui: Fix race condition in setting notification panel height"
    
    This reverts commit 257b3d48f3efe54cf6616bbcc9c761a470f70efd.
    
    Change-Id: I0fa1a3a5bc181f259c0248662c9c78524f21c9cc
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/90960/

commit 8837002a9a280be6b017ca37d8e371632c1852dc
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 10 17:20:23 2015 +0000

    Revert "systemui: Fix KeyguardMonitor callbacks during configuration changes"
    
    This reverts commit 0beb0fcad4678241b8f5bfe13e81a8ced62cd05c.
    
    Change-Id: Ib8d5e1ba90a1ca4c48987a6232e3743d4ab4c8d8
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/91012/

commit 4c7f982febc77a4c31e9d850fc5d45a626740118
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 4 16:28:29 2015 -0800

    Themes: Add previous value and update time to mixnmatch [1/2]
    
    Change-Id: I546f8177cec86005293b8a680766c4b08aace0c1

commit d70d50b51b917bdf92f0c6d3cebf87ab76af712e
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 10 15:51:38 2015 -0700

    qsutils: use package manager to query whether nfc is present
    
    The NFC Manager may not have come up at this point, let's use a static
    runtime check.
    
    Change-Id: I72668e7efad3f109890aff0c0d422bb08f82c533
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit fe8eec3009511a9df61889409f9bffd225a06ab8
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 21:59:29 2015 -0700

    SystemUI: improve recreating statusbar
    
    - Don't recreate controllers if they are already there
    - Register receivers only the first time
    - Set proper empty shade state after creation
    - pause command queue a little earlier than right before creating new
      views
    - collapse notifications panel so the views can be recreated properly
    
    Change-Id: Id3fb285cd12e7e63564ff52886d7de5a97744a9c
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Patchset: 4
    http://review.cyanogenmod.org/#/c/91014/

commit 085c85b9feae94f641a48d91042ebf4b5aea7004
Author: d34d <clark@cyngn.com>
Date:   Tue Mar 10 16:45:59 2015 -0700

    SysUI: Clip to outline in ActivatableNotificationView
    
    This will ensure the entire notification is clipped to the background
    drawable.  If that drawable is a shape, such as a rounded rectangle
    then the entire notification should be clipped to that.
    
    Change-Id: I0a59712618223f28325126e2f0b96b4cfe000fbe

commit 1c36a6eeac39ef39a23b8ca925466c733cc8ccbe
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 22:03:05 2015 -0700

    Revert: FWB: LS weather disabler (1/2)
    
    PS2: No more FC
    
    Change-Id: I551fbbcb78712e8b04fcd316561f117693056bfc
    
    Conflicts: (reverted from commit 4f928d3dc259309fb130cb34bfcde000e4b6ea07)

commit 6e58317c7e805f07e6f61bd986fc7e761df95296
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Wed Mar 11 22:06:01 2015 -0700

    FWB: Proper LS weather switch from XXMrHyde
    
    Change-Id: I9b730d53ac4bc40be77dab91e9f361a3ad970dcd
    
    Conflicts:
    	core/java/android/provider/Settings.java

commit 2d75d887e0a6abac5165dda37ee462118d96372d
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Mar 12 22:15:48 2015 -0700

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

commit a9e1dad376a43f6f0554290b39fed5cb5830f950
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Wed Mar 11 02:11:17 2015 +0100

    keyguard: don't use eq visualized in LowEndGfx devices
    
    Eq Visualizer is a costly graphics operation which can impact in devices with old graphic hardward
    
    Change-Id: I21b0e0c2fcf237fee4e11c312ff85d3c421ca575
    JIRA: NIGHTLIES-826
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/91052/

commit df9a1888f25bce847a525cce75e2955cd5453cee
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

commit 5a77c39cab4f76805b26b58a73fabc2fa926add9
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 11 11:23:15 2015 -0700

    Themes: Process theme resources after package scanned [1/2]
    
    This patch processes a theme's resources after the package is
    scanned and the theme is added to the PackageManager.
    
    Change-Id: I098e7e8bd192a8ead0c382ff60e28701c064329c

commit 35ac9761cbb3d75b1a6840aacb5cd1efbdc9ea4f
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 14:01:30 2015 -0700

    SystemUI: disable visualizers during power save mode
    
    Change-Id: I2ab4502d2654d1bcfe19782a600fe35585085b9a
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/qs/tiles/VisualizerTile.java

commit c0d100467bae1e48570a7129034429e0577e530c
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 12:13:05 2015 -0700

    SystemUI: improve DISMISS_KEYGUARD_SECURELY_ACTION behavior
    
    When the screen is not yet turned on, calls to dismiss() will never
    actually dismiss the keyguard since it goes through the bouncer, which
    checks if the screen is on before executing its logic. If we receive the
    intent to dismiss the keyguard while the screen is off, wait until its
    turned on and then execute the dismiss.
    
    Change-Id: I652458c639230bc7fe32a955e103e40c27289b4d
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 34c25f8bc03eda23322ee78ab839715942b5ac90
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 15:16:13 2015 -0700

    SystemUI: don't display protected lockscreen shortcuts
    
    If an app was protected, do not display that app in the lockscreen.
    
    Change-Id: I301a43c8f512e358d47f559320fef490751571ca
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit a7eca79ea13fa9c59a6bb393c6210831f6b8203c
Author: padarshr <padarshr@codeaurora.org>
Date:   Fri May 23 21:05:18 2014 +0530

    Provider: Add multi SIM ringtone support in SettingsProvider
    
    This change will handle multi-sim queries in
    SettingsProvider.java when openFile and
    openAssetFile APIs are called by other components.
    Thus, it will ensure to play the correct ringtone
    corresponding to the SIM.
    
    CRs-Fixed: 661216
    Change-Id: I7b22c233b9c41669c1ad948b83a7aa2c55442af1

commit c841dff6545880658e1837e8861137436ffb38ff
Author: Danesh M <daneshm90@gmail.com>
Date:   Wed Nov 12 12:16:57 2014 -0800

    MediaScanner : Add support for default ringtones per sim
    
    Change-Id: I1ed112a38d2b3676e31a78eb70ea0e16a3957b02

commit 1caa839efeec53df095eec9bfca1b7878767e544
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Tue Mar 3 17:42:09 2015 -0800

    Remove more duplicate sounds
    
    Best testing area is DeskClock alarm sound > Ringtone
    
    Change-Id: I5085382b3b8dae66f415691436ce297f684cb892

commit 2b640a91f41344d842cf820e0d11adec08b60e0b
Author: d34d <clark@cyngn.com>
Date:   Thu Mar 12 12:15:38 2015 -0700

    Themes: Add CONFIG_THEME_FONT to Configuration.diff()
    
    We were updating this change in updateFrom() but forgot to add it
    to the diff() method, which resulted in fonts not changing.
    
    Change-Id: I88e230f3b148ec7efff095d54186018195e2feec

commit 1e35c0e53a7d7d8803095cffebc61417c9ce6cb0
Author: XXMrHyde <xxmrhyde@gmx.co.uk>
Date:   Thu Mar 12 14:49:43 2015 +0100

    Lock screen: Text and icon colors, (1/2):
    
    - Global lock screen text color
    - Global lock screen icon color
    
    The weather panel is using the global lock screen colors
    
    This won`t colorize the pattern-, password-, pin-
    and face unlock views, this will follow in one of the next commits.
    
    Change-Id: I6e5591b4d78ee703d01ebd14382a2ce7b162d9a6

commit 860b6434529108a774c8f2c3831146e7f06553b6
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Mar 12 20:17:25 2015 -0700

    (1/2) Frameworks: allow to toggle smart cover wake
    
      * disable by default
    
    Change-Id: I83d96696fefedc19fc3bce7265a4fcf2d4c894bc
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 0f03d95ae9f5ee7f08c7020dcf688258e0c52989
Author: tiger_huang <tiger_huang@htc.com>
Date:   Mon Feb 16 21:37:12 2015 +0800

    Wait for visible wallpaper drawn before starting app transitions
    
    If the opening app has wallpaper, when the closing app starts hiding,
    the wallpaper would be revealed. It would be nice if we play the app
    transitions while opening apps, closing apps, and visible wallpapers
    are all drawn.
    
    https://code.google.com/p/android/issues/detail?id=150811
    
    Change-Id: I3c7d140f6f6e43e18119e48f9cab441ee96b17e5
    
    Conflicts:
    	services/core/java/com/android/server/wm/WindowManagerService.java

commit 801f53c7812cac99c2c6cd57dff334a04f757e55
Author: tiger_huang <tiger_huang@htc.com>
Date:   Tue Feb 17 14:07:40 2015 +0800

    Wait for opening apps ready before stopping freezing display
    
    When the screen rotation is changing, we will freeze the display
    until all the window surfaces are all drawn (this is not including
    windows which have no surface). If the opening app's window surface
    is created after we stop freezing the display, there would be no
    waiting for the app, and the user would see the black screen.
    
    In this change, we would not only wait for the windows which have
    surface, but also wait for the windows about to have surface before
    stopping freezing display.
    
    https://code.google.com/p/android/issues/detail?id=150921
    
    Change-Id: I7de4db8ca902236f3e9f730b04dbde681cf8c032

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

commit 9115dfb3740cf25f8a2733faf09edbd2525367db
Author: Gianmarco Reverberi <gianmarco.reverberi@gmail.com>
Date:   Mon Mar 16 20:02:15 2015 +0100

    SystemUpdateService: enable service but lock its receivers [1/2]
    
    Added a check for ensure that disabled components are not
    re-enabled at runtime
    
    Added code for forcing enable of previously disabled components
    
    Change-Id: Icfcfa26ccb85028d32edbb5cdb3dd7cdae85b720
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/91579/

commit cc46e54a466da9852dcbbe57bfd45c3987596280
Author: tsubus <tsubus@ilwt.org>
Date:   Sat Mar 14 23:47:03 2015 +0100

    Do not start music app when headset is unplugged
    
    Change-Id: Ic56ba6c30a72deaf119da40e65ca83a9dcc35c43

commit 9a84d5d7c83e629ab35d2526521763ef043f6861
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:10:23 2015 -0700

    Frameworks/base: Fix missing cast
    
    Without a cast, the division is integer division.
    
    Change-Id: I050e53778de8b1591a0be16ebbee8eed70eb1528

commit cbb1a36ac281aaa0736db78d501adb9ff75975b2
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:19:43 2015 -0700

    Frameworks/base: Fix always-false equals
    
    Rect != Insets.
    
    Change-Id: I3d4ff890608e446b51f09a1b633af742f0c069d4

commit d0785060d27c965cb5bd90037ffd400c43ce13a7
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 14:38:59 2015 -0700

    Frameworks/base: Fix a hashCode implementation
    
    Equals uses Arrays.equals. That means two responses are equal if
    the content of the data arrays is equal. By convention, the hash
    code of those objects should agree. In that case one cannot use
    hashCode on the array (which is the identity hash code).
    
    Change-Id: Icce8e2e71e9142421f5dac8a0ee8a211623fb704

commit 5f2939fb628c402d4536435659136bba49692476
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:07:19 2015 -0700

    Frameworks/base: Fix null-pointer check
    
    Change-Id: I715a21c313e909ae654e0c1aa67bdf7bcd89de76

commit 53d2e9041f914b15ec424989a5181dbff03e459e
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:39:21 2015 -0700

    Frameworks/base: Use equals for Integer comparison
    
    Integer == is dangerous, as equal objects may not be identical
    objects. In fact, MediaFormat.setInteger was creating a new object
    every time.
    
    Change MediaFormat.setInteger and setLong to use valueOf, which
    may reuse returned objects.
    
    Change-Id: Iedcc6003adbf05c0c870aa4b3ada7f181a5b870e

commit d981f045bc16e2dd2e435e4b4f88b0da04e35e9d
Author: Andreas Gampe <agampe@google.com>
Date:   Sun Mar 15 15:57:30 2015 -0700

    Frameworks/base: Check before foreach in Script
    
    According to the if below, ains == null is potentially valid. But
    the foreach loop would throw a NullPointerException.
    
    Change-Id: I4460fb1357eaa3abfe0ab9a21effb608f474ab51
    
    Conflicts:
    	rs/java/android/renderscript/Script.java

commit 47011b860f86d161d3c6a8d77b46fe70053080ed
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

project frameworks/opt/chips/
commit 15785bcd55931e3b24f791ec846586a1b295b007
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Thu Mar 12 05:00:24 2015 +0100

    chips: fix NPE errors
    
    Avoid access to potencial null references. Only chips_autocomplete_recipient_dropdown_item has
    all the suggested contacts views. Only remove objects with valid destination references
    
    Change-Id: I0e53d76a9bb6d319511269568a32104c8ffd3521
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

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
commit dae53778d37c31cc60318c5998393e930f7501d5
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:03:48 2015 -0700

    kernel/power/powersuspend: new PM kernel driver for Android w/o early_suspend v1.7 (faux123/Yank555.lu)
    
    - do only run state change if change actually requests a new state

commit 2fecf66725b34f3ce2f387fe4c766299072e27fa
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:04:54 2015 -0700

    intelli_plug: intelligent hotplug cpu driver with eco mode - squashed committ to v3.8 (faux123)
    
    intelli_plug: intelligent hotplug cpu driver with eco mode
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	arch/arm/mach-msm/Kconfig
    	arch/arm/mach-msm/Makefile
    intelli_plug: tweak for faster wakeup from suspend
    
    bump version to 1.1
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: increase cores on persistence
    
    also replace hardcoded values with Macros for ease of updating later
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: make it gcc-4.6.x eabi compatible :p
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: use rq_stats to help detect artificial or constant loads
    
    benchmarks often create fake / artificial loads at a constant rate.  These
    type of loads are not detected corectly by run average algorithms. Use
    the run queue stats to help detect these cases and bring up the cores in
    correspondence.
    
    bump version to 1.2
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: use mp_decision() algorithm for core 3 and 4
    
    This replaces the simplistic check for run queue thresholds with a more
    sophisticate algorithm with time awareness
    
    bump version to 1.3
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: tweak mp_decsion parameters and remove unused logic
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: bump threshold slightly for better response
    
    Signed-off-by: faux123 <reioux@gmail.com>
    wip: intelli_plug: change logic for better benchmark performance
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: use mp_decision to reduce online persistence count for cores
    
    this should bring down the cores faster when run queue is low
    also optimized code a bit using local vars
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: disable by default
    
    let the user enable via sysfs so it won't clash with mpdecision which is
    enabled by default for qualcomm phones
    
    Signed-off-by: faux123 <reioux@gmail.com>
    intelli_plug: slow down hotplug activity from 50ms to 200ms
    
    this will reduce the hotplug chaos which may in turn save more power
    
    Signed-off-by: faux123 <reioux@gmail.com>
    
    Conflicts:
    	arch/arm/mach-msm/intelli_plug.c
    intelli_plug: code clean up and minor bug fixes
    
    bump to version 1.6
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelliplug: replaced deprecated early_suspend driver with userspace interface
    
    early_suspend has been deprecated, so move original functionality to sysfs
    interfae and have userspace app to replicate the early_suspend functionality
    
    bump version to 1.7
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add dynamic load sampling rate logic
    
    Add dynamic sampling logic based on load. If load is high and required more
    than 2 cores, increase the sampling rate for a duration of 3 seconds to help
    manage the load better during this time.  Once duration expires, revert back
    to lazier sampling rate for better batter performance.
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add new power_suspend PM driver
    
    bump version to 1.9
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add touch input logic
    
    changed intelli_plug sampling rates and bump to version 2.0
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: use a context safe function call instead
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: performance tune-up continued...
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: switch to use dedicated high priority workqueue
    
    from the shared global workqueue.  This should prevent hang ups while the
    global workqueue is busy and cleaned up some logic issues.
    
    give input boost its own workqueue
    
    bump to version 2.2
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: code review clean up
    
    set def sampling rate to something sane rather than zero (instantaneous
    rescheduling is not good if intelli_plug is disabled)
    
    make touch input more generic rather than tied to a touchscreen driver
    
    remove unused code
    
    thanks to @dorimanx for the code reviews and suggestions
    
    bump to version 2.3
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    Intelli_plug: add wakeup cpufreq boost for quicker wakeup
    
    bump version to 2.4
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add screen off max controls
    
    bump to version 2.5
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add parameter to control touch boost on/off
    
    bump version to 2.6
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: refactor stats calculation code to be less intrusive
    
    this is done for those kernels which do not have 100% source code available
    and must use existing closed source modules such as wifi drivers
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	kernel/sched/sched.h
    Intelli_plug: kernel sched/core: add per cpu nr_running stats
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add profiles support and misc code optimization
    
    bump to version 3.0
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: use per cpu nr_runnings stats for unplugging cores
    
    bump version to 3.1
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: allow cpu_nr_running_threshold to be user adjustable
    
    bump version to 3.2
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: tweak cpu_nr_running threshold
    
    and fix minor logic issues
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: remove legacy msm_rq based code
    
    just use the original algorithm based on nr_running_stats
    
    bump version to 3.3
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add nr_running_thresholds based on thread capacity of SOC type
    
    instead of hard coded nr_running_thresholds, perform compile time calculation
    of thresholds based on thread capacity of SOC types.
    
    bump version to 3.4
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: misc minor code fixup post 3.4 update
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add automatic dual-core initializations
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: deprecate eco mode. replaced by built-in profile
    
    bump version to 3.5
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: add eco-extreme profile for more dual core use options
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: post 3.5 tweaks and code clean up
    
    bump to version 3.6
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: move to its own directory. It's been cross platform for a while
    
    intelli_plug driver has been working on OMAP44xx, TEGRA 3, Exynos and
    MSM Krait/Cortex multi-core SOCs.  So it doesn't make sense to patch on a per
    SOC basis, move it to its own ARM platform independent folder so patches can
    apply to all supported ARM platforms
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	arch/arm/mach-msm/Kconfig
    	arch/arm/mach-msm/Makefile
    intelli_plug: unify powersuspend and earlysuspend drivers
    
    also minor clean up on the persist logic
    
    bump to version 3.7
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: adjust thread capacity for Cortex A7 SOCs
    
    Cortex A7 is much weaker than Krait processors
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: fix thread capacity threshold calculation
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: fix logic error for eco mode profiles
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: only apply suspend/resume logic if active
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: fix incorrect cpufreq API usage
    
    This resolves the wakeup kick and screen off max issues
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: initialize ip_info struct element during driver init
    
    this will eliminate race issues
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: use primary CPU's info data for non-boot cpu's settings
    
    Async CPU design has caused quite a bit of grief for controlling cpu
    frequencies
    
    bump to version 3.8
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    intelli_plug: older Qualcomm kernel compatibility fixup
    
    ARGH... really angry at CAF code.
    
    some cpufreq driver APIs are incredibly unstable with some of the older
    MSM kernels.  The correct way is the fix the cpufreq drivers, but there are
    tons of variations out there, so rather than depending on a fix, make
    intelli_plug more universal by avoiding the troubling APIs altogether
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 3db89ac33c8c2d48afb5d1bebe95caf5f4bf4d63
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:07:15 2015 -0700

    drivers/cpufreq/cpu-boost: Allow input boost code to be excludable in defconfig (Yank555)

commit 33e1385e31476fca6fe3fd5cba64aabdbbd30644
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:09:24 2015 -0700

    Sound Control: initial bring up for Nexus 6 Linux 3.10 kernel driver (faux123)
    
    Initial import of FauxSound Driver 3.6 from 3.4 linux kernel drivers tailored
    for Nexus 6
    
    GPL Copyright 2014 Paul Reioux (Faux123)
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 01ef44ea94a9a0b2185ee61d3d031bb4a734924a
Author: myfluxi <linflux@arcor.de>
Date:   Sun Feb 9 21:33:28 2014 +0100

    PM: devfreq: Fix simple_ondemand crashing on startup
    
    simple_ondemands private data must be set to NULL, otherwise we would
    run into a NULL pointer in kgsl_devfreq_get_dev_status().
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 7066139f10dcb3c626cabf521f376228f74c1410
Author: Paul Reioux <reioux@gmail.com>
Date:   Thu Jan 15 03:01:02 2015 -0600

    Simple GPU Algorithm: Initial coding for devfreq based Adreno Drivers
    
    This is an open source user configurable simple GPU Control Algorithm used to
    replace the closed sourced Qualcomm TrustZone GPU controller
    
    Copyright 2011~2015
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit e6da331796d689af40ceaa2113747487e9c9e4d9
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:13:07 2015 -0700

    cpufreq: CPU max. hardlimit v2.1 (Yank555.lu)
    
    - initial port to shamu
    
    SysFs Interface :
    
     * /sys/kernel/cpufreq_hardlimit/scaling_max_freq_screen_on (rw)
     *
     *   set or show the real hard CPU max frequency limit when screen is on
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_max_freq_screen_off (rw)
     *
     *   set or show the real hard CPU max frequency limit when screen is off
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_min_freq_screen_on (rw)
     *
     *   set or show the real hard CPU min frequency limit when screen is on
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_min_freq_screen_off (rw)
     *
     *   set or show the real hard CPU min frequency limit when screen is off
     *
     * /sys/kernel/cpufreq_hardlimit/wakeup_kick_freq (rw)
     *
     *   set or show the wakeup kick frequency (scaling_min for delay time)
     *
     * /sys/kernel/cpufreq_hardlimit/wakeup_kick_delay (rw)
     *
     *   set or show the wakeup kick duration (in ms)
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_lo_freq (rw)
     *
     *   set or show touchboost low frequency
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_hi_freq (rw)
     *
     *   set or show touchboost high frequency
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_delay (rw)
     *
     *   set or show touchboost delay (0 = disabled, up to 10000ms)
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_eventcount (rw)
     *
     *   set or show touchboost eventcount necessary to go into high frequency (1-10)
     *
     * /sys/kernel/cpufreq_hardlimit/userspace_dvfs_lock (rw)
     *
     *   0 = allow changes to scaling min/max
     *   1 = ignore (don't apply, but don't return an error)
     *   2 = refuse (don't apply, return EINVAL)
     *
     * /sys/kernel/cpufreq_hardlimit/available_frequencies (ro)
     *
     *   display list of available CPU frequencies for convenience
     *
     * /sys/kernel/cpufreq_hardlimit/current_limit_max (ro)
     *
     *   display current applied hardlimit for CPU max
     *
     * /sys/kernel/cpufreq_hardlimit/current_limit_min (ro)
     *
     *   display current applied hardlimit for CPU min
     *
     * /sys/kernel/cpufreq_hardlimit/version (ro)
     *
     *   display CPU freq hard limit version information

commit 68655ec5b2e264d5f509139dcb379410d7e99518
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:14:43 2015 -0700

    cpufreq: CPU max. hardlimit v2.2 (Yank555.lu)
    
    - cpufreq pushed to cpu0 only "force cpuN policy to match cpu0 when setting min freq" (Imoseyon) takes care of the rest
    - touch detection completely rewritten (now device independant, more lightweight)
    - userspace dvfs lock code updated to hammerhead (was Note 3 code)
    - hook to mdss display panel if powersuspend is not available
    - slight code cleanup
    - debug output switchable in defconfig
    
    SysFs Interface :
    
     * /sys/kernel/cpufreq_hardlimit/scaling_max_freq_screen_on (rw)
     *
     *   set or show the real hard CPU max frequency limit when screen is on
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_max_freq_screen_off (rw)
     *
     *   set or show the real hard CPU max frequency limit when screen is off
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_min_freq_screen_on (rw)
     *
     *   set or show the real hard CPU min frequency limit when screen is on
     *
     * /sys/kernel/cpufreq_hardlimit/scaling_min_freq_screen_off (rw)
     *
     *   set or show the real hard CPU min frequency limit when screen is off
     *
     * /sys/kernel/cpufreq_hardlimit/wakeup_kick_freq (rw)
     *
     *   set or show the wakeup kick frequency (scaling_min for delay time)
     *
     * /sys/kernel/cpufreq_hardlimit/wakeup_kick_delay (rw)
     *
     *   set or show the wakeup kick duration (in ms)
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_lo_freq (rw)
     *
     *   set or show touchboost low frequency
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_hi_freq (rw)
     *
     *   set or show touchboost high frequency
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_delay (rw)
     *
     *   set or show touchboost delay (0 = disabled, up to 10000ms)
     *
     * /sys/kernel/cpufreq_hardlimit/touchboost_eventcount (rw)
     *
     *   set or show touchboost eventcount necessary to go into high frequency (1-10)
     *
     * /sys/kernel/cpufreq_hardlimit/touchinput_dev_name (ro)
     *
     *   display the used touch device name (only if debug set in defconfig)
     *
     * /sys/kernel/cpufreq_hardlimit/userspace_dvfs_lock (rw)
     *
     *   0 = allow changes to scaling min/max
     *   1 = ignore (don't apply, but don't return an error)
     *   2 = refuse (don't apply, return EINVAL)
     *
     * /sys/kernel/cpufreq_hardlimit/available_frequencies (ro)
     *
     *   display list of available CPU frequencies for convenience
     *
     * /sys/kernel/cpufreq_hardlimit/current_limit_max (ro)
     *
     *   display current applied hardlimit for CPU max
     *
     * /sys/kernel/cpufreq_hardlimit/current_limit_min (ro)
     *
     *   display current applied hardlimit for CPU min
     *
     * /sys/kernel/cpufreq_hardlimit/version (ro)
     *
     *   display CPU freq hard limit version information

commit 956e4460b4f6159305e2732da37ade308fae9b08
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:18:29 2015 -0700

    msm: mdss: savoca's KCAL pp control adapted for shamu (via imoseyon)
    
    SysFS Interface :
    
    rgb : /sys/devices/platform/kcal_ctrl.0/kcal
    rgb_min : /sys/devices/platform/kcal_ctrl.0/kcal_min
    switch : /sys/devices/platform/kcal_ctrl.0/kcal_enabled
    invert : /sys/devices/platform/kcal_ctrl.0/kcal_invert
    saturation : /sys/devices/platform/kcal_ctrl.0/kcal_sat
    hue : /sys/devices/platform/kcal_ctrl.0/kcal_hue
    gamma : /sys/devices/platform/kcal_ctrl.0/kcal_val
    contrast : /sys/devices/platform/kcal_ctrl.0/kcal_cont

commit 6911ec30a829648608aec3cd8022aeed14626d48
Author: savoca <adeddo27@gmail.com>
Date:   Thu Feb 19 19:37:09 2015 +0000

    msm: mdss: Replace PGC implementation with PCC for KCAL
    
     - Unify enable/update routines
     - Remove no longer used update call from probe function
     - Pass lut_data struct to all kcal/mdss functions
     - Thank you to @cyanogen for PCC code reference

commit 10125891e76f09adc7835ebcb7a3a9b0512b55b6
Author: savoca <adeddo27@gmail.com>
Date:   Fri Feb 20 20:38:31 2015 +0000

    msm: mdss: Add pa_v2 support to KCAL
    
     - Thank you @engstk for testing

commit ba69a437c9ef7e6221faa288dea4e9f15c890867
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 20:21:50 2015 -0700

    intelli_thermal v3.0: initial coding for Linux 3.10 Qualcomm kernels (faux123)
    
    Intelli_thermal is a replacement for the existing Qualcomm msm_thermal engine.
    It allows users greater controls over the stock Qualcomm thermal engine while
    maintaining full backwards compatibilty.
    
    Copyright 2014~2015 Paul Reioux (aka Faux123)
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 029c104d280b9715b2284875b28e3fa0a41faad2
Author: imoseyon <imoseyon@gmail.com>
Date:   Fri Nov 28 13:08:09 2014 -0800

    cpufreq: force cpuN policy to match cpu0 when changing freq or gov
    
    (cherry picked from commit c1b47d6e76e10afd5e874ec54192ffd2cc1adf64)
    
    (cherry picked from commit c1b47d6e76e10afd5e874ec54192ffd2cc1adf64)

commit 4f0f9a25a863ce21f0dfa31f814f2d67113cab9c
Author: imoseyon <imoseyon@gmail.com>
Date:   Sat Nov 29 00:32:19 2014 -0800

    cpufreq: force cpuN policy to match cpu0 when setting min freq
    
    * I omitted this on purpose before on N3 but no need to do that
    for shamu
    
    (cherry picked from commit b1dfdd962586502663bdc652a7ce51efc6b2bec0)
    
    (cherry picked from commit b1dfdd962586502663bdc652a7ce51efc6b2bec0)

commit d72857329856d9b4e4bae981270544c8c5d22926
Author: Steve Kondik <shade@chemlab.org>
Date:   Sun Jan 18 22:31:36 2015 -0700

    msm: Fix high load average from uninterruptible waits
    
     * The load average on all MSMs is currently hovering at around 14
       due to uninterruptible waits in various places.
     * Convert these waits to interruptible waits to bring the load
       back down to zero at idle.
    
    Change-Id: I14bad4af135b1594e235e2252cb484cb34d91054
    
    Conflicts:
    
    	drivers/thermal/msm_thermal.c
    
    Conflicts:
    	drivers/thermal/msm_thermal.c
    
    (cherry picked from commit fd023ead7a158b3e699c1eba426787a6ab258532)
    
    Conflicts:
    	drivers/video/msm/mdss/mdss_fb.c
    
    (cherry picked from commit 15ca5b7b79f2deab2db7f9288ebf7b17ef4553c6)
    
    (cherry picked from commit 15ca5b7b79f2deab2db7f9288ebf7b17ef4553c6)

commit cdcb4e36123c2b84c656a31c845f04a16e4d4701
Author: Xiaoming Zhou <zhoux@codeaurora.org>
Date:   Thu Feb 20 16:00:53 2014 -0500

    msm: mdss: properly handle panel on and off
    
    There is some condition that panel off will be called multiple times.
    In this case, it was blindly free the gpios that were already released.
    This is adding the check to handle this condition.
    
    Change-Id: I0140872be1255fe00ed5abd164a246fa57b2a245
    Signed-off-by: Xiaoming Zhou <zhoux@codeaurora.org>
    
    (cherry picked from commit afd48062c3382066ec76c090f2420a10806a36f7)
    
    (cherry picked from commit afd48062c3382066ec76c090f2420a10806a36f7)
    
    (cherry picked from commit 2e22bb9b268f5b43c9e83969bb751d9adbcf8949)
    
    (cherry picked from commit 2e22bb9b268f5b43c9e83969bb751d9adbcf8949)

commit 7d01a41cfe41e51d38e1965c03f44a47c740a18b
Author: imoseyon <imoseyon@gmail.com>
Date:   Sun Nov 30 09:01:11 2014 -0800

    fs: sync: Asynchronous Fsync from HTC
    
        * taken from Faux's S5 repo and modified/fixed-up
          for Linux 3.10 and shamu
    
    (cherry picked from commit a5e37a022d0c8b3b3dc54898d640aa3587a46956)
    
    (cherry picked from commit a5e37a022d0c8b3b3dc54898d640aa3587a46956)

commit 74c18d56b2c9a93baf79bf62429d18f07c1eabb5
Author: yank555-lu <yank555.lu@gmail.com>
Date:   Sat Dec 27 17:46:10 2014 +0100

    block: fiops ioscheduler - squashed commit (all credits for forward port to faux123)
    
    block: fiops ioscheduler core
    
    FIOPS (Fair IOPS) ioscheduler is IOPS based ioscheduler, so only targets
    for drive without I/O seek. It's quite similar like CFQ, but the dispatch
    decision is made according to IOPS instead of slice.
    
    The algorithm is simple. Drive has a service tree, and each task lives in
    the tree. The key into the tree is called vios (virtual I/O). Every request
    has vios, which is calculated according to its ioprio, request size and so
    on. Task's vios is the sum of vios of all requests it dispatches. FIOPS
    always selects task with minimum vios in the service tree and let the task
    dispatch request. The dispatched request's vios is then added to the task's
    vios and the task is repositioned in the sevice tree.
    
    Unlike CFQ, FIOPS doesn't have separate sync/async queues, because with I/O
    less writeback, usually a task can only dispatch either sync or async requests.
    Bias read or write request can still be done with read/write scale.
    
    One issue is if workload iodepth is lower than drive queue_depth, IOPS
    share of a task might not be strictly according to its priority, request
    Bias read or write request can still be done with read/write scale.
    
    One issue is if workload iodepth is lower than drive queue_depth, IOPS
    share of a task might not be strictly according to its priority, request
    size and so on. In this case, the drive is in idle actually. Solving the
    problem need make drive idle, so impact performance. I believe CFQ isn't
    completely fair between tasks in such case too.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	block/Makefile
    
    Conflicts:
    	block/Makefile
    block: fiops read/write request scale
    
    read/write speed of Flash based storage usually is different. For example,
    in my SSD maxium thoughput of read is about 3 times faster than that of
    write. Add a scale to differenate read and write. Also add a tunable, so
    user can assign different scale for read and write.
    
    By default, the scale is 1:1, which means the scale is a noop.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    block: fiops sync/async scale
    
    CFQ gives 2.5 times more share to sync workload. This matches CFQ.
    
    Note this is different with the read/write scale. We have 3 types of
    requests:
    1. read
    2. sync write
    3. write
    CFQ doesn't differentitate type 1 and 2, but request cost of 1 and 2
    are usually different for flash based storage. So we have both sync/async
    and read/write scale here.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    block: fiops add ioprio support
    
    Add CFQ-like ioprio support. Priority A will get 20% more share than priority
    A+1, which matches CFQ.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    block: fiops preserve vios key for deep queue depth workload
    
    If the task has running request, even it's added into service tree newly,
    we preserve its vios key, so it will not lost its share. This should work
    for task driving big queue depth. For single depth task, there is no approach
    to preserve its vios key.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    block: fiops bias sync workload
    
    If there are async requests running, delay async workload. Otherwise
    async workload (usually very deep iodepth) will use all queue iodepth
    and later sync requests will get long delayed. The idea is from CFQ.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    block: fiops add some trace information
    
    Add some trace information, which is helpful when I do debugging.
    
    Signed-off-by: Shaohua Li <shaohua.li@intel.com>
    FIOPS: forward port for use on 3.10 Linux
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 2479eb11027045068b4e63276e5d32f52ccee3b7
Author: yank555-lu <yank555.lu@gmail.com>
Date:   Sun Feb 2 21:28:59 2014 +0100

    binfmt_elf.c: use get_random_int() to fix entropy depleting (Jeff Liu )
    
    See http://lkml.indiana.edu/hypermail/linux/kernel/1211.1/03767.html for details.

commit 45c0b1f0616ce7102cb5fb42b2aa0ad474d29c78
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Feb 25 22:38:31 2015 -0700

    Force Fast Charge v1.2 [Yank555.lu]

commit 89be94925aa89af547e6ec6108380f8d526d93cf
Author: friedrich420 <kelpidorou@yahoo.com>
Date:   Wed Jan 7 16:34:42 2015 +0200

    network speed tweak [ch33kybutt]

commit b42842da14dcdedafcd0bbaec5117c4a8ce70a49
Author: friedrich420 <kelpidorou@yahoo.com>
Date:   Wed Nov 5 20:11:18 2014 +0200

    Stereo Call Recording Support

commit a2f8dd8f1d65d6f5f01088464e56310cff646ff1
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Sat Jan 3 17:47:31 2015 +0100

    cpufreq: cpu-boost: don't boost migrations with load below the threshold
    Even if we don't use load_based_syncs (there seems to be a bug that make
    min_freq stuck at random frequencies) we can prevent this feature
    to boost the target cpu if the task load is below the migration
    threshold. We might save some mA down the road with this.
    
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>
    
    (cherry picked from commit 917c9a8b2372d65f26955c8e98952246aa037a78)
    
    (cherry picked from commit 8080f25a966ef01364241edd9ab300acfb9cb177)
    
    (cherry picked from commit 8080f25a966ef01364241edd9ab300acfb9cb177)
    
    (cherry picked from commit 448b5385b176f1a793f8c2a02b294b1a898afebc)
    
    (cherry picked from commit 448b5385b176f1a793f8c2a02b294b1a898afebc)
    
    (cherry picked from commit 45252a3466be83108ded0981a6ab2a0f45e396c4)
    
    (cherry picked from commit 45252a3466be83108ded0981a6ab2a0f45e396c4)

commit f49215a9c7cbf2fc86a16f42be62fbd08011caf7
Author: Jane Li <jiel@marvell.com>
Date:   Fri Jan 3 17:17:41 2014 +0800

    cpufreq: Fix timer/workqueue corruption by protecting reading governor_enabled
    
    When a CPU is hot removed we'll cancel all the delayed work items via
    gov_cancel_work(). Sometimes the delayed work function determines that
    it should adjust the delay for all other CPUs that the policy is
    managing. If this scenario occurs, the canceling CPU will cancel its own
    work but queue up the other CPUs works to run.
    
    Commit 3617f2 (cpufreq: Fix timer/workqueue corruption due to double
    queueing) has tried to fix this, but reading governor_enabled is not
    protected by cpufreq_governor_lock. Even though od_dbs_timer() checks
    governor_enabled before gov_queue_work(), this scenario may occur. For
    example:
    
     CPU0                                        CPU1
     ----                                        ----
     cpu_down()
      ...                                        <work runs>
      __cpufreq_remove_dev()                     od_dbs_timer()
       __cpufreq_governor()                       policy->governor_enabled
        policy->governor_enabled = false;
        cpufreq_governor_dbs()
         case CPUFREQ_GOV_STOP:
          gov_cancel_work(dbs_data, policy);
           cpu0 work is canceled
            timer is canceled
            cpu1 work is canceled
            <waits for cpu1>
                                                  gov_queue_work(*, *, true);
                                                   cpu0 work queued
                                                   cpu1 work queued
                                                   cpu2 work queued
                                                   ...
            cpu1 work is canceled
            cpu2 work is canceled
            ...
    
    At the end of the GOV_STOP case cpu0 still has a work queued to
    run although the code is expecting all of the works to be
    canceled. __cpufreq_remove_dev() will then proceed to
    re-initialize all the other CPUs works except for the CPU that is
    going down. The CPUFREQ_GOV_START case in cpufreq_governor_dbs()
    will trample over the queued work and debugobjects will spit out
    a warning:
    
    WARNING: at lib/debugobjects.c:260 debug_print_object+0x94/0xbc()
    ODEBUG: init active (active state 0) object type: timer_list hint: delayed_work_timer_fn+0x0/0x14
    Modules linked in:
    CPU: 1 PID: 1205 Comm: sh Tainted: G        W    3.10.0 #200
    [<c01144f0>] (unwind_backtrace+0x0/0xf8) from [<c0111d98>] (show_stack+0x10/0x14)
    [<c0111d98>] (show_stack+0x10/0x14) from [<c01272cc>] (warn_slowpath_common+0x4c/0x68)
    [<c01272cc>] (warn_slowpath_common+0x4c/0x68) from [<c012737c>] (warn_slowpath_fmt+0x30/0x40)
    [<c012737c>] (warn_slowpath_fmt+0x30/0x40) from [<c034c640>] (debug_print_object+0x94/0xbc)
    [<c034c640>] (debug_print_object+0x94/0xbc) from [<c034c7f8>] (__debug_object_init+0xc8/0x3c0)
    [<c034c7f8>] (__debug_object_init+0xc8/0x3c0) from [<c01360e0>] (init_timer_key+0x20/0x104)
    [<c01360e0>] (init_timer_key+0x20/0x104) from [<c04872ac>] (cpufreq_governor_dbs+0x1dc/0x68c)
    [<c04872ac>] (cpufreq_governor_dbs+0x1dc/0x68c) from [<c04833a8>] (__cpufreq_governor+0x80/0x1b0)
    [<c04833a8>] (__cpufreq_governor+0x80/0x1b0) from [<c0483704>] (__cpufreq_remove_dev.isra.12+0x22c/0x380)
    [<c0483704>] (__cpufreq_remove_dev.isra.12+0x22c/0x380) from [<c0692f38>] (cpufreq_cpu_callback+0x48/0x5c)
    [<c0692f38>] (cpufreq_cpu_callback+0x48/0x5c) from [<c014fb40>] (notifier_call_chain+0x44/0x84)
    [<c014fb40>] (notifier_call_chain+0x44/0x84) from [<c012ae44>] (__cpu_notify+0x2c/0x48)
    [<c012ae44>] (__cpu_notify+0x2c/0x48) from [<c068dd40>] (_cpu_down+0x80/0x258)
    [<c068dd40>] (_cpu_down+0x80/0x258) from [<c068df40>] (cpu_down+0x28/0x3c)
    [<c068df40>] (cpu_down+0x28/0x3c) from [<c068e4c0>] (store_online+0x30/0x74)
    [<c068e4c0>] (store_online+0x30/0x74) from [<c03a7308>] (dev_attr_store+0x18/0x24)
    [<c03a7308>] (dev_attr_store+0x18/0x24) from [<c0256fe0>] (sysfs_write_file+0x100/0x180)
    [<c0256fe0>] (sysfs_write_file+0x100/0x180) from [<c01fec9c>] (vfs_write+0xbc/0x184)
    [<c01fec9c>] (vfs_write+0xbc/0x184) from [<c01ff034>] (SyS_write+0x40/0x68)
    [<c01ff034>] (SyS_write+0x40/0x68) from [<c010e200>] (ret_fast_syscall+0x0/0x48)
    
    In gov_queue_work(), lock cpufreq_governor_lock before gov_queue_work,
    and unlock it after __gov_queue_work(). In this way, governor_enabled
    is guaranteed not changed in gov_queue_work().
    
    Signed-off-by: Jane Li <jiel@marvell.com>
    Acked-by: Viresh Kumar <viresh.kumar@linaro.org>
    Reviewed-by: Dmitry Torokhov <dmitry.torokhov@gmail.com>
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
    Signed-off-by: flar2 <asegaert@gmail.com>
    
    (cherry picked from commit 97dfaaff13b0c3fa6145e75ccd9ef7c8ce431004)
    
    (cherry picked from commit 97dfaaff13b0c3fa6145e75ccd9ef7c8ce431004)

commit 5ba3e2a49b2d9be3932ab4b916baf6b6e21536aa
Author: Bibek Basu <bbasu@nvidia.com>
Date:   Mon May 19 10:24:01 2014 +0530

    cpufreq: remove race while accessing cur_policy
    
    While accessing cur_policy during executing events
    CPUFREQ_GOV_START, CPUFREQ_GOV_STOP, CPUFREQ_GOV_LIMITS,
    same mutex lock is not taken, dbs_data->mutex, which leads
    to race and data corruption while running continious suspend
    resume test. This is seen with ondemand governor with suspend
    resume test using rtcwake.
    
     Unable to handle kernel NULL pointer dereference at virtual address 00000028
     pgd = ed610000
     [00000028] *pgd=adf11831, *pte=00000000, *ppte=00000000
     Internal error: Oops: 17 [#1] PREEMPT SMP ARM
     Modules linked in: nvhost_vi
     CPU: 1 PID: 3243 Comm: rtcwake Not tainted 3.10.24-gf5cf9e5 #1
     task: ee708040 ti: ed61c000 task.ti: ed61c000
     PC is at cpufreq_governor_dbs+0x400/0x634
     LR is at cpufreq_governor_dbs+0x3f8/0x634
     pc : [<c05652b8>] lr : [<c05652b0>] psr: 600f0013
     sp : ed61dcb0 ip : 000493e0 fp : c1cc14f0
     r10: 00000000 r9 : 00000000 r8 : 00000000
     r7 : eb725280 r6 : c1cc1560 r5 : eb575200 r4 : ebad7740
     r3 : ee708040 r2 : ed61dca8 r1 : 001ebd24 r0 : 00000000
     Flags: nZCv IRQs on FIQs on Mode SVC_32 ISA ARM Segment user
     Control: 10c5387d Table: ad61006a DAC: 00000015
     [<c05652b8>] (cpufreq_governor_dbs+0x400/0x634) from [<c055f700>] (__cpufreq_governor+0x98/0x1b4)
     [<c055f700>] (__cpufreq_governor+0x98/0x1b4) from [<c0560770>] (__cpufreq_set_policy+0x250/0x320)
     [<c0560770>] (__cpufreq_set_policy+0x250/0x320) from [<c0561dcc>] (cpufreq_update_policy+0xcc/0x168)
     [<c0561dcc>] (cpufreq_update_policy+0xcc/0x168) from [<c0561ed0>] (cpu_freq_notify+0x68/0xdc)
     [<c0561ed0>] (cpu_freq_notify+0x68/0xdc) from [<c008eff8>] (notifier_call_chain+0x4c/0x8c)
     [<c008eff8>] (notifier_call_chain+0x4c/0x8c) from [<c008f3d4>] (__blocking_notifier_call_chain+0x50/0x68)
     [<c008f3d4>] (__blocking_notifier_call_chain+0x50/0x68) from [<c008f40c>] (blocking_notifier_call_chain+0x20/0x28)
     [<c008f40c>] (blocking_notifier_call_chain+0x20/0x28) from [<c00aac6c>] (pm_qos_update_bounded_target+0xd8/0x310)
     [<c00aac6c>] (pm_qos_update_bounded_target+0xd8/0x310) from [<c00ab3b0>] (__pm_qos_update_request+0x64/0x70)
     [<c00ab3b0>] (__pm_qos_update_request+0x64/0x70) from [<c004b4b8>] (tegra_pm_notify+0x114/0x134)
     [<c004b4b8>] (tegra_pm_notify+0x114/0x134) from [<c008eff8>] (notifier_call_chain+0x4c/0x8c)
     [<c008eff8>] (notifier_call_chain+0x4c/0x8c) from [<c008f3d4>] (__blocking_notifier_call_chain+0x50/0x68)
     [<c008f3d4>] (__blocking_notifier_call_chain+0x50/0x68) from [<c008f40c>] (blocking_notifier_call_chain+0x20/0x28)
     [<c008f40c>] (blocking_notifier_call_chain+0x20/0x28) from [<c00ac228>] (pm_notifier_call_chain+0x1c/0x34)
     [<c00ac228>] (pm_notifier_call_chain+0x1c/0x34) from [<c00ad38c>] (enter_state+0xec/0x128)
     [<c00ad38c>] (enter_state+0xec/0x128) from [<c00ad400>] (pm_suspend+0x38/0xa4)
     [<c00ad400>] (pm_suspend+0x38/0xa4) from [<c00ac114>] (state_store+0x70/0xc0)
     [<c00ac114>] (state_store+0x70/0xc0) from [<c027b1e8>] (kobj_attr_store+0x14/0x20)
     [<c027b1e8>] (kobj_attr_store+0x14/0x20) from [<c019cd9c>] (sysfs_write_file+0x104/0x184)
     [<c019cd9c>] (sysfs_write_file+0x104/0x184) from [<c0143038>] (vfs_write+0xd0/0x19c)
     [<c0143038>] (vfs_write+0xd0/0x19c) from [<c0143414>] (SyS_write+0x4c/0x78)
     [<c0143414>] (SyS_write+0x4c/0x78) from [<c000f080>] (ret_fast_syscall+0x0/0x30)
     Code: e1a00006 eb084346 e59b0020 e5951024 (e5903028)
     ---[ end trace 0488523c8f6b0f9d ]---
    
    Signed-off-by: Bibek Basu <bbasu@nvidia.com>
    Acked-by: Viresh Kumar <viresh.kumar@linaro.org>
    Cc: 3.11+ <stable@vger.kernel.org> # 3.11+
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
    Signed-off-by: flar2 <asegaert@gmail.com>
    
    (cherry picked from commit 88c348e3ebbedaed7db3122dc545f7bc327c65ca)
    
    (cherry picked from commit 88c348e3ebbedaed7db3122dc545f7bc327c65ca)

commit c38f7fa51d4fb7c8523031e88946c161c2a57deb
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:42:37 2015 -0700

    Intelliplug on by default

commit 9227acece356efda6d90c66864f82d6f9c167005
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:43:41 2015 -0700

    Enable last_kmsg and increase log buffer shift plus add pr_alert when last_kmsg is not initialized
    and add shit load of tcp congestion control options & enabled f2fs

commit 96e2e75989126961cc15c61e2b0887a8be104167
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Fri Dec 5 17:51:32 2014 -0500

    mdss: implement panel color control
    
    Adapted and modified work by CM-10.2, morfic and ktoonsez
    
    Creates a syfs interface here:
    /sys/class/lcd/panel/panel_colors
    
    Will accept 0-4 for parameters:
    0 - Cold (more blues)
    1 - Cool
    2 - Normal (stock colors)
    3 - Warm
    4 - Hot (more reds)
    
    (cherry picked from commit e3548519c119be79073ac0de24a4fdaee7167f9b)
    
    (cherry picked from commit 129ff66abd0b42df54343395d1ed92e0ff2e0e86)
    
    (cherry picked from commit 129ff66abd0b42df54343395d1ed92e0ff2e0e86)
    
    (cherry picked from commit 8a03cf1aa5ade58782e80047a349fa9587ea8fed)
    
    (cherry picked from commit 8a03cf1aa5ade58782e80047a349fa9587ea8fed)

commit 53a4e10f39d8522c0d0f1ce1a8ce3d5901f7bb3c
Author: ktoonsez <ktoonsez@gmail.com>
Date:   Thu Nov 13 21:16:30 2014 -0700

    Add variant detection
    
    (cherry picked from commit 25bac2231ca23bbe9348e2386e0c54be06380889)
    
    (cherry picked from commit e33bbc0bd875d4d70e178b1949777458635f973e)
    
    (cherry picked from commit e33bbc0bd875d4d70e178b1949777458635f973e)
    
    (cherry picked from commit 6f8b4fc3e15b20e48667f9e7ecc8e580e5e87f0d)
    
    (cherry picked from commit 6f8b4fc3e15b20e48667f9e7ecc8e580e5e87f0d)

commit 8f7b4455f33b806c4e8102129a37cc5038c32ffb
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 23:54:27 2015 -0700

    Revert: Sound Control: initial bring up for Nexus 6 Linux 3.10 kernel driver (faux123)
    
    Initial import of FauxSound Driver 3.6 from 3.4 linux kernel drivers tailored
    for Nexus 6
    
    GPL Copyright 2014 Paul Reioux (Faux123)
    
    Signed-off-by: Paul Reioux <reioux@gmail.com> (reverted from commit 33e1385e31476fca6fe3fd5cba64aabdbbd30644)

commit d8c484033e2582948afc40c9c656ac9c3370cf79
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 23:59:09 2015 -0700

    sound/soc/codecs: Faux Sound control for WCD9330 TomTom codec driver
    
    First implementation:
    Faux Sound control adapted for the wcd9330 driver.
    Thanks for the tip to thehacker911.
    
    Signed-off-by: Pafcholini <pafcholini@gmail.com>

commit 78e72c386fdb3ac3d725dd915495b4a23b8cf3d9
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Fri Jan 23 14:34:23 2015 +0100

    sound/soc/codecs: fix speaker gain and mic gain for the Note 4
    
    Signed-off-by: Pafcholini <pafcholini@gmail.com>
    
    (cherry picked from commit 7f960e42a8123dfff411cef304a8c9c8a4080cb5)
    
    (cherry picked from commit 7f960e42a8123dfff411cef304a8c9c8a4080cb5)
    
    (cherry picked from commit f45e483773df9ac8a55975c9565a234a2a46616b)
    
    (cherry picked from commit f45e483773df9ac8a55975c9565a234a2a46616b)
    
    (cherry picked from commit 56dfe7d232ec44252cb7b898b3c8c7c23428080a)
    
    (cherry picked from commit 56dfe7d232ec44252cb7b898b3c8c7c23428080a)

commit ccd6acb2965f7ea572f1cf4da699c02fa1431e8f
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Sat Jan 24 03:30:24 2015 +0100

    sound/soc/codecs: add sound_control_locked
    
    (cherry picked from commit 8b9cb07f8d10c470c50ca396ba207e9ee17cb96c)
    
    (cherry picked from commit 8b9cb07f8d10c470c50ca396ba207e9ee17cb96c)
    
    (cherry picked from commit a7f0a16fdc5ef66f156c99e5aaa29c44c6ac15dc)
    
    (cherry picked from commit a7f0a16fdc5ef66f156c99e5aaa29c44c6ac15dc)
    
    (cherry picked from commit 469a98b8a09325ecaa4ee6632f666e57a82fc349)
    
    (cherry picked from commit 469a98b8a09325ecaa4ee6632f666e57a82fc349)

commit d7120174e32d3fa01006f9644ed521fb16492b06
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Thu Jan 29 14:27:51 2015 +0100

    Sound Control: 3.6
    
    fix some issues and bump version to 3.6
    
    Signed-off-by: Pafcholini <pafcholini@gmail.com>
    
    (cherry picked from commit 644ce4a6271dc263ad380d683e1b933051f06592)
    
    (cherry picked from commit 644ce4a6271dc263ad380d683e1b933051f06592)
    
    (cherry picked from commit fe93a48dde4b21f23c46335a38060191de477d6d)
    
    (cherry picked from commit fe93a48dde4b21f23c46335a38060191de477d6d)

commit 488936f122262a19f81298cf8443948fb2890cc9
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Fri Jan 30 01:42:20 2015 +0100

    sound/soc/codecs: add TOMTOM_A_CDC_RX8
    
    (cherry picked from commit 6e9fd1e0c537e2691ea27a99b9e5cc6ac97423a5)
    
    (cherry picked from commit 6e9fd1e0c537e2691ea27a99b9e5cc6ac97423a5)
    
    (cherry picked from commit d0b76130109032afb2a24f39c55f2d4ae096590d)
    
    (cherry picked from commit d0b76130109032afb2a24f39c55f2d4ae096590d)

commit 79e36cd5369c422326cbfa8bfc6417517c14a8cf
Author: Paul Reioux <reioux@gmail.com>
Date:   Sat Dec 6 03:20:50 2014 -0600

    intelli_plug: add performance boost option
    
    also fixed dependency on __cpuinit
    
    bumped to version 3.9
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit e486a2d654394125f8f22c28b45da8870b536a44
Author: Paul Reioux <reioux@gmail.com>
Date:   Sat Dec 6 03:21:52 2014 -0600

    dm-crypt: add intelli_plug performance boost optimization
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit a419aa4c4085ec81a0a9a08575127c73ec033ca0
Author: Paul Reioux <reioux@gmail.com>
Date:   Sat Dec 6 19:41:35 2014 -0600

    dm-crypt: use 2x number of write threads to saturate each cpus pipeline
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 3f179f162b2bfae980d326b6672c74592dd3d467
Author: Paul Reioux <reioux@gmail.com>
Date:   Mon Mar 9 03:43:40 2015 -0500

    android: binder: use GPF_HIGHUSER flag since binder is designed for userspace
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 7a8f364642aa85d679f8044cc0eea810919f2d63
Author: faux123 <reioux@gmail.com>
Date:   Wed Mar 11 00:11:17 2015 -0700

    intelli_plug: add perf_boost sysfs entry and clean up permissions
    
    add new automatic calculations for ARM64 and APQ8084 processor types
    
    also bump to version 4.0
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	arch/arm/hotplug/intelli_plug.c

commit 7714091f35acce6697f5dd0470cc10993986b2aa
Author: flar2 <asegaert@gmail.com>
Date:   Tue Dec 2 16:41:08 2014 -0500

    GPU: start at 240MHz
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 564caaaa8c213fc6fdf49483dd5c115db93b733c
Author: flar2 <asegaert@gmail.com>
Date:   Tue Dec 2 17:15:57 2014 -0500

    Lower GPU voltage constraint
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 857bfd9c28c932c577f540d7d2c5e55803d17e22
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:39:31 2014 -0600

    sched: add a new arch_sd_local_flags for sched_domain init
    
    Date	Fri, 18 Oct 2013 13:52:15 +0200
    
    The function arch_sd_local_flags is used to set flags in sched_domains
    according to the platform architecture. A new flag SD_SHARE_POWERDOMAIN is
    also created to reflect whether groups of CPUs in a sched_domain level can or
    not reach different power state. As an example, the flag should be cleared at
    CPU level if groups of cores can be power gated independently. This information
    is used to decide if it's worth packing some tasks in a group of CPUs in order
    to power gate the other groups instead of spreading the tasks. The default
    behavior of the scheduler is to spread tasks across CPUs and groups of CPUs so
    the flag is set into all sched_domains.
    
    The cpu parameter of arch_sd_local_flags can be used by architecture to fine
    tune the scheduler domain flags. As an example SD_SHARE_POWERDOMAIN flag can be
    set differently for groups of CPUs according to DT information
    
    Signed-off-by: Vincent Guittot <vincent.guittot at linaro.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit b2edf2527168411ec67b2f6605c22c2fb5afd8da
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:41:21 2014 -0600

    ARM: sched: clear SD_SHARE_POWERDOMAIN
    
    Fri Oct 18 07:54:53 EDT 2013
    
    The ARM platforms take advantage of packing tasks on few cores if the latters
    can be powergated independantly. We use DT and the cpu topology descirption
    to define at which level a core can be independantly powergated to the others
    and the SD_SHARE_POWERDOMAIN will be set accordingly at MC and CPU sched_domain
    level.
    
    The power-gate properties should be added with the value 1 in cpu and cluster
    node when then can power gate independantly from the other.
    
    As an example of a quad cores system which can power gate each core
    independantly, we should have a DT similar to the example below
    
    	cpus {
    		#address-cells = <1>;
    		#size-cells = <0>;
    
    	       cpu-map {
    	               cluster0 {
    				power-gate = <1>;
    				core0 {
    	                               cpu = <&cpu0>;
    					power-gate = <1>;
    				};
    				core1 {
    				        cpu = <&cpu1>;
    					power-gate = <1>;
    				};
    				core2 {
    					cpu = <&cpu2>;
    					power-gate = <1>;
    				};
    				core3 {
    					cpu = <&cpu3>;
    					power-gate = <1>;
    				};
    			};
    		};
    
    	...
    
    	};
    
    Signed-off-by: Vincent Guittot <vincent.guittot at linaro.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 3383f0abdc38fade8ce2e92c90e0ca977d03cc2e
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:42:45 2014 -0600

    sched: define pack buddy CPUs
    
    Date	Fri, 18 Oct 2013 13:52:16 +0200
    
    During the creation of sched_domain, we define a pack buddy CPU for each CPU
    when one is available. We want to pack at all levels where a group of CPUs can
    be power gated independently from others.
    On a system that can't power gate a group of CPUs independently, the flag is
    set at all sched_domain level and the buddy is set to -1. This is the default
    behavior for all architectures.
    
    On a dual clusters / dual cores system which can power gate each core and
    cluster independently, the buddy configuration will be :
    
          | Cluster 0   | Cluster 1   |
          | CPU0 | CPU1 | CPU2 | CPU3 |
    -----------------------------------
    buddy | CPU0 | CPU0 | CPU0 | CPU2 |
    
    If the cores in a cluster can't be power gated independently, the buddy
    configuration becomes:
    
          | Cluster 0   | Cluster 1   |
          | CPU0 | CPU1 | CPU2 | CPU3 |
    -----------------------------------
    buddy | CPU0 | CPU1 | CPU0 | CPU0 |
    
    Signed-off-by: Vincent Guittot <vincent.guittot at linaro.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 3471c5ee4d59c1ed9bc23cda7e6c6f3bec56557a
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:43:43 2014 -0600

    sched: do load balance only with packing cpus
    
    Date	Fri, 18 Oct 2013 13:52:17 +0200
    
    The tasks will be scheduled only on the CPUs that participate to the packing
    effort. A CPU participates to the packing effort when it is its own buddy.
    
    For ILB, look for an idle CPU close to the packing CPUs whenever possible.
    The goal is to prevent the wake up of a CPU which doesn't share the power
    domain of the pack buddy CPU.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 0253425be135d79428666b29d24c01f3c9dcd8f9
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:45:15 2014 -0600

    sched: add a packing level knob
    
    Date	Fri, 18 Oct 2013 13:52:18 +0200
    
    The knob is used to set an average load threshold that will be used to trig
    the inclusion/removal of CPUs in the packing effort list.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	kernel/sysctl.c

commit 50f0cf44b68f5b6b051969f7d3accb46c539c751
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:46:18 2014 -0600

    sched: create a new field with available capacity
    
    Date	Fri, 18 Oct 2013 13:52:19 +0200
    
    This new field power_available reflects the available capacity of a CPU
    unlike the cpu_power which reflects the current capacity.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit fcbb4f251c5cecbd4b49e56832c45f335832c500
Author: Paul Reioux <reioux@gmail.com>
Date:   Wed Nov 19 20:54:47 2014 -0600

    sched: get CPU's activity statistic
    
    Date	Fri, 18 Oct 2013 13:52:20 +0200
    
    Monitor the activity level of each group of each sched_domain level. The
    activity is the amount of cpu_power that is currently used on a CPU. We use
    the runnable_avg_sum and _period to evaluate this activity level. In the
    special use case where the CPU is fully loaded by more than 1 task, the
    activity level is set above the cpu_power in order to reflect the overload of
    The cpu
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    backported to Linux 3.10
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 9923c6c0933933c03751d2287adc11d6290c115d
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 20:55:54 2014 -0600

    sched: move load idx selection in find_idlest_group
    
    Date	Fri, 18 Oct 2013 13:52:21 +0200
    
    load_idx is used in find_idlest_group but initialized in select_task_rq_fair
    even when not used. The load_idx initialisation is moved in find_idlest_group
    and the sd_flag replaces it in the function's args.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit edf28fefdaad91093fd268f2a4b47a273d7a4c18
Author: Joonsoo Kim <iamjoonsoo.kim@lge.com>
Date:   Tue Aug 6 17:36:42 2013 +0900

    sched: Factor out code to should_we_balance()
    
    Now checking whether this cpu is appropriate to balance or not
    is embedded into update_sg_lb_stats() and this checking has no direct
    relationship to this function. There is not enough reason to place
    this checking at update_sg_lb_stats(), except saving one iteration
    for sched_group_cpus.
    
    In this patch, I factor out this checking to should_we_balance() function.
    And before doing actual work for load_balancing, check whether this cpu is
    appropriate to balance via should_we_balance(). If this cpu is not
    a candidate for balancing, it quit the work immediately.
    
    With this change, we can save two memset cost and can expect better
    compiler optimization.
    
    Below is result of this patch.
    
     * Vanilla *
       text	   data	    bss	    dec	    hex	filename
      34499	   1136	    116	  35751	   8ba7	kernel/sched/fair.o
    
     * Patched *
       text	   data	    bss	    dec	    hex	filename
      34243	   1136	    116	  35495	   8aa7	kernel/sched/fair.o
    
    In addition, rename @balance to @continue_balancing in order to represent
    its purpose more clearly.
    
    Signed-off-by: Joonsoo Kim <iamjoonsoo.kim@lge.com>
    [ s/should_balance/continue_balancing/g ]
    Reviewed-by: Paul Turner <pjt@google.com>
    [ Made style changes and a fix in should_we_balance(). ]
    Signed-off-by: Peter Zijlstra <peterz@infradead.org>
    Link: http://lkml.kernel.org/r/1375778203-31343-3-git-send-email-iamjoonsoo.kim@lge.com
    Signed-off-by: Ingo Molnar <mingo@kernel.org>

commit 40f758095e92dc39890a37ef6b9ee7295f11abf9
Author: Joonsoo Kim <iamjoonsoo.kim@lge.com>
Date:   Tue Sep 10 15:54:49 2013 +0900

    sched: Fix load balancing performance regression in should_we_balance()
    
    Commit 23f0d20 ("sched: Factor out code to should_we_balance()")
    introduces the should_we_balance() function.  This function should
    return 1 if this cpu is appropriate for balancing. But the newly
    introduced code doesn't do so, it returns 0 instead of 1.
    
    This introduces performance regression, reported by Dave Chinner:
    
                            v4 filesystem           v5 filesystem
    3.11+xfsdev:            220k files/s            225k files/s
    3.12-git                180k files/s            185k files/s
    3.12-git-revert         245k files/s            247k files/s
    
    You can find more detailed information at:
    
      https://lkml.org/lkml/2013/9/10/1
    
    This patch corrects the return value of should_we_balance()
    function as orignally intended.
    
    With this patch, Dave Chinner reports that the regression is gone:
    
                            v4 filesystem           v5 filesystem
    3.11+xfsdev:            220k files/s            225k files/s
    3.12-git                180k files/s            185k files/s
    3.12-git-revert         245k files/s            247k files/s
    3.12-git-fix            249k files/s            248k files/s
    
    Reported-by: Dave Chinner <dchinner@redhat.com>
    Tested-by: Dave Chinner <dchinner@redhat.com>
    Signed-off-by: Joonsoo Kim <iamjoonsoo.kim@lge.com>
    Cc: Paul Turner <pjt@google.com>
    Cc: Peter Zijlstra <peterz@infradead.org>
    Cc: Dave Chinner <david@fromorbit.com>
    Link: http://lkml.kernel.org/r/20130910065448.GA20368@lge.com
    Signed-off-by: Ingo Molnar <mingo@kernel.org>

commit aa9d863ee50b7c38b559ce9b3d3602d22808c9d8
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 21:08:36 2014 -0600

    sched: update the packing cpu list
    
    Date	Fri, 18 Oct 2013 13:52:22 +0200
    
    Use the activity statistics to update the list of CPUs that should be used
    to hanlde the current system activity.
    
    The cpu_power is updated for CPUs that don't participate to the packing
    effort. We consider that their cpu_power is allocated to idleness as it
    could be allocated by rt. So the cpu_power that remains available for cfs,
    is set to min value (i.e. 1).
    
    The cpu_power is used for a task that wakes up because a waking up task is
    already taken into account in the current activity whereas we use the
    power_available for a fork and exec because the task is not part of the current
    activity.
    
    In order to quickly found the packing starting point, we save information that
    will be used to directly start with the right sched_group at the right
    sched_domain level instead of running the complete update_packing_domain
    algorithm each time we need to use the packing cpu list.
    
    The sd_power_leader defines the leader of a group of CPU that can't be
    powergated independantly. As soon as this CPU is used, all the CPU in the same
    group will be used based on the fact that it doesn't worth to keep some cores
    idle if they can't be power gated while one core in the group is running.
    The sd_pack_group and sd_pack_domain are used to quickly check if a power
    leader should be used in the packing effort
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 981471b79ef78b6d952e3709fa93b3544c0f00f1
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 21:10:08 2014 -0600

    sched: init this_load to max in find_idlest_group
    
    Date	Fri, 18 Oct 2013 13:52:23 +0200
    
    Init this_load to max value instead of 0 in find_idlest_group.
    If the local group is skipped because it doesn't have allowed CPUs, this_load
    stays to 0,  no idlest group will be returned and the selected CPU will be a
    not allowed one (which will be replaced in select_fallback_rq by a random
    one). With a default value set to max, we will use the idlest group even if we
    skip the local_group.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 4a96fd4602970cf0a3feb1676a7f715b55c21a8e
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 21:10:58 2014 -0600

    sched: add a SCHED_PACKING_TASKS config
    
    Date	Fri, 18 Oct 2013 13:52:24 +0200
    
    The SCHED_PACKING_TASKS config is used to enable the packing tasks mecanism
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 3ccddd6ec42d18791291f7f705b14ead0c07d49c
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 21:11:53 2014 -0600

    sched: create a statistic structure
    
    Date	Fri, 18 Oct 2013 13:52:25 +0200
    
    Create a statistic structure that will be used to share information with
    other frameworks like cpuidle and cpufreq. This structure only contains the
    current wake up latency of a core for now but could be extended with other
    usefull information.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 2060f020f4dbb4f23187a61b815b891f4efe7aeb
Author: Paul Reioux <reioux@gmail.com>
Date:   Wed Nov 19 21:13:48 2014 -0600

    sched: differantiate idle cpu
    
    Date	Fri, 18 Oct 2013 13:52:26 +0200
    
    The cost for waking up of a core varies according to its current idle state.
    This includes C-state and intermediate state when some sync between cores is
    required to reach a deep C-state.
    Waking up a CPU in a deep C-state for running a short task is not efficient
    from both a power and a performance point of view. We should take into account
    the wake up latency of an idle CPU when the scheduler looks for the best CPU
    to use for a waking task.
    The wake up latency of a CPU is computed into a load that can be directly
    compared with task load and other CPUs load.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Backported to Linux 3.10
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit ff4690afce7551562fcc22630f3390a44e1e9e31
Author: Vincent Guittot <vincent.guittot@linaro.org>
Date:   Wed Nov 19 21:15:13 2014 -0600

    cpuidle: set the current wake up latency
    
    Date	Fri, 18 Oct 2013 13:52:27 +0200
    
    Save the current wake up latency of a core. This latency is not always
    the latency of a defined c-state but can also be an intermediate value
    when a core is ready to shutdown (timer migration, cache flush ...) but
    wait for the last core of the cluster to finalize the cluster power down.
    This latter use case is not manage by the current version of the patch because
    it implies that the cpuidle drivers set the wake up latency instead of the
    cpuidle core.
    
    Signed-off-by: Vincent Guittot <vincent.guittot@linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	drivers/cpuidle/cpuidle.c

commit 6fe9e47468bc68189f991308dcbfec92217489fc
Author: Paul Reioux <reioux@gmail.com>
Date:   Fri Nov 21 00:04:42 2014 -0600

    sched: fair: disable trace due to API update
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 3b4130b50cc7d897ee521f0b4280853093536ac7
Author: faux123 <reioux@gmail.com>
Date:   Mon Mar 19 17:22:43 2012 -0700

    Optimized ARM RWSEM algorithm
    
    RWSEM implementation for ARM using atomic functions.
    Heavily based on arch/sh/include/asm/rwsem.h
    
    Signed-off-by: Ashwin Chaugule <ashwinc@codeaurora.org>

commit 208131c1f2efb63bf0d44e308fad54748e2f5509
Author: Paul Reioux <reioux@gmail.com>
Date:   Mon Mar 24 21:57:01 2014 -0700

    page_alloc: Make watermarks tunable separately
    
    This patch introduces three new sysctls to /proc/sys/vm:
    wmark_min_kbytes, wmark_low_kbytes and wmark_high_kbytes.
    
    Each entry is used to compute watermark[min], watermark[low]
    and watermark[high] for each zone.
    
    These parameters are also updated when min_free_kbytes are
    changed because originally they are set based on min_free_kbytes.
    On the other hand, min_free_kbytes is updated when wmark_free_kbytes
    changes.
    
    By using the parameters one can adjust the difference among
    watermark[min], watermark[low] and watermark[high] and as a result
    one can tune the kernel reclaim behaviour to fit their requirement.
    
    Signed-off-by: Satoru Moriya <satoru.moriya@hds.com>
    
    modified and tuned for Hammerhead
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	kernel/sysctl.c
    	mm/page_alloc.c

commit a43f8856ea37c0191dea7ff50d0a7b6fdc0fc9cc
Author: Paul Reioux <reioux@gmail.com>
Date:   Sun Jun 15 17:34:18 2014 -0500

    sched/cpuidle: reduce IPI store. Backport upstream 3.16 scheduler updates
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	kernel/sched/core.c

commit 0a4ccc2d29bf7e722cd689e78f05824f4359f76a
Author: Alex Frid <afrid@nvidia.com>
Date:   Fri Dec 16 13:44:23 2011 -0800

    PM QoS: Add max online cpus as PM QoS parameter
    
    Bug 894200
    
    Change-Id: Ieb009a13c6ef9bca2388e234eb973d65a4e3a58b
    Signed-off-by: Alex Frid <afrid@nvidia.com>
    Reviewed-on: http://git-master/r/71034
    Reviewed-by: Rohan Somvanshi <rsomvanshi@nvidia.com>
    Tested-by: Rohan Somvanshi <rsomvanshi@nvidia.com>
    
    Rebase-Id: R5791d3cb0bb66f3b8079f5a8af5fa758fb3c6705

commit e873f2b110404267a2c221ae9e87d2b16d0befe9
Author: Antti P Miettinen <amiettinen@nvidia.com>
Date:   Tue Dec 27 12:28:21 2011 +0200

    PM QoS: Add CPU frequency min/max as PM QoS params
    
    Add minimum and maximum CPU frequency as PM QoS parameters.
    
    Bug 888312
    
    Change-Id: I18abddded35a044a6ad8365035e31d1a2213a329
    Reviewed-on: http://git-master/r/72206
    Signed-off-by: Antti P Miettinen <amiettinen@nvidia.com>
    Signed-off-by: Varun Wadekar <vwadekar@nvidia.com>
    Reviewed-on: http://git-master/r/75883
    Reviewed-by: Automatic_Commit_Validation_User
    
    Rebase-Id: R1007bbef60489ecc81a9acd0ce3b0abfa9a05f3e

commit 422681b38dcb480a22d19dd58f2dba28fa7f2008
Author: Gaurav Sarode <gsarode@nvidia.com>
Date:   Fri Feb 17 15:25:43 2012 +0530

    PM Qos: Add min online cpus as PM QoS parameter
    
    Bug 940061
    
    Change-Id: Ibae842fdc3af3c92ec7e6125c602417110d8b55e
    Signed-off-by: Gaurav Sarode <gsarode@nvidia.com>
    Reviewed-on: http://git-master/r/84521
    Reviewed-by: Sachin Nikam <snikam@nvidia.com>
    Tested-by: Aleksandr Frid <afrid@nvidia.com>
    Reviewed-by: Diwakar Tundlam <dtundlam@nvidia.com>
    
    Rebase-Id: R830d4e99f1e03b61a8c4e52e11645b7ed2f10f56

commit 8cb607cd7a4beedfe0bfcd5ec9dda74da2ab8b96
Author: Antti P Miettinen <amiettinen@nvidia.com>
Date:   Mon Aug 20 19:36:38 2012 +0300

    PM QoS: Add disable parameter
    
    For testing purposes it is useful to be able to disable
    PM Qos.
    
    Bug 1020898
    Bug 917572
    
    Reviewed-on: http://git-master/r/124667
    
    Change-Id: I266f5b5730cfe4705197d8b09db7f9eda6766c7c
    Signed-off-by: Antti P Miettinen <amiettinen@nvidia.com>
    Signed-off-by: Varun Wadekar <vwadekar@nvidia.com>
    
    Rebase-Id: Re2088674f90436e0b9dd74310d5cda1f9e2868e4

commit 16eca757a28837ade72c3352d00dfbab1a3d020a
Author: Li Li <lli5@nvidia.com>
Date:   Mon Jan 7 14:30:09 2013 -0800

    PM / QoS: export pm_qos_update_request_timeout()
    
    This pm_qos_update_request_timeout() was introduced without being exported.
    Should export it as all of the other PM QoS APIs so those drivers compiled as
    modules can use it.
    
    Change-Id: Ie51ce52db4ca633117fe18441c42b562220399e8
    Signed-off-by: Li Li <lli5@nvidia.com>
    Reviewed-on: http://git-master/r/189306
    Reviewed-by: Automatic_Commit_Validation_User
    GVS: Gerrit_Virtual_Submit
    Reviewed-by: Eric Miao <emiao@nvidia.com>
    Reviewed-by: Bharat Nihalani <bnihalani@nvidia.com>

commit 26ce41720150c1b67f55f6cc649c315b1e3e2c57
Author: Alex Frid <afrid@nvidia.com>
Date:   Mon Jul 22 21:26:11 2013 -0700

    PM QoS: Add GPU frequency limits to PM QoS
    
    Added GPU frequency min/max as PM QoS classes.
    
    Bug 1330780
    
    Change-Id: I2428c62748521c17e23b2df9ca409deda8b36160
    Signed-off-by: Alex Frid <afrid@nvidia.com>
    Reviewed-on: http://git-master/r/267702
    Reviewed-by: Ilan Aelion <iaelion@nvidia.com>
    Reviewed-by: Mitch Luban <mluban@nvidia.com>
    Reviewed-by: Yu-Huan Hsu <yhsu@nvidia.com>

commit d054ec132725f90edf4a539d544138f62234a827
Author: Sai Gurrappadi <sgurrappadi@nvidia.com>
Date:   Tue Oct 1 10:01:27 2013 -0700

    pmqos: Replace spinlock with mutex for pm_qos_lock
    
    Using a spinlock (taken with irqsave) meant that pm_qos_lock couldn't be
    used to synchronize on the notifiers in order to ensure proper order of
    the notifications. This is needed in case where there might be two near
    simultaneous pmqos client requests for a bound on the same constraint;
    the notifiers in pm_qos_update_target for the two clients could
    potentially engage in a race.
    
    Example:
    
    Assume two requests are made (A, B with A coming first) for max cpufreq
    and these are the only requests currently available.
    
    Current behavior can result in:
    
    notify(max_cpu_freq, minof(A, B))
    notify(max_cpu_freq, minof(LONG_MAX, A))
    
    Expected behavior:
    
    notify(max_cpu_freq, minof(LONG_MAX, A))
    notify(max_cpu_freq, minof(A, B))
    
    Most of the PM QoS and Dev PM QoS requester clients were reviewed and
    none of them were found to be calling pm_qos_add/update/remove request
    from interrupt or atomic context since those calls include the blocking
    notifier call which cannot be done in atomic context.
    
    Change-Id: I2fb43cc38da4c701e4872b937dd82cd38f1a1c1e
    Signed-off-by: Sai Gurrappadi <sgurrappadi@nvidia.com>
    Reviewed-on: http://git-master/r/299036
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Diwakar Tundlam <dtundlam@nvidia.com>

commit ad23e80b246e7903b1d84a0a0b113f7c82120c20
Author: Sai Gurrappadi <sgurrappadi@nvidia.com>
Date:   Tue Oct 1 10:37:35 2013 -0700

    power: PM QoS support for bounded constraints
    
    Extended PM QoS to allow binding of two constraints. Bounded constraints
    add the following functionality:
    
    	- Priority for min/max bound requests. Targets bounds are set
    	  to satisfy all priorities (intersection of all ranges). If it
    	  is not possible to do so, higher priorities prevail
    	- Timeouts for bound requests
    	- Userspace interface that exposes bound requests
    
    PM QoS still supports its original kernelspace and userspace interfaces
    
    Bug 1270839
    Bug 1349096
    
    Change-Id: Ic83444912b330fc71335d9a5b59077b1d16496bd
    Signed-off-by: Sai Gurrappadi <sgurrappadi@nvidia.com>
    Reviewed-on: http://git-master/r/299037
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Paul Walmsley <pwalmsley@nvidia.com>
    Reviewed-by: Diwakar Tundlam <dtundlam@nvidia.com>
    
    Conflicts:
    	kernel/power/qos.c

commit bdc436b5cb9fef6bc135d9dc60c2bdcf024e89ee
Author: Terje Bergstrom <tbergstrom@nvidia.com>
Date:   Wed Oct 9 15:21:42 2013 +0300

    PM / QoS: Add notifier for flags
    
    dev_pm_qos has a notifier for DEV_PM_QOS_LATENCY. Add a similar
    notifier for DEV_PM_QOS_FLAGS.
    
    Bug 1364240
    
    Change-Id: Ica4c58708855938818a1e75896503b9023b96573
    Signed-off-by: Terje Bergstrom <tbergstrom@nvidia.com>
    Reviewed-on: http://git-master/r/288810

commit df3a5922db6a85913c7cc5de5371f3e148b35637
Author: Sai Gurrappadi <sgurrappadi@nvidia.com>
Date:   Mon Oct 21 10:44:23 2013 -0700

    power: Prefer min over max for online cpus
    
    We prefered min_online_cpus over max_online_cpus if min > max.
    min_wins is now true for online cpu PmQoS requests.
    
    Bug 1270839
    
    Change-Id: I2888538dd1a4616babb7cd1532264272de5cfe64
    Signed-off-by: Sai Gurrappadi <sgurrappadi@nvidia.com>
    Reviewed-on: http://git-master/r/301871
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Diwakar Tundlam <dtundlam@nvidia.com>

commit 0a9943ba064b5960133a12166d47cd8385025747
Author: Sai Gurrappadi <sgurrappadi@nvidia.com>
Date:   Tue Jan 14 10:26:22 2014 -0800

    power: Fix coverity error
    
    Properly null-terminate userspace input string. Otherwise, the subsequent
    strsep() could continue off into arbitrary chunks of kmalloc() space
    that aren't part of the original string buffer.
    
    Change-Id: I3868dbcdd9df7e7172c001eb6bc41c605d48604b
    Signed-off-by: Sai Gurrappadi <sgurrappadi@nvidia.com>
    Reviewed-on: http://git-master/r/355578
    Reviewed-by: Paul Walmsley <pwalmsley@nvidia.com>
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Diwakar Tundlam <dtundlam@nvidia.com>

commit 0a83209f05eba84d83b2752623228799cb61ba5b
Author: Puneet Saxena <puneets@nvidia.com>
Date:   Mon Jan 27 16:30:29 2014 +0530

    Power: pmqos: Add emc freq pmqos constraint
    
    It adds min emc freq pmqos.
    
    Bug 1432476
    
    Change-Id: If05c2e8cceffc9ca071ed0b023c29e1ef2921245
    Signed-off-by: Puneet Saxena <puneets@nvidia.com>
    Reviewed-on: http://git-master/r/360379
    Reviewed-by: Automatic_Commit_Validation_User
    Reviewed-by: Aleksandr Frid <afrid@nvidia.com>
    Reviewed-by: Sachin Nikam <snikam@nvidia.com>

commit 896941396e1124aebd51c8b94eb1f694018136e4
Author: Dave Chinner <dchinner@redhat.com>
Date:   Tue Jul 2 22:38:35 2013 +1000

    sync: don't block the flusher thread waiting on IO
    
    When sync does it's WB_SYNC_ALL writeback, it issues data Io and
    then immediately waits for IO completion. This is done in the
    context of the flusher thread, and hence completely ties up the
    flusher thread for the backing device until all the dirty inodes
    have been synced. On filesystems that are dirtying inodes constantly
    and quickly, this means the flusher thread can be tied up for
    minutes per sync call and hence badly affect system level write IO
    performance as the page cache cannot be cleaned quickly.
    
    We already have a wait loop for IO completion for sync(2), so cut
    this out of the flusher thread and delegate it to wait_sb_inodes().
    Hence we can do rapid IO submission, and then wait for it all to
    complete.
    
    Effect of sync on fsmark before the patch:
    
    FSUse%        Count         Size    Files/sec     App Overhead
    .....
         0       640000         4096      35154.6          1026984
         0       720000         4096      36740.3          1023844
         0       800000         4096      36184.6           916599
         0       880000         4096       1282.7          1054367
         0       960000         4096       3951.3           918773
         0      1040000         4096      40646.2           996448
         0      1120000         4096      43610.1           895647
         0      1200000         4096      40333.1           921048
    
    And a single sync pass took:
    
      real    0m52.407s
      user    0m0.000s
      sys     0m0.090s
    
    After the patch, there is no impact on fsmark results, and each
    individual sync(2) operation run concurrently with the same fsmark
    workload takes roughly 7s:
    
      real    0m6.930s
      user    0m0.000s
      sys     0m0.039s
    
    IOWs, sync is 7-8x faster on a busy filesystem and does not have an
    adverse impact on ongoing async data write operations.
    
    Signed-off-by: Dave Chinner <dchinner@redhat.com>
    Reviewed-by: Jan Kara <jack@suse.cz>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit 263b529e71bd1e8035e6f3c979546dde68adbff5
Author: Kyungsik Lee <kyungsik.lee@lge.com>
Date:   Mon Jul 8 16:01:45 2013 -0700

    decompressor: add LZ4 decompressor module
    
    Add support for LZ4 decompression in the Linux Kernel.  LZ4 Decompression
    APIs for kernel are based on LZ4 implementation by Yann Collet.
    
    Benchmark Results(PATCH v3)
    Compiler: Linaro ARM gcc 4.6.2
    
    1. ARMv7, 1.5GHz based board
       Kernel: linux 3.4
       Uncompressed Kernel Size: 14MB
            Compressed Size  Decompression Speed
       LZO  6.7MB            20.1MB/s, 25.2MB/s(UA)
       LZ4  7.3MB            29.1MB/s, 45.6MB/s(UA)
    
    2. ARMv7, 1.7GHz based board
       Kernel: linux 3.7
       Uncompressed Kernel Size: 14MB
            Compressed Size  Decompression Speed
       LZO  6.0MB            34.1MB/s, 52.2MB/s(UA)
       LZ4  6.5MB            86.7MB/s
    - UA: Unaligned memory Access support
    - Latest patch set for LZO applied
    
    This patch set is for adding support for LZ4-compressed Kernel.  LZ4 is a
    very fast lossless compression algorithm and it also features an extremely
    fast decoder [1].
    
    But we have five of decompressors already and one question which does
    arise, however, is that of where do we stop adding new ones?  This issue
    had been discussed and came to the conclusion [2].
    
    Russell King said that we should have:
    
     - one decompressor which is the fastest
     - one decompressor for the highest compression ratio
     - one popular decompressor (eg conventional gzip)
    
    If we have a replacement one for one of these, then it should do exactly
    that: replace it.
    
    The benchmark shows that an 8% increase in image size vs a 66% increase
    in decompression speed compared to LZO(which has been known as the
    fastest decompressor in the Kernel).  Therefore the "fast but may not be
    small" compression title has clearly been taken by LZ4 [3].
    
    [1] http://code.google.com/p/lz4/
    [2] http://thread.gmane.org/gmane.linux.kbuild.devel/9157
    [3] http://thread.gmane.org/gmane.linux.kbuild.devel/9347
    
    LZ4 homepage: http://fastcompression.blogspot.com/p/lz4.html
    LZ4 source repository: http://code.google.com/p/lz4/
    
    Signed-off-by: Kyungsik Lee <kyungsik.lee@lge.com>
    Signed-off-by: Yann Collet <yann.collet.73@gmail.com>
    Cc: "H. Peter Anvin" <hpa@zytor.com>
    Cc: Ingo Molnar <mingo@elte.hu>
    Cc: Thomas Gleixner <tglx@linutronix.de>
    Cc: Russell King <rmk@arm.linux.org.uk>
    Cc: Borislav Petkov <bp@alien8.de>
    Cc: Florian Fainelli <florian@openwrt.org>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit 90739cc3364d6dd302d1807acfe291435616e1a0
Author: Kyungsik Lee <kyungsik.lee@lge.com>
Date:   Mon Jul 8 16:01:46 2013 -0700

    lib: add support for LZ4-compressed kernel
    
    Add support for extracting LZ4-compressed kernel images, as well as
    LZ4-compressed ramdisk images in the kernel boot process.
    
    Signed-off-by: Kyungsik Lee <kyungsik.lee@lge.com>
    Cc: "H. Peter Anvin" <hpa@zytor.com>
    Cc: Ingo Molnar <mingo@elte.hu>
    Cc: Thomas Gleixner <tglx@linutronix.de>
    Cc: Russell King <rmk@arm.linux.org.uk>
    Cc: Borislav Petkov <bp@alien8.de>
    Cc: Florian Fainelli <florian@openwrt.org>
    Cc: Yann Collet <yann.collet.73@gmail.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit 41bb9874759571d72c9d1a815917f72f1820e6af
Author: Chanho Min <chanho.min@lge.com>
Date:   Mon Jul 8 16:01:49 2013 -0700

    lib: add lz4 compressor module
    
    This patchset is for supporting LZ4 compression and the crypto API using
    it.
    
    As shown below, the size of data is a little bit bigger but compressing
    speed is faster under the enabled unaligned memory access.  We can use
    lz4 de/compression through crypto API as well.  Also, It will be useful
    for another potential user of lz4 compression.
    
    lz4 Compression Benchmark:
    Compiler: ARM gcc 4.6.4
    ARMv7, 1 GHz based board
       Kernel: linux 3.4
       Uncompressed data Size: 101 MB
             Compressed Size  compression Speed
       LZO   72.1MB		  32.1MB/s, 33.0MB/s(UA)
       LZ4   75.1MB		  30.4MB/s, 35.9MB/s(UA)
       LZ4HC 59.8MB		   2.4MB/s,  2.5MB/s(UA)
    - UA: Unaligned memory Access support
    - Latest patch set for LZO applied
    
    This patch:
    
    Add support for LZ4 compression in the Linux Kernel.  LZ4 Compression APIs
    for kernel are based on LZ4 implementation by Yann Collet and were changed
    for kernel coding style.
    
    LZ4 homepage : http://fastcompression.blogspot.com/p/lz4.html
    LZ4 source repository : http://code.google.com/p/lz4/
    svn revision : r90
    
    Two APIs are added:
    
    lz4_compress() support basic lz4 compression whereas lz4hc_compress()
    support high compression or CPU performance get lower but compression
    ratio get higher.  Also, we require the pre-allocated working memory with
    the defined size and destination buffer must be allocated with the size of
    lz4_compressbound.
    
    [akpm@linux-foundation.org: make lz4_compresshcctx() static]
    Signed-off-by: Chanho Min <chanho.min@lge.com>
    Cc: "Darrick J. Wong" <djwong@us.ibm.com>
    Cc: Bob Pearson <rpearson@systemfabricworks.com>
    Cc: Richard Weinberger <richard@nod.at>
    Cc: Herbert Xu <herbert@gondor.hengli.com.au>
    Cc: Yann Collet <yann.collet.73@gmail.com>
    Cc: Kyungsik Lee <kyungsik.lee@lge.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit ab8750365fcd48fe4c79932c16070e50bad4e3af
Author: Colin Cross <ccross@android.com>
Date:   Tue May 21 22:32:14 2013 -0700

    power: Add option to log time spent in suspend
    
    Below is a patch from android kernel that maintains a histogram of
    suspend times. Please review and provide feedback.
    
    Statistices on the time spent in suspend are kept in
    /sys/kernel/debug/sleep_time.
    
    Cc: Android Kernel Team <kernel-team@android.com>
    Cc: Colin Cross <ccross@android.com>
    Cc: Todd Poynor <toddpoynor@google.com>
    Cc: San Mehat <san@google.com>
    Cc: Benoit Goby <benoit@android.com>
    Cc: John Stultz <john.stultz@linaro.org>
    Cc: Thomas Gleixner <tglx@linutronix.de>
    Signed-off-by: Colin Cross <ccross@android.com>
    Signed-off-by: Todd Poynor <toddpoynor@google.com>
    [zoran.markovic@linaro.org: Re-formatted suspend time table to better
    fit expected values. Moved accounting of suspend time into timekeeping
    core. Removed CONFIG_SUSPEND_TIME flag and made the feature conditional
    on CONFIG_DEBUG_FS. Changed the file name to sleep_time to better fit
    terminology in timekeeping core. Changed seq_printf to seq_puts. Tweaked
    commit message]
    Signed-off-by: Zoran Markovic <zoran.markovic@linaro.org>
    Signed-off-by: John Stultz <john.stultz@linaro.org>

commit b42728095589cbe50a014175ad70c85c766e0224
Author: Kamalesh Babulal <kamalesh@linux.vnet.ibm.com>
Date:   Tue Jun 25 13:33:36 2013 +0530

    sched/debug: Add load-tracking statistics to task
    
    At present we print per-entity load-tracking statistics for
    cfs_rq of cgroups/runqueues. Given that per task statistics
    is maintained, it can be used to know the contribution made
    by the task to its parenting cfs_rq level.
    
    This patch adds per-task load-tracking statistics to /proc/<PID>/sched.
    
    Signed-off-by: Kamalesh Babulal <kamalesh@linux.vnet.ibm.com>
    Signed-off-by: Peter Zijlstra <peterz@infradead.org>
    Link: http://lkml.kernel.org/r/20130625080336.GA20175@linux.vnet.ibm.com
    Signed-off-by: Ingo Molnar <mingo@kernel.org>

commit a3d9ab960f2765e2238dca798ab81177533d9ddc
Author: Kent Overstreet <koverstreet@google.com>
Date:   Fri May 31 15:26:45 2013 -0700

    percpu: implement generic percpu refcounting
    
    This implements a refcount with similar semantics to
    atomic_get()/atomic_dec_and_test() - but percpu.
    
    It also implements two stage shutdown, as we need it to tear down the
    percpu counts.  Before dropping the initial refcount, you must call
    percpu_ref_kill(); this puts the refcount in "shutting down mode" and
    switches back to a single atomic refcount with the appropriate
    barriers (synchronize_rcu()).
    
    It's also legal to call percpu_ref_kill() multiple times - it only
    returns true once, so callers don't have to reimplement shutdown
    synchronization.
    
    [akpm@linux-foundation.org: fix build]
    [akpm@linux-foundation.org: coding-style tweak]
    Signed-off-by: Kent Overstreet <koverstreet@google.com>
    Cc: Zach Brown <zab@redhat.com>
    Cc: Felipe Balbi <balbi@ti.com>
    Cc: Greg Kroah-Hartman <gregkh@linuxfoundation.org>
    Cc: Mark Fasheh <mfasheh@suse.com>
    Cc: Joel Becker <jlbec@evilplan.org>
    Cc: Rusty Russell <rusty@rustcorp.com.au>
    Cc: Jens Axboe <axboe@kernel.dk>
    Cc: Asai Thambi S P <asamymuthupa@micron.com>
    Cc: Selvan Mani <smani@micron.com>
    Cc: Sam Bradshaw <sbradshaw@micron.com>
    Cc: Jeff Moyer <jmoyer@redhat.com>
    Cc: Al Viro <viro@zeniv.linux.org.uk>
    Cc: Benjamin LaHaise <bcrl@kvack.org>
    Cc: Tejun Heo <tj@kernel.org>
    Cc: Oleg Nesterov <oleg@redhat.com>
    Cc: Christoph Lameter <cl@linux-foundation.org>
    Cc: Ingo Molnar <mingo@redhat.com>
    Reviewed-by: "Theodore Ts'o" <tytso@mit.edu>
    Signed-off-by: Tejun Heo <tj@kernel.org>

commit 1e57753fcdb1ebed63e4024334af5d9562e95d19
Author: Michael Wang <wangyun@linux.vnet.ibm.com>
Date:   Thu Jul 4 12:55:51 2013 +0800

    sched: Implement smarter wake-affine logic
    
    The wake-affine scheduler feature is currently always trying to pull
    the wakee close to the waker. In theory this should be beneficial if
    the waker's CPU caches hot data for the wakee, and it's also beneficial
    in the extreme ping-pong high context switch rate case.
    
    Testing shows it can benefit hackbench up to 15%.
    
    However, the feature is somewhat blind, from which some workloads
    such as pgbench suffer. It's also time-consuming algorithmically.
    
    Testing shows it can damage pgbench up to 50% - far more than the
    benefit it brings in the best case.
    
    So wake-affine should be smarter and it should realize when to
    stop its thankless effort at trying to find a suitable CPU to wake on.
    
    This patch introduces 'wakee_flips', which will be increased each
    time the task flips (switches) its wakee target.
    
    So a high 'wakee_flips' value means the task has more than one
    wakee, and the bigger the number, the higher the wakeup frequency.
    
    Now when making the decision on whether to pull or not, pay attention to
    the wakee with a high 'wakee_flips', pulling such a task may benefit
    the wakee. Also imply that the waker will face cruel competition later,
    it could be very cruel or very fast depends on the story behind
    'wakee_flips', waker therefore suffers.
    
    Furthermore, if waker also has a high 'wakee_flips', that implies that
    multiple tasks rely on it, then waker's higher latency will damage all
    of them, so pulling wakee seems to be a bad deal.
    
    Thus, when 'waker->wakee_flips / wakee->wakee_flips' becomes
    higher and higher, the cost of pulling seems to be worse and worse.
    
    The patch therefore helps the wake-affine feature to stop its pulling
    work when:
    
    	wakee->wakee_flips > factor &&
    	waker->wakee_flips > (factor * wakee->wakee_flips)
    
    The 'factor' here is the number of CPUs in the current CPU's NUMA node,
    so a bigger node will lead to more pulling since the trial becomes more
    severe.
    
    After applying the patch, pgbench shows up to 40% improvements and no regressions.
    
    Tested with 12 cpu x86 server and tip 3.10.0-rc7.
    
    The percentages in the final column highlight the areas with the biggest wins,
    all other areas improved as well:
    
    	pgbench		    base	smart
    
    	| db_size | clients |  tps  |	|  tps  |
    	+---------+---------+-------+   +-------+
    	| 22 MB   |       1 | 10598 |   | 10796 |
    	| 22 MB   |       2 | 21257 |   | 21336 |
    	| 22 MB   |       4 | 41386 |   | 41622 |
    	| 22 MB   |       8 | 51253 |   | 57932 |
    	| 22 MB   |      12 | 48570 |   | 54000 |
    	| 22 MB   |      16 | 46748 |   | 55982 | +19.75%
    	| 22 MB   |      24 | 44346 |   | 55847 | +25.93%
    	| 22 MB   |      32 | 43460 |   | 54614 | +25.66%
    	| 7484 MB |       1 |  8951 |   |  9193 |
    	| 7484 MB |       2 | 19233 |   | 19240 |
    	| 7484 MB |       4 | 37239 |   | 37302 |
    	| 7484 MB |       8 | 46087 |   | 50018 |
    	| 7484 MB |      12 | 42054 |   | 48763 |
    	| 7484 MB |      16 | 40765 |   | 51633 | +26.66%
    	| 7484 MB |      24 | 37651 |   | 52377 | +39.11%
    	| 7484 MB |      32 | 37056 |   | 51108 | +37.92%
    	| 15 GB   |       1 |  8845 |   |  9104 |
    	| 15 GB   |       2 | 19094 |   | 19162 |
    	| 15 GB   |       4 | 36979 |   | 36983 |
    	| 15 GB   |       8 | 46087 |   | 49977 |
    	| 15 GB   |      12 | 41901 |   | 48591 |
    	| 15 GB   |      16 | 40147 |   | 50651 | +26.16%
    	| 15 GB   |      24 | 37250 |   | 52365 | +40.58%
    	| 15 GB   |      32 | 36470 |   | 50015 | +37.14%
    
    Signed-off-by: Michael Wang <wangyun@linux.vnet.ibm.com>
    Cc: Mike Galbraith <efault@gmx.de>
    Signed-off-by: Peter Zijlstra <peterz@infradead.org>
    Link: http://lkml.kernel.org/r/51D50057.9000809@linux.vnet.ibm.com
    [ Improved the changelog. ]
    Signed-off-by: Ingo Molnar <mingo@kernel.org>

commit 8080677cf402756d76ecd201c0676edb0e65eb35
Author: Ard Biesheuvel <ard.biesheuvel@linaro.org>
Date:   Fri May 17 18:51:23 2013 +0200

    ARM: crypto: add NEON accelerated XOR implementation
    
    Add a source file xor-neon.c (which is really just the reference
    C implementation passed through the GCC vectorizer) and hook it
    up to the XOR framework.
    
    Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
    Acked-by: Nicolas Pitre <nico@linaro.org>

commit b299d56e72f0e4c49ff31ff68fb05d6526018475
Author: Yuchung Cheng <ycheng@google.com>
Date:   Thu Oct 31 09:19:32 2013 -0700

    tcp: enable sockets to use MSG_FASTOPEN by default
    
    Applications have started to use Fast Open (e.g., Chrome browser has
    such an optional flag) and the feature has gone through several
    generations of kernels since 3.7 with many real network tests. It's
    time to enable this flag by default for applications to test more
    conveniently and extensively.
    
    Signed-off-by: Yuchung Cheng <ycheng@google.com>
    Signed-off-by: Neal Cardwell <ncardwell@google.com>
    Acked-by: Eric Dumazet <edumazet@google.com>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit fac2b9e0e1c156293e8846bcb57da7ba99ad8c05
Author: Davidlohr Bueso <davidlohr@hp.com>
Date:   Sun Jan 12 15:31:23 2014 -0800

    futexes: Increase hash table size for better performance
    
    Currently, the futex global hash table suffers from its fixed,
    smallish (for today's standards) size of 256 entries, as well as
    its lack of NUMA awareness. Large systems, using many futexes,
    can be prone to high amounts of collisions; where these futexes
    hash to the same bucket and lead to extra contention on the same
    hb->lock. Furthermore, cacheline bouncing is a reality when we
    have multiple hb->locks residing on the same cacheline and
    different futexes hash to adjacent buckets.
    
    This patch keeps the current static size of 16 entries for small
    systems, or otherwise, 256 * ncpus (or larger as we need to
    round the number to a power of 2). Note that this number of CPUs
    accounts for all CPUs that can ever be available in the system,
    taking into consideration things like hotpluging. While we do
    impose extra overhead at bootup by making the hash table larger,
    this is a one time thing, and does not shadow the benefits of
    this patch.
    
    Furthermore, as suggested by tglx, by cache aligning the hash
    buckets we can avoid access across cacheline boundaries and also
    avoid massive cache line bouncing if multiple cpus are hammering
    away at different hash buckets which happen to reside in the
    same cache line.
    
    Also, similar to other core kernel components (pid, dcache,
    tcp), by using alloc_large_system_hash() we benefit from its
    NUMA awareness and thus the table is distributed among the nodes
    instead of in a single one.
    
    For a custom microbenchmark that pounds on the uaddr hashing --
    making the wait path fail at futex_wait_setup() returning
    -EWOULDBLOCK for large amounts of futexes, we can see the
    following benefits on a 80-core, 8-socket 1Tb server:
    
     +---------+--------------------+------------------------+-----------------------+-------------------------------+
     | threads | baseline (ops/sec) | aligned-only (ops/sec) | large table (ops/sec) | large table+aligned (ops/sec) |
     +---------+--------------------+------------------------+-----------------------+-------------------------------+
     |     512 |              32426 | 50531  (+55.8%)        | 255274  (+687.2%)     | 292553  (+802.2%)             |
     |     256 |              65360 | 99588  (+52.3%)        | 443563  (+578.6%)     | 508088  (+677.3%)             |
     |     128 |             125635 | 200075 (+59.2%)        | 742613  (+491.1%)     | 835452  (+564.9%)             |
     |      80 |             193559 | 323425 (+67.1%)        | 1028147 (+431.1%)     | 1130304 (+483.9%)             |
     |      64 |             247667 | 443740 (+79.1%)        | 997300  (+302.6%)     | 1145494 (+362.5%)             |
     |      32 |             628412 | 721401 (+14.7%)        | 965996  (+53.7%)      | 1122115 (+78.5%)              |
     +---------+--------------------+------------------------+-----------------------+-------------------------------+
    
    Reviewed-by: Darren Hart <dvhart@linux.intel.com>
    Reviewed-by: Peter Zijlstra <peterz@infradead.org>
    Reviewed-by: Paul E. McKenney <paulmck@linux.vnet.ibm.com>
    Reviewed-by: Waiman Long <Waiman.Long@hp.com>
    Reviewed-and-tested-by: Jason Low <jason.low2@hp.com>
    Reviewed-by: Thomas Gleixner <tglx@linutronix.de>
    Signed-off-by: Davidlohr Bueso <davidlohr@hp.com>
    Cc: Mike Galbraith <efault@gmx.de>
    Cc: Jeff Mahoney <jeffm@suse.com>
    Cc: Linus Torvalds <torvalds@linux-foundation.org>
    Cc: Scott Norton <scott.norton@hp.com>
    Cc: Tom Vaden <tom.vaden@hp.com>
    Cc: Aswin Chandramouleeswaran <aswin@hp.com>
    Link: http://lkml.kernel.org/r/1389569486-25487-3-git-send-email-davidlohr@hp.com
    Signed-off-by: Ingo Molnar <mingo@kernel.org>
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Modified for Nexus 9
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	kernel/futex.c
    
    Conflicts:
    	kernel/futex.c
    
    Conflicts:
    	kernel/futex.c

commit 92310a9edd06e6ce983f98aa45eb4eb73cfac22e
Author: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
Date:   Wed Feb 26 01:00:30 2014 +0100

    PCI / PM: Resume runtime-suspended devices later during system suspend
    
    Runtime-suspended devices are resumed during system suspend by
    pci_pm_prepare() for two reasons: First, because they may need
    to be reprogrammed in order to change their wakeup settings and,
    second, because they may need to be operatonal for their children
    to be successfully suspended.  That is a problem, though, if there
    are many runtime-suspended devices that need to be resumed this
    way during system suspend, because the .prepare() PM callbacks of
    devices are executed sequentially and the times taken by them
    accumulate, which may increase the total system suspend time quite
    a bit.
    
    For this reason, move the resume of runtime-suspended devices up
    to the next phase of device suspend (during system suspend), except
    for the ones that have power.ignore_children set.  The exception is
    made, because the devices with power.ignore_children set may still
    be necessary for their children to be successfully suspended (during
    system suspend) and they won't be resumed automatically as a result
    of the runtime resume of their children.
    
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
    Acked-by: Bjorn Helgaas <bhelgaas@google.com>

commit 8373f586032443904f18767c46ce51785b44299a
Author: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
Date:   Wed Feb 26 01:00:19 2014 +0100

    ACPI / PM: Resume runtime-suspended devices later during system suspend
    
    Runtime-suspended devices are resumed during system suspend by
    acpi_subsys_prepare() for two reasons: First, because they may need
    to be reprogrammed in order to change their wakeup settings and,
    second, because they may need to be operatonal for their children
    to be successfully suspended.  That is a problem, though, if there
    are many runtime-suspended devices that need to be resumed this
    way during system suspend, because the .prepare() PM callbacks of
    devices are executed sequentially and the times taken by them
    accumulate, which may increase the total system suspend time quite
    a bit.
    
    For this reason, move the resume of runtime-suspended devices up
    to the next phase of device suspend (during system suspend), except
    for the ones that have power.ignore_children set.  The exception is
    made, because the devices with power.ignore_children set may still
    be necessary for their children to be successfully suspended (during
    system suspend) and they won't be resumed automatically as a result
    of the runtime resume of their children.
    
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>

commit c18063e3d2dccde0865d0e846e3b9935aaf5e003
Author: Mel Gorman <mgorman@suse.de>
Date:   Wed Jun 4 16:07:14 2014 -0700

    mm: disable zone_reclaim_mode by default
    
    When it was introduced, zone_reclaim_mode made sense as NUMA distances
    punished and workloads were generally partitioned to fit into a NUMA
    node.  NUMA machines are now common but few of the workloads are
    NUMA-aware and it's routine to see major performance degradation due to
    zone_reclaim_mode being enabled but relatively few can identify the
    problem.
    
    Those that require zone_reclaim_mode are likely to be able to detect
    when it needs to be enabled and tune appropriately so lets have a
    sensible default for the bulk of users.
    
    This patch (of 2):
    
    zone_reclaim_mode causes processes to prefer reclaiming memory from
    local node instead of spilling over to other nodes.  This made sense
    initially when NUMA machines were almost exclusively HPC and the
    workload was partitioned into nodes.  The NUMA penalties were
    sufficiently high to justify reclaiming the memory.  On current machines
    and workloads it is often the case that zone_reclaim_mode destroys
    performance but not all users know how to detect this.  Favour the
    common case and disable it by default.  Users that are sophisticated
    enough to know they need zone_reclaim_mode will detect it.
    
    Signed-off-by: Mel Gorman <mgorman@suse.de>
    Acked-by: Johannes Weiner <hannes@cmpxchg.org>
    Reviewed-by: Zhang Yanfei <zhangyanfei@cn.fujitsu.com>
    Acked-by: Michal Hocko <mhocko@suse.cz>
    Reviewed-by: Christoph Lameter <cl@linux.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit 3e038ffc2fd7e4f50ec3e1e9ca77267031ce7900
Author: Srivatsa S. Bhat <srivatsa.bhat@linux.vnet.ibm.com>
Date:   Sun Jun 8 02:11:43 2014 +0530

    cpufreq: governor: Be friendly towards latency-sensitive bursty workloads
    
    Cpufreq governors like the ondemand governor calculate the load on the CPU
    periodically by employing deferrable timers. A deferrable timer won't fire
    if the CPU is completely idle (and there are no other timers to be run), in
    order to avoid unnecessary wakeups and thus save CPU power.
    
    However, the load calculation logic is agnostic to all this, and this can
    lead to the problem described below.
    
    Time (ms)               CPU 1
    
    100                Task-A running
    
    110                Governor's timer fires, finds load as 100% in the last
                       10ms interval and increases the CPU frequency.
    
    110.5              Task-A running
    
    120		   Governor's timer fires, finds load as 100% in the last
    		   10ms interval and increases the CPU frequency.
    
    125		   Task-A went to sleep. With nothing else to do, CPU 1
    		   went completely idle.
    
    200		   Task-A woke up and started running again.
    
    200.5		   Governor's deferred timer (which was originally programmed
    		   to fire at time 130) fires now. It calculates load for the
    		   time period 120 to 200.5, and finds the load is almost zero.
    		   Hence it decreases the CPU frequency to the minimum.
    
    210		   Governor's timer fires, finds load as 100% in the last
    		   10ms interval and increases the CPU frequency.
    
    So, after the workload woke up and started running, the frequency was suddenly
    dropped to absolute minimum, and after that, there was an unnecessary delay of
    10ms (sampling period) to increase the CPU frequency back to a reasonable value.
    And this pattern repeats for every wake-up-from-cpu-idle for that workload.
    This can be quite undesirable for latency- or response-time sensitive bursty
    workloads. So we need to fix the governor's logic to detect such wake-up-from-
    cpu-idle scenarios and start the workload at a reasonably high CPU frequency.
    
    One extreme solution would be to fake a load of 100% in such scenarios. But
    that might lead to undesirable side-effects such as frequency spikes (which
    might also need voltage changes) especially if the previous frequency happened
    to be very low.
    
    We just want to avoid the stupidity of dropping down the frequency to a minimum
    and then enduring a needless (and long) delay before ramping it up back again.
    So, let us simply carry forward the previous load - that is, let us just pretend
    that the 'load' for the current time-window is the same as the load for the
    previous window. That way, the frequency and voltage will continue to be set
    to whatever values they were set at previously. This means that bursty workloads
    will get a chance to influence the CPU frequency at which they wake up from
    cpu-idle, based on their past execution history. Thus, they might be able to
    avoid suffering from slow wakeups and long response-times.
    
    However, we should take care not to over-do this. For example, such a "copy
    previous load" logic will benefit cases like this: (where # represents busy
    and . represents idle)
    
    ##########.........#########.........###########...........##########........
    
    but it will be detrimental in cases like the one shown below, because it will
    retain the high frequency (copied from the previous interval) even in a mostly
    idle system:
    
    ##########.........#.................#.....................#...............
    
    (i.e., the workload finished and the remaining tasks are such that their busy
    periods are smaller than the sampling interval, which causes the timer to
    always get deferred. So, this will make the copy-previous-load logic copy
    the initial high load to subsequent idle periods over and over again, thus
    keeping the frequency high unnecessarily).
    
    So, we modify this copy-previous-load logic such that it is used only once
    upon every wakeup-from-idle. Thus if we have 2 consecutive idle periods, the
    previous load won't get blindly copied over; cpufreq will freshly evaluate the
    load in the second idle interval, thus ensuring that the system comes back to
    its normal state.
    
    [ The right way to solve this whole problem is to teach the CPU frequency
    governors to also track load on a per-task basis, not just a per-CPU basis,
    and then use both the data sources intelligently to set the appropriate
    frequency on the CPUs. But that involves redesigning the cpufreq subsystem,
    so this patch should make the situation bearable until then. ]
    
    Experimental results:
    +-------------------+
    
    I ran a modified version of ebizzy (called 'sleeping-ebizzy') that sleeps in
    between its execution such that its total utilization can be a user-defined
    value, say 10% or 20% (higher the utilization specified, lesser the amount of
    sleeps injected). This ebizzy was run with a single-thread, tied to CPU 8.
    
    Behavior observed with tracing (sample taken from 40% utilization runs):
    ------------------------------------------------------------------------
    
    Without patch:
    ~~~~~~~~~~~~~~
    kworker/8:2-12137  416.335742: cpu_frequency: state=2061000 cpu_id=8
    kworker/8:2-12137  416.335744: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40753  416.345741: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-12137  416.345744: cpu_frequency: state=4123000 cpu_id=8
    kworker/8:2-12137  416.345746: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40753  416.355738: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    <snip>  ---------------------------------------------------------------------  <snip>
          <...>-40753  416.402202: sched_switch: prev_comm=ebizzy ==> next_comm=swapper/8
         <idle>-0      416.502130: sched_switch: prev_comm=swapper/8 ==> next_comm=ebizzy
          <...>-40753  416.505738: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-12137  416.505739: cpu_frequency: state=2061000 cpu_id=8
    kworker/8:2-12137  416.505741: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40753  416.515739: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-12137  416.515742: cpu_frequency: state=4123000 cpu_id=8
    kworker/8:2-12137  416.515744: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
    
    Observation: Ebizzy went idle at 416.402202, and started running again at
    416.502130. But cpufreq noticed the long idle period, and dropped the frequency
    at 416.505739, only to increase it back again at 416.515742, realizing that the
    workload is in-fact CPU bound. Thus ebizzy needlessly ran at the lowest frequency
    for almost 13 milliseconds (almost 1 full sample period), and this pattern
    repeats on every sleep-wakeup. This could hurt latency-sensitive workloads quite
    a lot.
    
    With patch:
    ~~~~~~~~~~~
    
    kworker/8:2-29802  464.832535: cpu_frequency: state=2061000 cpu_id=8
    <snip>  ---------------------------------------------------------------------  <snip>
    kworker/8:2-29802  464.962538: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40738  464.972533: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-29802  464.972536: cpu_frequency: state=4123000 cpu_id=8
    kworker/8:2-29802  464.972538: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40738  464.982531: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    <snip>  ---------------------------------------------------------------------  <snip>
    kworker/8:2-29802  465.022533: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40738  465.032531: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-29802  465.032532: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40738  465.035797: sched_switch: prev_comm=ebizzy ==> next_comm=swapper/8
         <idle>-0      465.240178: sched_switch: prev_comm=swapper/8 ==> next_comm=ebizzy
          <...>-40738  465.242533: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    kworker/8:2-29802  465.242535: sched_switch: prev_comm=kworker/8:2 ==> next_comm=ebizzy
          <...>-40738  465.252531: sched_switch: prev_comm=ebizzy ==> next_comm=kworker/8:2
    
    Observation: Ebizzy went idle at 465.035797, and started running again at
    465.240178. Since ebizzy was the only real workload running on this CPU,
    cpufreq retained the frequency at 4.1Ghz throughout the run of ebizzy, no
    matter how many times ebizzy slept and woke-up in-between. Thus, ebizzy
    got the 10ms worth of 4.1 Ghz benefit during every sleep-wakeup (as compared
    to the run without the patch) and this boost gave a modest improvement in total
    throughput, as shown below.
    
    Sleeping-ebizzy records-per-second:
    -----------------------------------
    
    Utilization  Without patch  With patch  Difference (Absolute and % values)
        10%         274767        277046        +  2279 (+0.829%)
        20%         543429        553484        + 10055 (+1.850%)
        40%        1090744       1107959        + 17215 (+1.578%)
        60%        1634908       1662018        + 27110 (+1.658%)
    
    A rudimentary and somewhat approximately latency-sensitive workload such as
    sleeping-ebizzy itself showed a consistent, noticeable performance improvement
    with this patch. Hence, workloads that are truly latency-sensitive will benefit
    quite a bit from this change. Moreover, this is an overall win-win since this
    patch does not hurt power-savings at all (because, this patch does not reduce
    the idle time or idle residency; and the high frequency of the CPU when it goes
    to cpu-idle does not affect/hurt the power-savings of deep idle states).
    
    Signed-off-by: Srivatsa S. Bhat <srivatsa.bhat@linux.vnet.ibm.com>
    Reviewed-by: Gautham R. Shenoy <ego@linux.vnet.ibm.com>
    Acked-by: Viresh Kumar <viresh.kumar@linaro.org>
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>

commit ce7e47457450a2f76b1a2165bd15325be0c01975
Author: Paul Reioux <reioux@gmail.com>
Date:   Thu Jan 9 14:31:09 2014 -0600

    ARM: move VFP init to an earlier boot stage
    
    In order to use the NEON unit in the kernel, we should
    initialize it a bit earlier in the boot process so NEON users
    that like to do a quick benchmark at load time (like the
    xor_blocks or RAID-6 code) find the NEON/VFP unit already
    enabled.
    
    Replaced late_initcall() with core_initcall().
    
    Signed-off-by: Ard Biesheuvel <ard.biesheuvel at linaro.org>
    Acked-by: Nicolas Pitre <nico at linaro.org>
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>
    
    Conflicts:
    	arch/arm/vfp/vfpmodule.c

commit 2683b9da4ef95b039ad9e7074d3aeb746dac6a0a
Author: Paul Reioux <reioux@gmail.com>
Date:   Thu Jan 9 01:22:04 2014 -0800

    ARM: be strict about FP exceptions in kernel mode
    
    The support code in vfp_support_entry does not care whether the
    exception that caused it to be invoked occurred in kernel mode or
    in user mode. However, neither condition that could trigger this
    exception (lazy restore and VFP bounce to support code) is
    currently allowable in kernel mode.
    
    In either case, print a message describing the condition before
    letting the undefined instruction handler run its course and trigger
    an oops.
    
    Signed-off-by: Ard Biesheuvel <ard.biesheuvel at linaro.org>
    Acked-by: Nicolas Pitre <nico at linaro.org>
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 810bb46cabcababe4a35d6e5a67d8c1b08fdc6d9
Author: Paul Reioux <reioux@gmail.com>
Date:   Thu Jan 9 01:16:06 2014 -0800

    ARM: add support for kernel mode NEON
    
    In order to safely support the use of NEON instructions in
    kernel mode, some precautions need to be taken:
    - the userland context that may be present in the registers (even
      if the NEON/VFP is currently disabled) must be stored under the
      correct task (which may not be 'current' in the UP case),
    - to avoid having to keep track of additional vfpstates for the
      kernel side, disallow the use of NEON in interrupt context
      and run with preemption disabled,
    - after use, re-enable preemption and re-enable the lazy restore
      machinery by disabling the NEON/VFP unit.
    
    This patch adds the functions kernel_neon_begin() and
    kernel_neon_end() which take care of the above. It also adds
    the Kconfig symbol KERNEL_MODE_NEON to enable it.
    
    Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
    Acked-by: Nicolas Pitre <nico@linaro.org>
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit a023f5e4277947d9c0035f402edde765daabaf1b
Author: Ard Biesheuvel <ard.biesheuvel@linaro.org>
Date:   Mon Sep 9 14:08:38 2013 +0000

    ARM: 7835/2: fix modular build of xor_blocks() with NEON enabled
    
    Commit 0195659 introduced a NEON accelerated version of the xor_blocks()
    function, but it needs the changes in this patch to allow it to be built
    as a module rather than statically into the kernel.
    
    This patch creates a separate module xor-neon.ko which exports the NEON
    inner xor_blocks() functions depended upon by the regular xor.ko if it
    is built with CONFIG_KERNEL_MODE_NEON=y
    
    Reported-by: Josh Boyer <jwboyer@fedoraproject.org>
    Signed-off-by: Ard Biesheuvel <ard.biesheuvel@linaro.org>
    Signed-off-by: Russell King <rmk+kernel@arm.linux.org.uk>

commit 5c67d36cb2619c5dfd641a0aa31889cfbf644df0
Author: Russell King <rmk+kernel@arm.linux.org.uk>
Date:   Sun Sep 22 10:08:50 2013 +0000

    ARM: only allow kernel mode neon with AEABI
    
    This prevents the linker erroring with:
    
    arm-linux-ld: error: arch/arm/lib/xor-neon.o uses VFP instructions, whereas arch/arm/lib/built-in.o does not
    arm-linux-ld: failed to merge target specific data of file arch/arm/lib/xor-neon.o
    
    This is due to the non-neon files being marked as containing FPA data/
    instructions (even though they do not) being mixed with files which
    contain VFP, which is an incompatible floating point format.
    
    Signed-off-by: Russell King <rmk+kernel@arm.linux.org.uk>

commit 97191505ece8d1213ff134ca811d5efca9813958
Author: Paul Reioux <reioux@gmail.com>
Date:   Sun Jan 18 22:36:40 2015 -0600

    arm/kernel/irq.c: remove irq affinity warnings
    
    the spurious warning was a result of deeper idle mode which act like unplugging
    without actually unplugged thus lead to this warning.
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 4f68c7f3fa243bf5b9ded8d3816ca7a0cea89bcf
Author: Zhang Rui <rui.zhang@intel.com>
Date:   Wed May 28 15:23:35 2014 +0800

    PM / sleep: unregister wakeup source when disabling device wakeup
    
    When enabling a device' wakeup capability, a wakeup source
    is created for the device automatically. But the wakeup source
    is not unregistered when disabling the device' wakeup capability.
    
    This results in zombie wakeup sources, after devices/drivers are unregistered.
    
    Signed-off-by: Zhang Rui <rui.zhang@intel.com>
    Signed-off-by: Rafael J. Wysocki <rafael.j.wysocki@intel.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit b467316fe875abff5cccd993068f3c17b4d27251
Author: Arun Kumar Neelakantam <aneela@codeaurora.org>
Date:   Tue Oct 28 13:57:25 2014 +0530

    soc: qcom: smd: Register SMD & SMSM IRQs with IRQF_NO_SUSPEND flag
    
    During system suspend/resume path IRQs are temporarily disabled unless
    the IRQF_NO_SUSPEND flag is specified. If a wakeup-enabled interrupt
    comes in during this timeframe, it will be masked until the suspend
    process is complete leading to delayed processing.
    
    Register the SMD and SMSM wakeup enable IRQs with IRQF_NO_SUSPEND flags
    to avoid delaying the interrupt during system suspend/resume path.
    
    CRs-Fixed: 724932
    Change-Id: Ib93c911f4a4e70638ebf23bc22ee7f5a685dca70
    Signed-off-by: Arun Kumar Neelakantam <aneela@codeaurora.org>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit d5fa8d3b4a3415b2d016b5554506f27c78e4bebc
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 21:15:27 2015 -0700

    Add /dev/frandom support
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit a28ec854d4279a037ebc8935d5ad134dab5b66f4
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 21:22:27 2015 -0700

    update defconfig

commit ded88c4ad5543172ea5e0b874aa51fb39f1b9d2c
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Tue Dec 16 04:33:42 2014 -0500

    drivers: w1: register any S-View cover as authentic
    
    This allows setting a kernel config flag to force the read of any
    S-View cover as an authentic Samsung product

commit 39795a2dcf0b430e2e5557ba8eeec870c2b27436
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Thu Jan 1 20:33:43 2015 -0500

    drivers: w1: allow user to override S-View bypass
    
    The user may now disable the S-View authentication bypass by changing
    the sysfs value for “user” to 0.
    Developers may also prevent the authentication bypass by not defining
    the config flag “CONFIG_SVIEW_BYPASS”
    
    Conflicts:
    	drivers/w1/w1.c

commit ed58b7462e971708480ec5600f6b782d8d2c2479
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Fri Jan 2 12:30:58 2015 -0500

    drivers: w1: enable readwrite for S-View bypass

commit 97aa32d247100a339cdfc127df6b24dbb530fde3
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 21:26:30 2015 -0700

    added sysfs interface for GENTLE_FAIR_SLEEPERS [neobuddy89]

commit e00222b0d97850e98e29c84a3469022a5ff02d48
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Sun Jan 4 20:57:48 2015 +0100

    reduce wakelocks: wlan_rx_wake and wlan_ctrl_wake

commit 8be012ba3a662be10ba6008a8d0f013b59f7d2fb
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Tue Dec 30 20:46:21 2014 +0100

    add Led Control
    
    Thanks to Twistedumbrella and Ktoonsez
    
    Conflicts:
    
    	drivers/leds/leds-max77843-rgb.c

commit 2120000d10700413ebc79ca3d43aef8bd393a1e8
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 21:34:12 2015 -0700

    add Dynamic Fsync control
    version 1.5 by faux123

commit 4f13bfa0be8120a6c8c778ca52735dd1b4def646
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 23:30:12 2015 -0700

    Revert : add Led Control
    
    Thanks to Twistedumbrella and Ktoonsez
    
    Conflicts:
    
    	drivers/leds/leds-max77843-rgb.c (reverted from commit 8be012ba3a662be10ba6008a8d0f013b59f7d2fb)

commit 8011a0f0774322570e4311f7ace8a26c6bdeffc4
Author: Paul Reioux <reioux@gmail.com>
Date:   Fri Nov 21 12:53:59 2014 -0600

    system_rev: fix type mismatch derps by Samsung
    
    Signed-off-by: Paul Reioux <reioux@gmail.com>

commit 99e73acb0e325889d6209d0f31303b1e52a08c6a
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Mar 11 23:49:38 2015 -0700

    fix compile errors for dyynamic fsync

commit fe81847273d93be05293bd070265b787b2d111df
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 00:47:16 2015 -0700

    Revert: intelli_thermal v3.0: initial coding for Linux 3.10 Qualcomm kernels (faux123)
    
    Intelli_thermal is a replacement for the existing Qualcomm msm_thermal engine.
    It allows users greater controls over the stock Qualcomm thermal engine while
    maintaining full backwards compatibilty.
    
    Copyright 2014~2015 Paul Reioux (aka Faux123)
    
    Signed-off-by: Paul Reioux <reioux@gmail.com> (reverted from commit ba69a437c9ef7e6221faa288dea4e9f15c890867)

commit bb12a28e80c4da9b26d0c4a96b332de228198e2e
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 08:33:30 2015 -0700

    system_rev: fix type

commit 6df08163ba42601030ec20043d25dc3a3c04cb1e
Author: imoseyon <imoseyon@gmail.com>
Date:   Mon Nov 24 19:56:09 2014 -0800

    clock-krait/cpufreq: custom voltage control v1

commit 61b260291e142f4e86c864933e7ef9c58eaf8bdd
Author: imoseyon <imoseyon@gmail.com>
Date:   Mon Nov 24 20:02:19 2014 -0800

    clock-krait: 8084 can go up to 1.275v safely

commit 6d6f831882aae5f130acc66e4d071b267f76e8de
Author: franciscofranco <franciscofranco.1990@gmail.com>
Date:   Sun Jan 4 03:50:57 2015 +0000

    arm: dts: Allow power collapse as minimum l2 gdhs mode. From https://github.com/myfluxi/android_kernel_lge_hammerhead/commit/0318f7f4fbebe391ecfdebff4d7d82be2fca93d9
    
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 7b3f319dccdc2f64d0329e03144f830e4a93e5c4
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Thu Jan 8 12:33:08 2015 +0100

    cpufreq: interactive: don't skip waking up speedchange_task if target…
    …_freq > policy->cur
    
    When __cpufreq_driver_target() in speedchange_task failed for some reason, the
    policy->cur could be lower than the target_freq. The governor misses to change
    the target_freq if the target_freq is equal to the next_freq at the next sample
    time.
    
    Added a check to prevent the CPU to stay at the speed that is lower than the
    target_freq for long duration.
    
    Change-Id: Ibfdcd193b8280390b8f8374a63218aa31267f310
    Signed-off-by: Minsung Kim <ms925.kim@samsung.com>

commit 60429b85fb0ab5d10274d20f930c13e78d8d285b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 22:08:08 2015 -0700

    cpufreq_interactive: import interactive governor from Shamu
    
    Damn Samsung! You are cheating. In his stock kernel the interactive governor is going very well, from his source code interactive is very laggy.
    Now The governor runs well.
    
    Signed-off-by: Pafcholini <pafcholini@gmail.com>

commit cd17227c1dc5104575f7e5e5b955e8203f7bdaa4
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 23:02:26 2015 -0700

    Add a few governors

commit ea757d5cee6e208c44c5ff4b2f42e91d6c41fee2
Author: Stratos Karafotis <stratosk@semaphore.gr>
Date:   Thu Jul 3 06:28:22 2014 -0400

    cpufreq: Introduce new relation for freq selection Introduce CPUFREQ_RELATION_C for frequency selection. It selects the frequency with the minimum euclidean distance to target. In case of equal distance between 2 frequencies, it will select the greater freq.
    
    Signed-off-by: Stratos Karafotis <stratosk@semaphore.gr>
    
    Conflicts:
    	include/linux/cpufreq.h

commit 67026689228f6ca3ac5de82af2450d58760b7a58
Author: Stratos Karafotis <stratosk@semaphore.gr>
Date:   Thu Jul 3 06:31:21 2014 -0400

    Currently, ondemand calculates the target frequency proportional to load using the formula:
    
    Target frequency = C * load
    where C = policy->cpuinfo.max_freq / 100
    
    Though, in many cases, the minimum available frequency is pretty high
    and
    the above calculation introduces a dead band from load 0 to
    100 * policy->cpuinfo.min_freq / policy->cpuinfo.max_freq where the
    target
    frequency is always calculated to less than policy->cpuinfo.min_freq and
    the minimum frequency is selected.
    
    For example: on Intel i7-3770 @ 3.4GHz the policy->cpuinfo.min_freq =
    1600000
    and the policy->cpuinfo.max_freq = 3400000 (without turbo). Thus, the
    CPU
    starts to scale up at a load above 47.
    On quad core 1500MHz Krait the policy->cpuinfo.min_freq = 384000
    and the policy->cpuinfo.max_freq = 1512000. Thus, the CPU starts to
    scale
    at load above 25.
    
    Change the calculation of target frequency to eliminate the above
    effect using
    the formula:
    
    Target frequency = A + B * load
    where A = policy->cpuinfo.min_freq and
    B = (policy->cpuinfo.max_freq - policy->cpuinfo->min_freq) / 100
    
    This will map load values 0 to 100 linearly to cpuinfo.min_freq to
    cpuinfo.max_freq.
    
    Also, use the CPUFREQ_RELATION_C in __cpufreq_driver_target to select
    the
    closest frequency in frequency_table. This is necessary to avoid
    selection
    of minimum frequency only when load equals to 0. It will also help for
    selection
    of frequencies using a more 'fair' criterion.
    
    In tables below is presented the difference in selected frequency for
    specific
    values of load without and with this patch. On Intel i7-3770 @ 3.40GHz:
    Without			With
    Load	Target	Selected	Target	Selected
    0	0	1600000		1600000	1600000
    5	170050	1600000		1690050	1700000
    10	340100	1600000		1780100	1700000
    15	510150	1600000		1870150	1900000
    20	680200	1600000		1960200	2000000
    25	850250	1600000		2050250	2100000
    30	1020300	1600000		2140300	2100000
    35	1190350	1600000		2230350	2200000
    40	1360400	1600000		2320400	2400000
    45	1530450	1600000		2410450	2400000
    50	1700500	1900000		2500500	2500000
    55	1870550	1900000		2590550	2600000
    60	2040600	2100000		2680600	2600000
    65	2210650	2400000		2770650	2800000
    70	2380700	2400000		2860700	2800000
    75	2550750	2600000		2950750	3000000
    80	2720800	2800000		3040800	3000000
    85	2890850	2900000		3130850	3100000
    90	3060900	3100000		3220900	3300000
    95	3230950	3300000		3310950	3300000
    100	3401000	3401000		3401000	3401000
    
    On ARM quad core 1500MHz Krait:
    Without			With
    Load	Target	Selected	Target	Selected
    0	0	384000		384000	384000
    5	75600	384000		440400	486000
    10	151200	384000		496800	486000
    15	226800	384000		553200	594000
    20	302400	384000		609600	594000
    25	378000	384000		666000	702000
    30	453600	486000		722400	702000
    35	529200	594000		778800	810000
    40	604800	702000		835200	810000
    45	680400	702000		891600	918000
    50	756000	810000		948000	918000
    55	831600	918000		1004400	1026000
    60	907200	918000		1060800	1026000
    65	982800	1026000		1117200	1134000
    70	1058400	1134000		1173600	1134000
    75	1134000	1134000		1230000	1242000
    80	1209600	1242000		1286400	1242000
    85	1285200	1350000		1342800	1350000
    90	1360800	1458000		1399200	1350000
    95	1436400	1458000		1455600	1458000
    100	1512000	1512000		1512000	1512000
    
    Tested on Intel i7-3770 CPU @ 3.40GHz and on ARM quad core 1500MHz Krait
    (Android smartphone).
    
    Signed-off-by: Stratos Karafotis <stratosk@semaphore.gr>

commit 8cb8d9305f33f9d5edf9f7e6b71cf3450b991efb
Author: friedrich420 <kelpidorou@yahoo.com>
Date:   Fri Jan 30 13:41:08 2015 +0200

    Interactive Governor: Use CPUFREQ_RELATION_C

commit d6b41b79054236dad3ec81480d401e2841d4eea9
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Sun Jan 18 01:01:49 2015 -0500

    cpufreq: convert "index" to corresponding variable

commit ffb2738d9dbd196b8216fd9dd7f020eb6551f51b
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 22:25:55 2015 -0700

    cpufreq: ondemand: disable cpu-boost when switched to ondemand
    * ondemand and cpu-boost don't play nice together
    
    Thanks to imoseyon

commit 8464d85372d28ff00da37dd078e44457c7b92283
Author: franciscofranco <franciscofranco.1990@gmail.com>
Date:   Wed Oct 15 00:38:31 2014 +0000

    cpufreq: cpu-boost: we can hit a small performance loss by not queuing input works less than 150ms apart when our default input work duration is only 40ms, so use that 40ms as a magic value instead of the 150ms minimum interval.
    
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>

commit 4de3d09d575dbb97310429a1810511a67663fc43
Author: imoseyon <imoseyon@gmail.com>
Date:   Thu Jan 3 15:18:26 2013 -0800

    random: entropy tweaks are all the rage nowadays
    
    use non-blocking pool for all
    
    http://lwn.net/Articles/489734/
    
    Conflicts:
    
    	drivers/char/random.c
    
    Conflicts:
    	drivers/char/random.c

commit 94322488257e22cb1d981753437a491d89741ca3
Author: imoseyon <imoseyon@gmail.com>
Date:   Fri Jan 4 13:05:20 2013 -0800

    random: prevent add_input from doing anything

commit 11f89b34f0d6e21a6b628605dbef42c47340ce98
Author: imoseyon <imoseyon@gmail.com>
Date:   Sun Mar 17 17:53:33 2013 -0700

    random: remove warning

commit bd1f72e68b2a21302d5837cb42319ef1cfb38c03
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 22:32:44 2015 -0700

    mdss: expose panel on/off events as a global variable (Imoseyon)
    
        * to be used for my X governors

commit e8ed20ff9caa2498bf9b614ef01ccf3a1e4ab496
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 22:41:35 2015 -0700

    cpufreq: interactiveX V4: limit max freq when screen off (Imoseyon)
    
        * screen_off_max configurable via sysfs - default 2.27ghz

commit 2605d7a6a979d9ba5f19d63d48a47d57eb76c3c4
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 22:51:11 2015 -0700

    cpufreq: cpu-boost: allow enable/disable via sysfs

commit d38a85b3cc9b6e5d1a51a3027b86fda5844db050
Author: Hannes Frederic Sowa <hannes@stressinduktion.org>
Date:   Mon Nov 11 12:20:33 2013 +0100

    random32: add periodic reseeding
    
    The current Tausworthe PRNG is never reseeded with truly random data after
    the first attempt in late_initcall. As this PRNG is used for some critical
    random data as e.g. UDP port randomization we should try better and reseed
    the PRNG once in a while with truly random data from get_random_bytes().
    
    When we reseed with prandom_seed we now make also sure to throw the first
    output away. This suffices the reseeding procedure.
    
    The delay calculation is based on a proposal from Eric Dumazet.
    
    Joint work with Daniel Borkmann.
    
    Cc: Eric Dumazet <eric.dumazet@gmail.com>
    Cc: Theodore Ts'o <tytso@mit.edu>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 1cc643ee1f3b0b03c225a6f3c8348bf8dad24552
Author: Hannes Frederic Sowa <hannes@stressinduktion.org>
Date:   Mon Nov 11 12:20:34 2013 +0100

    random32: add prandom_reseed_late() and call when nonblocking pool becomes initialized
    
    The Tausworthe PRNG is initialized at late_initcall time. At that time the
    entropy pool serving get_random_bytes is not filled sufficiently. This
    patch adds an additional reseeding step as soon as the nonblocking pool
    gets marked as initialized.
    
    On some machines it might be possible that late_initcall gets called after
    the pool has been initialized. In this situation we won't reseed again.
    
    (A call to prandom_seed_late blocks later invocations of early reseed
    attempts.)
    
    Joint work with Daniel Borkmann.
    
    Cc: Eric Dumazet <eric.dumazet@gmail.com>
    Cc: Theodore Ts'o <tytso@mit.edu>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Acked-by: "Theodore Ts'o" <tytso@mit.edu>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit dd1f06d51f6fa760d46270d35cd7634b829ae742
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Mon Nov 11 12:20:35 2013 +0100

    random32: move rnd_state to linux/random.h
    
    struct rnd_state got mistakenly pulled into uapi header. It is not
    used anywhere and does also not belong there!
    
    Commit 5960164fde ("lib/random32: export pseudo-random number
    generator for modules"), the last commit on rnd_state before it
    got moved to uapi, says:
    
      This patch moves the definition of struct rnd_state and the inline
      __seed() function to linux/random.h.  It renames the static __random32()
      function to prandom32() and exports it for use in modules.
    
    Hence, the structure was moved from lib/random32.c to linux/random.h
    so that it can be used within modules (FCoE-related code in this
    case), but not from user space. However, it seems to have been
    mistakenly moved to uapi header through the uapi script. Since no-one
    should make use of it from the linux headers, move the structure back
    to the kernel for internal use, so that it can be modified on demand.
    
    Joint work with Hannes Frederic Sowa.
    
    Cc: Joe Eykholt <jeykholt@cisco.com>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 72a2b40e472e69475d09e417b2a71eb28e59da04
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Mon Nov 11 12:20:36 2013 +0100

    random32: upgrade taus88 generator to taus113 from errata paper
    
    Since we use prandom*() functions quite often in networking code
    i.e. in UDP port selection, netfilter code, etc, upgrade the PRNG
    from Pierre L'Ecuyer's original paper "Maximally Equidistributed
    Combined Tausworthe Generators", Mathematics of Computation, 65,
    213 (1996), 203--213 to the version published in his errata paper [1].
    
    The Tausworthe generator is a maximally-equidistributed generator,
    that is fast and has good statistical properties [1].
    
    The version presented there upgrades the 3 state LFSR to a 4 state
    LFSR with increased periodicity from about 2^88 to 2^113. The
    algorithm is presented in [1] by the very same author who also
    designed the original algorithm in [2].
    
    Also, by increasing the state, we make it a bit harder for attackers
    to "guess" the PRNGs internal state. See also discussion in [3].
    
    Now, as we use this sort of weak initialization discussed in [3]
    only between core_initcall() until late_initcall() time [*] for
    prandom32*() users, namely in prandom_init(), it is less relevant
    from late_initcall() onwards as we overwrite seeds through
    prandom_reseed() anyways with a seed source of higher entropy, that
    is, get_random_bytes(). In other words, a exhaustive keysearch of
    96 bit would be needed. Now, with the help of this patch, this
    state-search increases further to 128 bit. Initialization needs
    to make sure that s1 > 1, s2 > 7, s3 > 15, s4 > 127.
    
    taus88 and taus113 algorithm is also part of GSL. I added a test
    case in the next patch to verify internal behaviour of this patch
    with GSL and ran tests with the dieharder 3.31.1 RNG test suite:
    
    $ dieharder -g 052 -a -m 10 -s 1 -S 4137730333 #taus88
    $ dieharder -g 054 -a -m 10 -s 1 -S 4137730333 #taus113
    
    With this seed configuration, in order to compare both, we get
    the following differences:
    
    algorithm                 taus88           taus113
    rands/second [**]         1.61e+08         1.37e+08
    sts_serial(4, 1st run)    WEAK             PASSED
    sts_serial(9, 2nd run)    WEAK             PASSED
    rgb_lagged_sum(31)        WEAK             PASSED
    
    We took out diehard_sums test as according to the authors it is
    considered broken and unusable [4]. Despite that and the slight
    decrease in performance (which is acceptable), taus113 here passes
    all 113 tests (only rgb_minimum_distance_5 in WEAK, the rest PASSED).
    In general, taus/taus113 is considered "very good" by the authors
    of dieharder [5].
    
    The papers [1][2] states a single warm-up step is sufficient by
    running quicktaus once on each state to ensure proper initialization
    of ~s_{0}:
    
    Our selection of (s) according to Table 1 of [1] row 1 holds the
    condition L - k <= r - s, that is,
    
      (32 32 32 32) - (31 29 28 25) <= (25 27 15 22) - (18 2 7 13)
    
    with r = k - q and q = (6 2 13 3) as also stated by the paper.
    So according to [2] we are safe with one round of quicktaus for
    initialization. However we decided to include the warm-up phase
    of the PRNG as done in GSL in every case as a safety net. We also
    use the warm up phase to make the output of the RNG easier to
    verify by the GSL output.
    
    In prandom_init(), we also mix random_get_entropy() into it, just
    like drivers/char/random.c does it, jiffies ^ random_get_entropy().
    random-get_entropy() is get_cycles(). xor is entropy preserving so
    it is fine if it is not implemented by some architectures.
    
    Note, this PRNG is *not* used for cryptography in the kernel, but
    rather as a fast PRNG for various randomizations i.e. in the
    networking code, or elsewhere for debugging purposes, for example.
    
    [*]: In order to generate some "sort of pseduo-randomness", since
    get_random_bytes() is not yet available for us, we use jiffies and
    initialize states s1 - s3 with a simple linear congruential generator
    (LCG), that is x <- x * 69069; and derive s2, s3, from the 32bit
    initialization from s1. So the above quote from [3] accounts only
    for the time from core to late initcall, not afterwards.
    [**] Single threaded run on MacBook Air w/ Intel Core i5-3317U
    
     [1] http://www.iro.umontreal.ca/~lecuyer/myftp/papers/tausme2.ps
     [2] http://www.iro.umontreal.ca/~lecuyer/myftp/papers/tausme.ps
     [3] http://thread.gmane.org/gmane.comp.encryption.general/12103/
     [4] http://code.google.com/p/dieharder/source/browse/trunk/libdieharder/diehard_sums.c?spec=svn490&r=490#20
     [5] http://www.phy.duke.edu/~rgb/General/dieharder.php
    
    Joint work with Hannes Frederic Sowa.
    
    Cc: Florian Weimer <fweimer@redhat.com>
    Cc: Theodore Ts'o <tytso@mit.edu>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit b19f89d6cdf6cf41aff134f9f020b576622d6b87
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Mon Nov 11 12:20:37 2013 +0100

    random32: add test cases for taus113 implementation
    
    We generated a battery of 100 test cases from GSL taus113 implemention
    and compare the results from a particular seed and a particular
    iteration with our implementation in the kernel. We have verified on
    32 and 64 bit machines that our taus113 kernel implementation gives
    same results as GSL taus113 implementation:
    
      [    0.147370] prandom: seed boundary self test passed
      [    0.148078] prandom: 100 self tests passed
    
    This is a Kconfig option that is disabled on default, just like the
    crc32 init selftests in order to not unnecessary slow down boot process.
    We also refactored out prandom_seed_very_weak() as it's now used in
    multiple places in order to reduce redundant code.
    
    GSL code we used for generating test cases:
    
      int i, j;
      srand(time(NULL));
      for (i = 0; i < 100; ++i) {
        int iteration = 500 + (rand() % 500);
        gsl_rng_default_seed = rand() + 1;
        gsl_rng *r = gsl_rng_alloc(gsl_rng_taus113);
        printf("\t{ %lu, ", gsl_rng_default_seed);
        for (j = 0; j < iteration - 1; ++j)
          gsl_rng_get(r);
        printf("%u, %lu },\n", iteration, gsl_rng_get(r));
        gsl_rng_free(r);
      }
    
    Joint work with Hannes Frederic Sowa.
    
    Cc: Florian Weimer <fweimer@redhat.com>
    Cc: Theodore Ts'o <tytso@mit.edu>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 43687b6387c104c64a6288b194af56ed2f01ace4
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Tue Nov 12 23:45:41 2013 +0100

    random32: add __init prefix to prandom_start_seed_timer
    
    We only call that in functions annotated with __init, so add __init
    prefix in prandom_start_seed_timer() as well, so that the kernel can
    make use of this hint and we can possibly free up resources after it's
    usage. And since it's an internal function rename it to
    __prandom_start_seed_timer().
    
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit eb6f7783226af8f01f83e3e762862124d172d34a
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Tue Nov 12 23:45:42 2013 +0100

    random32: use msecs_to_jiffies for reseed timer
    
    Use msecs_to_jiffies, for these calculations as different HZ
    considerations are taken into account for conversion of the timer
    shot, and also it makes the code more readable.
    
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit bd1358c87decb3ad2eab5e5b41a0f4fdbc47ad0b
Author: Sasha Levin <sasha.levin@oracle.com>
Date:   Fri Mar 28 17:38:42 2014 +0100

    random32: avoid attempt to late reseed if in the middle of seeding
    
    Commit 4af712e8df ("random32: add prandom_reseed_late() and call when
    nonblocking pool becomes initialized") has added a late reseed stage
    that happens as soon as the nonblocking pool is marked as initialized.
    
    This fails in the case that the nonblocking pool gets initialized
    during __prandom_reseed()'s call to get_random_bytes(). In that case
    we'd double back into __prandom_reseed() in an attempt to do a late
    reseed - deadlocking on 'lock' early on in the boot process.
    
    Instead, just avoid even waiting to do a reseed if a reseed is already
    occuring.
    
    Fixes: 4af712e8df99 ("random32: add prandom_reseed_late() and call when nonblocking pool becomes initialized")
    Signed-off-by: Sasha Levin <sasha.levin@oracle.com>
    Acked-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 9e82f8d4c880cba075895d44a66746a392b28f2f
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Thu Apr 3 14:49:08 2014 -0700

    lib/random32.c: minor cleanups and kdoc fix
    
    These are just some very minor and misc cleanups in the PRNG.  In
    prandom_u32() we store the result in an unsigned long which is
    unnecessary as it should be u32 instead that we get from
    prandom_u32_state().  prandom_bytes_state()'s comment is in kdoc format,
    so change it into such as it's done everywhere else.  Also, use the
    normal comment style for the header comment.  Last but not least for
    readability, add some newlines.
    
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Cc: Joe Perches <joe@perches.com>
    Signed-off-by: Andrew Morton <akpm@linux-foundation.org>
    Signed-off-by: Linus Torvalds <torvalds@linux-foundation.org>

commit bacc848ba8d658cd0836dbaf24213d1292a8ded6
Author: Hannes Frederic Sowa <hannes@stressinduktion.org>
Date:   Mon Jul 28 14:01:38 2014 +0200

    random32: mix in entropy from core to late initcall
    
    Currently, we have a 3-stage seeding process in prandom():
    
    Phase 1 is from the early actual initialization of prandom()
    subsystem which happens during core_initcall() and remains
    most likely until the beginning of late_initcall() phase.
    Here, the system might not have enough entropy available
    for seeding with strong randomness from the random driver.
    That means, we currently have a 32bit weak LCG() seeding
    the PRNG status register 1 and mixing that successively
    into the other 3 registers just to get it up and running.
    
    Phase 2 starts with late_initcall() phase resp. when the
    random driver has initialized its non-blocking pool with
    enough entropy. At that time, we throw away *all* inner
    state from its 4 registers and do a full reseed with strong
    randomness.
    
    Phase 3 starts right after that and does a periodic reseed
    with random slack of status register 1 by a strong random
    source again.
    
    A problem in phase 1 is that during bootup data structures
    can be initialized, e.g. on module load time, and thus access
    a weakly seeded prandom and are never changed for the rest
    of their live-time, thus carrying along the results from a
    week seed. Lets make sure that current but also future users
    access a possibly better early seeded prandom.
    
    This patch therefore improves phase 1 by trying to make it
    more 'unpredictable' through mixing in seed from a possible
    hardware source. Now, the mix-in xors inner state with the
    outcome of either of the two functions arch_get_random_{,seed}_int(),
    preferably arch_get_random_seed_int() as it likely represents
    a non-deterministic random bit generator in hw rather than
    a cryptographically secure PRNG in hw. However, not all might
    have the first one, so we use the PRNG as a fallback if
    available. As we xor the seed into the current state, the
    worst case would be that a hardware source could be unverifiable
    compromised or backdoored. In that case nevertheless it
    would be as good as our original early seeding function
    prandom_seed_very_weak() since we mix through xor which is
    entropy preserving.
    
    Joint work with Daniel Borkmann.
    
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 7af2bbadfbda68f43c910890418925f93e7678e7
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Sat Aug 23 17:03:28 2014 +0200

    random32: improvements to prandom_bytes
    
    This patch addresses a couple of minor items, mostly addesssing
    prandom_bytes(): 1) prandom_bytes{,_state}() should use size_t
    for length arguments, 2) We can use put_unaligned() when filling
    the array instead of open coding it [ perhaps some archs will
    further benefit from their own arch specific implementation when
    GCC cannot make up for it ], 3) Fix a typo, 4) Better use unsigned
    int as type for getting the arch seed, 5) Make use of
    prandom_u32_max() for timer slack.
    
    Regarding the change to put_unaligned(), callers of prandom_bytes()
    which internally invoke prandom_bytes_state(), don't bother as
    they expect the array to be filled randomly and don't have any
    control of the internal state what-so-ever (that's also why we
    have periodic reseeding there, etc), so they really don't care.
    
    Now for the direct callers of prandom_bytes_state(), which
    are solely located in test cases for MTD devices, that is,
    drivers/mtd/tests/{oobtest.c,pagetest.c,subpagetest.c}:
    
    These tests basically fill a test write-vector through
    prandom_bytes_state() with an a-priori defined seed each time
    and write that to a MTD device. Later on, they set up a read-vector
    and read back that blocks from the device. So in the verification
    phase, the write-vector is being re-setup [ so same seed and
    prandom_bytes_state() called ], and then memcmp()'ed against the
    read-vector to check if the data is the same.
    
    Akinobu, Lothar and I also tested this patch and it runs through
    the 3 relevant MTD test cases w/o any errors on the nandsim device
    (simulator for MTD devs) for x86_64, ppc64, ARM (i.MX28, i.MX53
    and i.MX6):
    
      # modprobe nandsim first_id_byte=0x20 second_id_byte=0xac \
                         third_id_byte=0x00 fourth_id_byte=0x15
      # modprobe mtd_oobtest dev=0
      # modprobe mtd_pagetest dev=0
      # modprobe mtd_subpagetest dev=0
    
    We also don't have any users depending directly on a particular
    result of the PRNG (except the PRNG self-test itself), and that's
    just fine as it e.g. allowed us easily to do things like upgrading
    from taus88 to taus113.
    
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Tested-by: Akinobu Mita <akinobu.mita@gmail.com>
    Tested-by: Lothar Waßmann <LW@KARO-electronics.de>
    Cc: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: David S. Miller <davem@davemloft.net>

commit 2b8b7d0dd2dad846df41b806b6d6d6bb7fe5e06e
Author: Daniel Borkmann <dborkman@redhat.com>
Date:   Wed Jan 22 02:29:39 2014 +0100

    random32: add prandom_u32_max and convert open coded users
    
    Many functions have open coded a function that returns a random
    number in range [0,N-1]. Under the assumption that we have a PRNG
    such as taus113 with being well distributed in [0, ~0U] space,
    we can implement such a function as uword t = (n*m')>>32, where
    m' is a random number obtained from PRNG, n the right open interval
    border and t our resulting random number, with n,m',t in u32 universe.
    
    Lets go with Joe and simply call it prandom_u32_max(), although
    technically we have an right open interval endpoint, but that we
    have documented. Other users can further be migrated to the new
    prandom_u32_max() function later on; for now, we need to make sure
    to migrate reciprocal_divide() users for the reciprocal_divide()
    follow-up fixup since their function signatures are going to change.
    
    Joint work with Hannes Frederic Sowa.
    
    Cc: Jakub Zawadzki <darkjames-ws@darkjames.pl>
    Cc: Eric Dumazet <eric.dumazet@gmail.com>
    Cc: linux-kernel@vger.kernel.org
    Signed-off-by: Hannes Frederic Sowa <hannes@stressinduktion.org>
    Signed-off-by: Daniel Borkmann <dborkman@redhat.com>
    Signed-off-by: David S. Miller <davem@davemloft.net>
    
    Conflicts:
    	net/packet/af_packet.c

commit 73388caec760bc1e11317ebb5677f94c8817cf4b
Author: Theodore Ts'o <tytso@mit.edu>
Date:   Sat Sep 21 13:58:22 2013 -0400

    random: allow architectures to optionally define random_get_entropy()
    
    Allow architectures which have a disabled get_cycles() function to
    provide a random_get_entropy() function which provides a fine-grained,
    rapidly changing counter that can be used by the /dev/random driver.
    
    For example, an architecture might have a rapidly changing register
    used to control random TLB cache eviction, or DRAM refresh that
    doesn't meet the requirements of get_cycles(), but which is good
    enough for the needs of the random driver.
    
    Signed-off-by: "Theodore Ts'o" <tytso@mit.edu>
    Cc: stable@vger.kernel.org

commit b1f8885d80d1456c2c7d8274e4b8e7524b3273b6
Author: imoseyon <imoseyon@gmail.com>
Date:   Sat Dec 13 16:39:49 2014 -0800

    random32: use e/frandom for reseeding, and a merge fixup

commit 3279f713ddfec7c8965006694be23e8f14be7e67
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 00:50:51 2015 -0700

    binfmt_elf: use prandom - do not deplete entropy

commit 4e4111ce7f01f0389e1921cfcb2f7abb29172ddf
Author: imoseyon <imoseyon@gmail.com>
Date:   Sat Dec 13 16:47:03 2014 -0800

    fs: ext4: use e/frandom, do not deplete entropy

commit c325ad57ce89dc7a57aef276fe22e1610f7c2d66
Author: imoseyon <imoseyon@gmail.com>
Date:   Sat Dec 13 16:53:13 2014 -0800

    random.h: declare erandom function

commit 97ee2f3c24fcc6f1326fe0fb0a39ee40b171fb57
Author: imoseyon <imoseyon@gmail.com>
Date:   Sat Dec 13 16:53:42 2014 -0800

    net/packet: merge fix

commit aaf08b1315d53bdfdec5dbdadbd06a6e1fef29c7
Author: imoseyon <imoseyon@gmail.com>
Date:   Sun Dec 14 10:36:51 2014 -0800

    random: sprinkle e/f/prandom in places that deplete entropy often

commit 0ee23d2a63bd75ca908347808cea6de91c94ccac
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 16:39:24 2015 -0700

    base kernel v.05

commit c72ab9dc97103bf3e3f5341fe6df68eb7606c697
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 17:25:01 2015 -0700

    update defconfig

commit 57e8cfeb533977bcdb580640f6fae8a178c40b7f
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 22:46:48 2015 -0700

    msm cpu frequency limit (faux123)

commit 088ba7983b461fc154891b67bae97acbdfc20a86
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 00:39:00 2015 -0700

    intelli-thermal v2: initial adaptation (faux123)
    
    Intellithermal 2.0 is based on the latest Qualcomm thermal driver
    adapted for
    in-kernel use and control.  Newer MSM8974+ chipsets should use this
    driver
    going forward

commit 2735862f4a11f44d71e0fdea4d46c1f005850521
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 11:36:09 2015 -0700

    Revert: Lower GPU voltage constraint
    
    Signed-off-by: flar2 <asegaert@gmail.com> (reverted from commit 564caaaa8c213fc6fdf49483dd5c115db93b733c)

commit ea2c9eefdc7d8f230268451af43bf9ab0ecded57
Author: TwistedUmbrella <twistedumbrella@gmail.com>
Date:   Tue Nov 4 13:17:14 2014 -0500

    cpufreq: Initial setup for new gov [Umbrella Core] (TwistedUmbella)

commit f86c87affdf4f4df7a2a540efbfbde64e344b3bc
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 20:19:00 2015 -0700

    ElementalX governor (flar2)
    
    elementalx governor: disable cpuboost

commit fdf4d9e9d92698d1de0e902ef5fe951bffc3f290
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 20:25:19 2015 -0700

    add Led Control
    
    Thanks to Twistedumbrella and Ktoonsez
    
    Conflicts:
    
    	drivers/leds/leds-max77843-rgb.c

commit 584d4a1916d44452d281ed1d23e7f5f4446d2d80
Author: Pavel <nadyaivanova14@gmail.com>
Date:   Tue Dec 30 20:41:58 2014 +0100

    include: linux: add Sysfs_helpers: Allow negative values

commit a197344e99cb641da6832eb54e45a0d61e4f62af
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 19:32:35 2015 -0700

    update shamu interactive governor

commit 719c1d0c6e16b0ee2f88ec3e3ae22e91b79c3fde
Author: franciscofranco <franciscofranco.1990@gmail.com>
Date:   Mon Dec 29 01:57:37 2014 +0000

    msm: thermal: add a module param to change the thermal throttle temperature point to userspace
    
    Signed-off-by: franciscofranco <franciscofranco.1990@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 1dbe5610c3bdc64a789a4694077f68e82f4b73c9
Author: myfluxi <linflux@arcor.de>
Date:   Wed Jan 1 11:31:16 2014 +0100

    msm: kgsl: Report correct GPU frequency in sysfs
    
    Change-Id: I1aac90d0554b9de0511ffb78042177a5a23855ce
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 9eb04bf27585503a17da4cbcb31efd8e5bf0fc59
Author: myfluxi <linflux@arcor.de>
Date:   Wed Jan 8 01:25:14 2014 +0100

    PM: devfreq: Use high priority workqueue
    
    It does not make sense to run kgsl on high and devfreq on regular
    priority.
    
    Change-Id: Ie5e6c9353a4e1324a6a49278e5ad3638462f551c
    
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 3dabc288c75e77c5261bab229d638ac7a91f6eab
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 11:48:48 2015 -0700

    block: cgroups, kconfig, build bits for BFQ-v7r6-3.10.8+
    
    Update Kconfig.iosched and do the related Makefile changes to include
    kernel configuration options for BFQ. Also add the bfqio controller
    to the cgroups subsystem.
    
    Signed-off-by: Paolo Valente <paolo.valente@unimore.it>
    Signed-off-by: Arianna Avanzini <avanzini.arianna@gmail.com>
    Signed-off-by: flar2 <asegaert@gmail.com>

commit 6b5bf205f46a8e67129342be572b1782e58e76cb
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

commit 9ea62b2c08144842a97b95a177557c3711dfd9e1
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

commit 3c89a7a86eb5f7fafcd4ca8bd28af8e8b79ebd08
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 20:56:07 2015 -0700

    Added sio, fifo, vr and zen I/O schedulers

commit 50c980376009f4657636f5177edeefb40ff99613
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 18:27:12 2015 -0700

    base CMRemix v1.2

project packages/apps/AudioFX/
commit 4f0eb650bdee6bcf6c479caa8eb8f998d38a2602
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:29 2015 +0200

    Automatic translation import
    
    Change-Id: Id5896de688909e7c308c741a1f7966292483edf4

project packages/apps/Bluetooth/
commit 9a70af67161ed2fd6b44d8c0519093ace90759a6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:35 2015 +0200

    Automatic translation import
    
    Change-Id: Ie2675992cd5ba2d38202e46c658667e79837516e

project packages/apps/BluetoothExt/
commit 31c24878e779fcac76a946fbdf2bc75cece88ee8
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:39 2015 +0200

    Automatic translation import
    
    Change-Id: I0dbd3486f50f9c10cc9af3ea0b2dc353efa5d34b

project packages/apps/Browser/
commit 5660167cfd9d3469d7b038f2c59d5caccf164841
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Wed Mar 11 00:30:27 2015 +0100

    browser: set security state even if user disable security alerts
    
    Even if a user disabled the security alerts (ssl errors), the security state
     SHOULD be set to shown that the certificate
    has a problem. Actually, the certificate is reported as valid, which is
     complety wrong.
    
    Change-Id: I9d8647f2a6dba2b9387b240b5511df18e1b4ea22
    JIRA: NIGHTLIES-813
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

project packages/apps/CMFileManager/
commit a0e7ac5f1eae637aa0fd23a0d2ce3cd90d42d73a
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Mar 11 16:01:01 2015 -0700

    CMFileManager: Fix back press events
    Use onBackPressed in stead of onKeyUp for back press events
    
    Repro:
    - Navigate to audio file
    - Open audio file with small player (e.g. Play Music)
    - Press back
    - Observe: audio player closes and CMFM navigates up one directory
    
    Change-Id: Ia7440c45241ec957b2405b932525235c92b9211c

commit 9cc59b6ac5ac3d6531ebf477b359b7b49342d478
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:15 2015 +0200

    Automatic translation import
    
    Change-Id: I1e77140dc7177e10bc98fcbdfe2110f6dc96a9d6

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

project packages/apps/Calculator/
commit 461eb696515358867bec10caf1614520663039d7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:44 2015 +0200

    Automatic translation import
    
    Change-Id: Iea408b84d3ac9048ae0a9890ead56d8b270ef500

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
commit e0a097b5c04567eb7914614a69638fa5e324f21d
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Mar 11 18:04:08 2015 -0700

    Calendar: add feature to select/deselect all events in delete view
    
    Change-Id: I1301d921474d848d6c877eb904bd7a00df13c48a

commit 1f28924c571f7b14ed2aef9200d6b6ae26bd7170
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:49 2015 +0200

    Automatic translation import
    
    Change-Id: I7890752036c3f6c12cf897c855303e39c8f162f9

commit 8d3bd6c49994cb27cb65e8622cc1db2aa4a1cf15
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 13 16:53:39 2015 -0700

    Calendar: support ACTION_VIEW instead of ACTION_SEND
    
    Change-Id: I9b7608a9161b1370a4ee4ab520c0e0e9a0fd9c9c

project packages/apps/Camera2/
commit 1d98281c19d314da039c0d1e987c254b27269ad0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:55 2015 +0200

    Automatic translation import
    
    Change-Id: Ic0ffbc7f6a7198ea341425c966fc238d42721058

commit 982bcc197bc6c035c2efc283a033d6bab5cf86d7
Merge: b656f91 1d98281
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:08:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/CellBroadcastReceiver/
commit c3ea6b5a6372e3bfb402dcf452eb89d28fb119ac
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:00 2015 +0200

    Automatic translation import
    
    Change-Id: I12ec8301573c3bdf604571ea33d90f5e496dd1dd

project packages/apps/Contacts/
commit 5231670251788a04d43cfe0ac3d8107cddbb5fb1
Author: Marcos Marado <mmarado@cyngn.com>
Date:   Wed Mar 11 16:25:28 2015 +0000

    Fix the event name
    
    This isn't very important ATM because we don't have the corresponding patch on
    ContactsCommon/src/com/android/contacts/common/interactions/ImportExportDialogFragment.java
    , so we'll never get an SUBACTIVITY_SHARE_VISIBLE_CONTACTS anyway.
    
    Change-Id: I9b55baad3e898471edf2acb3219e22f2199cebf1

commit 617bb3b76d8b5d2f0c080973f2a3cb9699364bb7
Author: Ethan Chen <intervigil@gmail.com>
Date:   Thu Mar 12 00:02:43 2015 +0000

    Revert "Fix the event name"
    
    This reverts commit 5231670251788a04d43cfe0ac3d8107cddbb5fb1.
    
    Change-Id: I4bf15a61507192a16a6b32e5d5d2e10e085689b7

commit a5a544f00da0b5b32ecc49b9baef46125de3b9aa
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:27 2015 +0200

    Automatic translation import
    
    Change-Id: Id2dc16829a8d9b7a3ecd5fe92a3cc0e25df7df62

project packages/apps/ContactsCommon/
commit 0d2ed5aa12839d3fc15ac9c769b28f564da53df7
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 10 10:08:23 2015 -0700

    ContactsCommon: fix FC when deleting SIM contacts after SIM is removed
    
    Repro:
     - Create local contact
     - Export to SIM
     - Remove SIM
     - Go to delete menu option
     - Select all (*include* exported SIM contact)
     - Click check mark
     - Observe Contacts app force closes when deleting the exported contact
    
    Change-Id: I2bfecf8b19c8f1eae9559a4e6f46ff477da4dc74

commit f08e8aa7a5a2c0e666581d6a8d22f4d397663769
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:33 2015 +0200

    Automatic translation import
    
    Change-Id: Ife47fda96ea9abefed27530a75dd084f2ccd34c2

project packages/apps/DeskClock/
commit 01a192a14355dce7ccc5a8540bb5de72aa4e3715
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:37 2015 +0200

    Automatic translation import
    
    Change-Id: I213fee9f3009771a35b5a48c3ea4037b167b07df

project packages/apps/Dialer/
commit 475a7e9cdefec248fe153ebd8afe8dfd6c90b29d
Author: cretin45 <cretin45@gmail.com>
Date:   Thu Mar 12 16:06:25 2015 -0700

    Dialer: Add call waiting vibrate option
    
    Change-Id: Id903310aa0ef74fe01349e39262159e4795f4501

commit b7cad7e94f8d1d256b8ffac1fbbb0ba5eae32f01
Merge: edd47fa 475a7e9
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 20:49:07 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

commit c44882cd616c61f5e3b817868768d4189216ed46
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:43 2015 +0200

    Automatic translation import
    
    Change-Id: I6a5b8697def638849ae9f1179f4e048228980097

commit 0ad236d3698b530f4f24cb08aeb2d77286761bfe
Merge: b7cad7e c44882c
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:08:43 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

project packages/apps/Eleven/
commit 1acc38bf8a57600f3bea031e39ea37a668c3912a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:49 2015 +0200

    Automatic translation import
    
    Change-Id: I706ba0b421b725967fca66376be10a6a4027e4f1

project packages/apps/Gallery2/
commit 7911e6b5c730f04684cc7f790095a976783fe06b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:54 2015 +0200

    Automatic translation import
    
    Change-Id: Ib1edaf2f04c5cec7840daa33701ca2dffb4d7226

commit d9001389537cca3481258144a543b9f3cb887bac
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Sun Feb 8 06:49:41 2015 +0000

    Moar materialize changes
    
    Change-Id: I2a4987c1220dfb772289c6638648702d26600aa7

project packages/apps/InCallUI/
commit d168c02c45928bf8e000ca5c98e2ead0e64fd8d1
Merge: e698a1d 967f67c
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:50:09 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 4743d756bfa24a9a6df3f85ca5602825b4d08c11
Author: cretin45 <cretin45@gmail.com>
Date:   Thu Mar 12 16:07:55 2015 -0700

    InCallUI: Bring back vibrate on call waiting
    
    Change-Id: I38f1d80ce4d29195b75df85b0fd0ab03371fbb5d

commit e4ef21b11c8b0ca2aac8c189fd997ccfb13412cc
Merge: d168c02 4743d75
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 20:50:01 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit f815c10e8cdbdc7a2bae6b4bbfff976ff2a9be6c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:59 2015 +0200

    Automatic translation import
    
    Change-Id: Ic5d377bbc6c1a95fb173673a54f50ee0795cf16f

commit e8c68fc828310532faf6b1921723bfacd1364c55
Merge: e4ef21b f815c10
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:09:32 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/apps/LockClock/
commit f1da736e118eb3d4160170c4ae572174186961b2
Author: Scott Mertz <scott@cyngn.com>
Date:   Tue Mar 10 16:42:55 2015 -0700

    LockClock: Ignore "inaccurate" locations
    
    - Location manager can report locations for any level of accuracy.  Filter
      locations that are generally not useful.
    - Set location accuracy threshold to 50km.
    
    Change-Id: I225ed4e74edec6c5089d886c61f8d78f09b11b34

commit 500804d7530802f34b21d1e230b207efedc7d56b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Wed Jan 15 22:11:47 2014 +0200

    cLock: Add to launcher
    
    Change-Id: I3f07657de97ab458390c8a98a46d4f8473c93ebd

commit 9e90260ff7deb9a6eeade93f487bdd18eb68fb10
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:05 2015 +0200

    Automatic translation import
    
    Change-Id: I1c97c5a6355c325f24b67cc9bdd9e9b3d588d8ab

project packages/apps/Mms/
commit ae6c7d64eda35437465acd104fba588cf4a7425e
Author: Marcos Marado <mmarado@cyngn.com>
Date:   Wed Mar 11 21:49:43 2015 +0000

    Mms: better vCard parser (getExtraSrc)
    
    We are now able to deal with
     * multiple contact vCards
     * single-contact vCard when the contact is unnamed
    
    Change-Id: I10f77441cad5d79406e7641f14bf92e4a3b34e1a
    (cherry picked from commit e6911a74aca8a78212243bea0dc4a05245339d27)

commit a983fbb0b2029fce5dba267cda477741e2532ab2
Merge: 703584b ae6c7d6
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 20:50:33 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

commit 271c955a923f7aa23245602ba8250afada29e530
Author: Dave Daynard <nardholio@gmail.com>
Date:   Mon Mar 9 20:24:03 2015 -0400

    Remove vibrate pattern on devices without vibrator
    
    Change-Id: I874a411a34eb2cfd388a2f15d513e29c4278ca54

commit 2dae5c2294f97e9dd148dab4cb3e25386536b398
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:10 2015 +0200

    Automatic translation import
    
    Change-Id: Ia1fd313e4d527f440b46f42838e68287d317215b

commit 593c82412cb8dff694b2367f92f656fe458fea31
Merge: a983fbb 2dae5c2
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:10:04 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0-2

project packages/apps/OmniSwitch/
commit d50ea730e2c850e396e21d08b703892ef714309e
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Mar 12 01:47:27 2015 +0100

    OmniSwitch: updates
    
    -time based filtering prework - inspired from Chainfire :)
    -added support for VectorDrawables
    -fix kill all
    -fix icon pack support
    
    Change-Id: Ie2ccc796204ab2eb3be5230d2ab64b3c97dd0c07

commit 05f56dac7931b1885a6f4d1e280c314fcd9e8f97
Merge: 7f2ff21 d50ea73
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Mar 16 22:27:47 2015 -0700

    Merge remote-tracking branch 'upstream/android-5.0' into cm-12.0

project packages/apps/PhoneCommon/
commit 0437e2cb60a677c0f64ddabd47ea5499df7ee955
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:18 2015 +0200

    Automatic translation import
    
    Change-Id: I3f164e5d4df8d3c92debf2878132f5f42649f2fd

project packages/apps/Settings/
commit 6d3a7e5f61c0d9cda9ed60624b2c6ee38fbe4fef
Author: Steve Kondik <steve@cyngn.com>
Date:   Mon Mar 9 16:05:32 2015 +0000

    settings: Use consistent headers for Privacy Guard
    
     * Show "Privacy Guard" instead of "App ops" in advanced settings
    
    Change-Id: I98107ba3ad94ba22bbd4dc9e92ea97a36f664ab8

commit 573c3dff7d21d6006a2aa8e4c097efab8c90112a
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 10 15:56:11 2015 -0700

    Settings: add summary for advanced mode
    
    Change-Id: Iff8a319fdde116119992c2a865fd6909712ca530
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit d2668957dea01f9d986e3e0814d5bf725a01e643
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 10 21:40:50 2015 -0700

    Settings: allow lock screen visualizer to be disabled
    
    Change-Id: Id1d77960c3e0d46ae8d69d1447c5c5d422754c4d
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Conflicts:
    	res/xml/security_settings_chooser.xml
    	res/xml/security_settings_lockscreen.xml
    	res/xml/security_settings_password.xml
    	res/xml/security_settings_pattern.xml
    	res/xml/security_settings_pin.xml
    
    Conflicts:
    	res/xml/security_settings_pattern.xml
    	res/xml/security_settings_pin.xml

commit 291ded8c3c188d9959b70620f08644758a86c5d2
Author: LorDClockaN <davor@losinj.com>
Date:   Tue Mar 10 17:48:08 2015 +0100

    Settings: Dotted circle battery (2/2)
    
    Change-Id: I025ba037143fcdfff99acd955532e34a3befd944

commit 54eacc2860c0e5967d168e1617fdd62022982b91
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Wed Mar 11 22:15:15 2015 -0700

    settings: prevent NPE in DisplaySettings
    
    Change-Id: If70f000bebfc7d072d060d71ee43e6b843167272
    JIRA: NIGHTLIES-830
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>
    
    Conflicts:
    	src/com/android/settings/DisplaySettings.java

commit 5aa25474b8e4c917c86c2a16bfdb8af2856cf8c5
Author: Steve Kondik <steve@cyngn.com>
Date:   Mon Mar 9 00:39:26 2015 +0100

    livedisplay: Add an "off" state
    
     * Don't force "day" to be the default state.
     * Change minimum value for color calibration to 20% so blackout doesn't
       happen when all sliders are at minimum.
     * Also improve a few strings to describe what day and night means.
    
    Change-Id: Ib2a617488fffb128c8e3e9e52d64fac6b261e53d

commit e7f862d3f4003f828f2ae2f32de6a778766c6121
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 2 20:51:17 2015 -0800

    Settings: Fix factory reset lock confirmation header text
    
    Repro:
     - Set password lock on device
     - Go Factory data reset option in Backup & reset
     - Click reset phone
     - Observe that the header asks to insert pattern
    
    Change-Id: I37c04293452adba446f4b5074f4a3434a57c74f7

commit 3792159ab5a3122af608adfdb0f5dd666029b302
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 13:00:23 2015 -0700

    Settings: fix potential NPE when resetting profiles
    
    When the user hits the positive button in the confirmation dialog to
    reset profiles, we force a refresh of the profiles list. This can lead
    to a NPE exception being thrown if it happens before the dialog actually
    gets dismissed (and the ProfilesList fragment is actually attached)
    since the reload list calls getPreferenceScreen(), which can be null,
    since it is not attached.
    
    After the dialog disappears, onResume() gets called in ProfilesList
    anyways, so there's no need for a forced refresh.
    
    Change-Id: I93de7115a69cc7545bf6a33de3a4abf5443658b9
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 89d040a9d5f8d316bbbec67ec93a36c70d85ef38
Author: Matt Garnes <matt@cyngn.com>
Date:   Wed Mar 11 12:27:44 2015 -0700

    Settings: fix "Mobile Networks" menu option in DataUsageSummary.
    
    Point to com.android.phone.MobileNetworkSettings instead of
    com.android.phone.msim.MobileNetworkSettings, which does not exist.
    
    Change-Id: Ibfbae3d94020fd1bcdcd3095d4c6c38f48f53609

commit 7bda6332cec956b562c2dc172d6eda751945766a
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Mon Mar 9 20:47:19 2015 +0000

    Sound settings: remove vibrate category on devices that dont support it
    
    also remove power notifications vibrate from other sounds
    
    Change-Id: I1929074a462f425cdf03cedba66f85dc9593f819
    
    Patchset: 2
    http://review.cyanogenmod.org/#/c/90972/

commit 43614ac1cf3cacd51ed756429bce14423a934f40
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Thu Feb 19 18:35:41 2015 -0800

    revert: Settings: LS weather disabler (2/2)
    
    PS2:
    Restart system to apply change
    PS3:
    Fix build
    
    Change-Id: I61f5fe7360d4c632108a05f9e7bf8c9e174a6db1
    
    Modified to temasek
    
    (cherry picked from commit 8cea39eff18cbdabeacd76e92adee8b49b102025)
    
    (cherry picked from commit 8276780362b2fcaacd112870226b6c02345fe7a3)
    
    (cherry picked from commit 8276780362b2fcaacd112870226b6c02345fe7a3) (reverted from commit b142599ffb9c3a34daac31ae0b467b153b95f09d)

commit e2bf2f9c949fbb7536d36a695c2dbf636019de5c
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Mar 12 01:29:48 2015 -0700

    Settings: hide keyguard visualizer toggle on low end gfx devices
    The visualizer is disabled on low end gfx devices
    
    Change-Id: I67178f59baa18fe7586bb08835f9f255c31f84f6
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/91122/1
    
    Conflicts:
    	src/com/android/settings/lockscreen/LockScreenSettings.java

commit ad72234256afaa68c04186dbf7a61e20f74fa5a6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Mar 12 20:26:53 2015 -0700

    Settings: Cleanup battery saver settings
    
    * Add back auto battery saver
    * Add back support for battery saver on devices without perf profiles
    
    Change-Id: I562420a81592fde54a96dca88a71ed9137bb59a9
    
    Conflicts:
    	res/xml/battery_saver_settings.xml
    	src/com/android/settings/fuelgauge/BatterySaverSettings.java
    
    Conflicts:
    	src/com/android/settings/fuelgauge/BatterySaverSettings.java
    	src/com/android/settings/fuelgauge/PowerUsageSummary.java
    	src/com/android/settings/search/SearchIndexableResources.java

commit 70ebe57ff7326e7aaac402b64bf27735413d7ab4
Author: alviteri <activethrasher00@gmail.com>
Date:   Thu Mar 12 20:29:15 2015 -0700

    Settings: Rework 'add ability to change the color in battery saver mode'
    
    Adapt to new changes following cm's one
    
    This update the following commit: 152650ed3a20bc777f1f8e6c474c506e9b304975
    
    Conflicts:
    	res/values-pt-rBR/cr_strings.xml
    	res/values-ru/cr_strings.xml

commit ad320bf0bd5276d7da68a412a1a4b97e82da94ab
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 13:24:25 2015 -0700

    Settings: bring up IME when renaming profile
    
    Change-Id: I3535503d5e5431e9e6790933171e0fabe05c3cc6
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit f35820ae6aedf7eba63d7663d74b55198ee0e0cc
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 17:11:32 2015 -0700

    Settings: theme mobile network settings from data usage screen
    
    Change-Id: I7cdd04a25ead453e8145ff07c8db60a498ef6df5
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 97dad500db125842048f91f7f1505a98f3c88cf1
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Thu Mar 12 12:45:49 2015 -0700

    Regulatory text color: make this readable
    
    Change-Id: I944f91f70d18f55542deee14f5153626f539ad29

commit fdc9951886edae29f7c9dc8fa16eb5cd85ef15a3
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Mar 12 19:28:37 2015 +0000

    Revert "Settings: fix potential NPE when resetting profiles"
    
    This reverts commit 9e729a248ce7001fa8607d3373f65a7f3c572edd.
    
    Change-Id: I8f7598803db143433cdcd85e99874b389b0c2af7

commit 6e0f0727d2f498168243c03fd7d8ec3ace2b91f5
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Mar 12 16:42:51 2015 -0700

    Settings: merge ProfilesList into ProfilesSettings
    
    ProfilesSettings previously had a viewpager with the profiles list, and
    an app group list. Then we removed app groups, but the viewpager was
    left over.
    
    The main reason for getting rid of it now is to make sure that
    refreshList() always works. Previously there was a small chance that
    because it was in a viewpager, the preference may not have been attached
    (at the time of the resetAll() dialog being shown and user pressing yes),
    which caused the refresh method call to fail, since it needs access to
    the preference screen, which is null at that time.
    
    Change-Id: Ib9c3a27e3062660bd8a91998c20c15b4ffb4390b
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 727f37f5f2ec2b81f9cd4f6a6c07181d89cee71c
Author: XXMrHyde <email@address.com>
Date:   Thu Mar 12 20:35:33 2015 -0700

    Lock screen: Text and icon colors, (2/2)
    
    Change-Id: Ib4a085aa00769b05530f6dfdfbf18c0792b31cc3

commit 2e2b6098b3d365aacb54c2138a6bfbb6d9a2f553
Author: alviteri <davidteri91@gmail.com>
Date:   Thu Mar 5 06:00:00 2015 +0100

    Settings: Materialize standard colors in colorpicker

commit c567f0b37142db9edda3799110bc52e7b981fcf8
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Thu Mar 12 20:41:23 2015 -0700

    (2/2) Settings: allow to toggle smart cover wake
    
      * disable by default
    
    Change-Id: I1f97dc1a945520d2b563cdafdb19becad23cb993
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit 1610343f6e6fc8e1e4a1456088ae0c07a53dd819
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 01:03:54 2015 -0700

    BATTERY_SAVER_MODE move to cmremix settings

commit a0599913cab340ddeae5ca78706bacd570eec987
Author: Janson Kang <temasek71@gmail.com>
Date:   Fri Mar 13 16:47:37 2015 +0800

    Remove duplicate weather on notification drawer option

commit d92256e7d9a3545a73971fff50e5459e14a5df3d
Author: Steve Kondik <steve@cyngn.com>
Date:   Fri Mar 13 15:33:06 2015 -0700

    livedisplay: Fix for multiuser
    
    Change-Id: If0ef1da91cf5310308abf08806f7902e25080d2c

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

project packages/apps/SoundRecorder/
commit 8fd462159f64b8d90d3c76f05af8a551e5d9b850
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:44 2015 +0200

    Automatic translation import
    
    Change-Id: I9a45be5d27dd6e3d347b87c4c1d7ae9fa1374b37

project packages/apps/Stk/
commit c50f40acf0054a591ec7d6ac6346fbf90a82390c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:49 2015 +0200

    Automatic translation import
    
    Change-Id: I16c007fc2872023bcc03cd48953343ccf6c55dab

project packages/apps/Terminal/
commit 37622aeb7ff5a026beae2a2e779f5f09070f848e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:54 2015 +0200

    Automatic translation import
    
    Change-Id: I4b294562545b9035562c97c3433270ea4ef1775d

project packages/apps/ThemeChooser/
commit 979a19ad3210a88449ac58829b2bcccb238000c1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:00 2015 +0200

    Automatic translation import
    
    Change-Id: I75989a6f5c7e6a16e08225d9cac0442e0dd3d2c8

commit 5e1a5f4bc0180a1f4511fd7af2dc2502b549d4e3
Merge: df1b5e2 979a19a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:13:30 2015 -0700

    Merge remote-tracking branch 'github/cm-12.0' into cm-12.0

project packages/apps/UnifiedEmail/
commit 55e9bb97d314bef3e091df5f86690ae15fcdeccf
Author: Kenshin <foufou33@gmail.com>
Date:   Thu Mar 12 13:54:52 2015 -0700

    UnifiedEmail: Fix build
    
    Change-Id: I180829783123498b1c6a06b0d877e9ce451429b0

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

project packages/providers/DownloadProvider/
commit 0d7a9c60e83236da17e5917c201dfc612c72bd81
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:53 2015 +0200

    Automatic translation import
    
    Change-Id: Ib0d03cb90567d7ac6123c2c97be226ef65859ca7

project packages/providers/ThemesProvider/
commit 4938b49e080438be59fe8d4dcd7ff10a7ba279ed
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 6 15:38:27 2015 -0800

    Themes: Add previous value and update time to mixnmatch [2/2]
    
    Change-Id: I6b4224e9416e61ce7792e608bd4fd602a9b34e47

commit cc0e0e1f3d19109cfe2a6ff2e2b616d5b97e90f6
Author: d34d <clark@cyngn.com>
Date:   Fri Mar 6 16:06:57 2015 -0800

    Return InstallState.UNKOWN if context or pkgName null
    
    Change-Id: I7e8f40335c4b5a202d457eba7f3bd337b9342908

commit 6c29892fc83a43a7f363f56950ac6e7a8423ac91
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 11 15:05:32 2015 -0700

    Themes: Process theme resources after package scanned [2/2]
    
    The provider now assumes that the theme service will process all
    themes and icons packs, and then sends the appropriate broadcast
    once processing is done for that package.
    
    The preview generator now queries for the theme 's capabilities rather
    than rely on that info to be passed in.  This is partly due to the
    new flow of installing a theme as well as the fact that legacy
    icon packs were not having previews generated.
    
    Change-Id: I418debb6f91296107476016367131fac2c3a32ce

commit 7320de5213287aa159a5a6695eaea47d3be15935
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:57 2015 +0200

    Automatic translation import
    
    Change-Id: Ic3e8aad4d67edc9afc8080e8c23aacd641ee5cfa

project packages/services/Mms/
commit e6cce3ac25963327ee451edbd4377b0faf600253
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:03 2015 +0200

    Automatic translation import
    
    Change-Id: Id569ae5e8f5048a2de22bd94c0bbfb6a76309c72

project packages/services/Telecomm/
commit 4e6de9d87de74eba3c4f4f22e161b644b03635b1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:07 2015 +0200

    Automatic translation import
    
    Change-Id: I62eee2d91dae9d4f8b81255bc75f761c69459710

commit 1952939241128b05a19fb44818aed7326482874f
Merge: e44d04d 4e6de9d
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:12:48 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/services/Telephony/
commit ae3bb13b4d7b343f8e6c1705f5b835539b4beff3
Merge: a5f8f8d 699f273
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:50:43 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 219cd9eba9ef4b8952d1a17dc6c211db62431978
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Mar 11 13:49:07 2015 -0700

    Dialer settings: fix "Additional settings" up arrow inconsistency
    
    Dialer > settings menu > settings > call settings > SIM card settings >
    Additional settings and then press the back arrow, you should go back to "SIM card settings"
    but, instead, you'll go to "call settings".
    
    Back button bring us to the correct screen, use the same logic for up
    arrow.
    
    Change-Id: I3b786458ede78bf906e12017c2e6943c47999e06
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit b710b9d159665fa198520dbe41347c751e11f0a2
Author: Lin Ma <lma@cyngn.com>
Date:   Thu Mar 12 16:13:46 2015 -0700

    phone: Fix crash in MSISDNEditPreference when changing phone num.
    
    When GsmUmtsAdditionalCallOptions's onCreate is called w/o a
    Bundle handle, mMSISDNButton.init won't get called, hence
    MSISDNEditPreference's mPhone is not initialized, which causes a
    crash when onDialogClosed accesses mPhone.
    
    * mMSISDNButton was not initialized, retrieve handle from prefSet
    * Call mMSISDNButton.init to make sure mPhone is initialized
    
    Change-Id: Ia0b629dab69edbc76d542dc603251f4d98715227

commit 4d3b02c94b0e44f98fc26b9e91f02174ba57db55
Merge: ae3bb13 219cd9e
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 20:51:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit bc21c0fe33452aab622986c5ef7ee5b449384b82
Merge: 4d3b02c b710b9d
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Mar 13 20:29:02 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

commit 60f23f71b75e54a2691b2c2c295cdbb0de6d8752
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:12 2015 +0200

    Automatic translation import
    
    Change-Id: Idef066c8e851fd1d7d3ed31d6400525494ad3677

commit 98c026a3c4449b622eabc56d77818a164370b74e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 03:37:23 2015 +0200

    Fix the build
    
    Change-Id: I92d4aa4b4b96067f666b744b85bbc4d088e37756

commit dcf923350a299f97e7622e070657e27d08ef29ba
Merge: bc21c0f 98c026a
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 00:13:10 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project packages/wallpapers/Galaxy4/
commit a888455046de53772306fe5df9fa3c534c6e79e2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:18 2015 +0200

    Automatic translation import
    
    Change-Id: Id45661d16d340f3801c92c01ec38cb0eb5071ea6

project packages/wallpapers/PhaseBeam/
commit 6ec4a28b5a99af777fa79ade2050be261a67168e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:23 2015 +0200

    Automatic translation import
    
    Change-Id: I0d2533e714b93d7224eb9599c1bb7297c8dc8230

project packages/wallpapers/PhotoPhase/
commit e5cfe1e367190810600ecea004c1797ade3f32e7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:28 2015 +0200

    Automatic translation import
    
    Change-Id: I21241d7958cd14d847de18fe324e6206e257b56c

project prebuilts/gcc/linux-x86/arm/arm-eabi-4.9/
commit ec483fab9cbd92b3c0161843971dd3c9b7b1ede4
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Mar 14 04:47:37 2015 -0600

    Initial commit
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

project prebuilts/gcc/linux-x86/arm/arm-linux-androideabi-4.8/
commit 6524d367f4bafb9d468b3fa0523501f2eec706cc
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sat Mar 14 03:35:52 2015 -0600

    Initial commit
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

project system/core/
commit 5d31618b987cef89ecf5cf980b048f0b5349f0bd
Author: Ricardo Cerqueira <ricardo@cyngn.com>
Date:   Fri Sep 19 10:43:12 2014 +0100

    init: Let a device's init.rc redefine service entries
    
    In case of duplicate service definitions, init.rc's version always
    wins. This is a less-than-ideal situation and the main reason for
    some devices to override the default init.rc, which leads to out-of-sync
    situations whenever we happen to insert something into the main copy.
    
    So let services be overridden. To prevent accidental override of
    system services, use a specific keyword for this, "service_redefine"
    
    Change-Id: Ib1cab6bd3008956e9a2f61355781861ef8bcf8ca

commit 7466283affe6989c1c462346f3d109e78a2345f4
Merge: 80ec2d9 5d31618
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:57:43 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project system/vold/
commit 85a78d5c762240424ad99cc8a4e6d6a7fb35b70e
Merge: b010385 97991de
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 10 21:52:33 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project vendor/cm/
commit 1245bc273a1266f063860d7e7e4eb7f47c10c858
Author: Howard M. Harte <hharte@cyngn.com>
Date:   Fri Mar 13 17:58:42 2015 -0700

    Add APN for Smartfren
    
    Change-Id: I1553dad104c200822167baa3a33d6fe6dbd176da

commit 359fddf704251c102935331ae8d762612bdaca4a
Author: Emerson Pinter <dev@pinter.com.br>
Date:   Thu Feb 12 19:20:19 2015 -0200

    sepolicy: Permissions for userinit
    
    Change-Id: Icaf9d191841a6214925729e40d84a61a2ebf2296
    
    Patchset: 8
    http://review.cyanogenmod.org/#/c/88652/

project vendor/cmremix/
commit 4c659dfa9c7f958324bc110cebb672cb623a090e
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 00:03:16 2015 -0700

    update Viper4Android to 2.3.4.0

commit 0f761027f5c94dcf0fc7b080e6d1187c59943a09
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 12 01:36:31 2015 -0700

    fix cmremix version

commit 863032ef128c9f91a0d38b00eab95ab8c9327518
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 00:30:47 2015 -0700

    USE_CLANG_QCOM_LTO (lto) in about

commit 931c1c4aa256f0e33482d3cea3bb60e21d4d3c85
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 16:22:01 2015 -0700

    random: set proper permissions for e/frandom

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

project vendor/samsung/
commit 3bbca26126cd482ed820cf1e27d794fdf363d473
Author: Arne Coucheron <arco68@gmail.com>
Date:   Thu Mar 12 05:32:33 2015 +0100

    serrano: Update blobs
    
     * From SHV-E370K's 4.4.4 ROM.

commit c0dc7958e69d2b7ec7bcff9115095cbd13b2ce5f
Merge: 8f6ed55 3bbca26
Author: Arne Coucheron <arco68@gmail.com>
Date:   Fri Mar 13 06:11:38 2015 +0100

    Merge pull request #593 from arco/cm-12.0
    
    serrano: Update blobs

commit 198ec0c1c5ad03e8554d92c563f47d1815eef86a
Author: Arne Coucheron <arco68@gmail.com>
Date:   Sun Mar 15 01:16:04 2015 +0100

    Partial revert "serrano: Update blobs"
    
     * Revert RIL blobs
    
    This reverts commit 3bbca26126cd482ed820cf1e27d794fdf363d473.

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
