
project bionic/
commit d0e6a2759af7c0264ba49f480d001ca6be5e4944
Merge: 9c38646 0e825a7
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Mar 14 23:53:37 2015 -0700

    Merge remote-tracking branch 'upstream/cm-12.0' into cm-12.0

project bootable/recovery-twrp/
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

project frameworks/base/
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

project packages/apps/BluetoothExt/
commit 31c24878e779fcac76a946fbdf2bc75cece88ee8
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:39 2015 +0200

    Automatic translation import
    
    Change-Id: I0dbd3486f50f9c10cc9af3ea0b2dc353efa5d34b

project packages/apps/CMFileManager/
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
commit a5a544f00da0b5b32ecc49b9baef46125de3b9aa
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:27 2015 +0200

    Automatic translation import
    
    Change-Id: Id2dc16829a8d9b7a3ecd5fe92a3cc0e25df7df62

project packages/apps/ContactsCommon/
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
commit 1acc38bf8a57600f3bea031e39ea37a668c3912a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:49 2015 +0200

    Automatic translation import
    
    Change-Id: I706ba0b421b725967fca66376be10a6a4027e4f1

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

project packages/apps/LockClock/
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

commit a3ac20d162bd67c9140b2afcc41cf35266105f1d
Author: Linus Lee <llee@cyngn.com>
Date:   Mon Mar 16 18:18:22 2015 -0700

    PhoneCommon: Adjust dimens for hdpi
    
    The spacing for the dial pad is too small, so
    create some more space by decreasing the whitespace
    between the dial pad at the top bar
    
    Change-Id: I2775ce417b53f7a69abeb3b8919169024a7714dd

project packages/apps/Settings/
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

project packages/apps/SlimCenter/
commit 01e134893dcc07c2363cc902c86f8f8f000e6bdc
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Mar 15 19:11:27 2015 -0700

    cmRemiX >>> CMRemix

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

commit 3909e40c68fddbfd3426f1f16f81e7a690c7bd38
Author: Tadashi G. Takaoka <takaoka@google.com>
Date:   Wed Nov 19 13:45:21 2014 +0900

    (DO NOT MERGE) Fix Greek accented upper case letters
    
    Cherry-picked 6fc92899d82f4d3cb30f7bb2c57133154f0babd2 from
    ub-latinimegoogle-edamame-mr1-release.
    
    Bug: 18418991
    Change-Id: Id4dff41ba488635ff9af899be6d4f84ab00a96c8

project packages/providers/DownloadProvider/
commit 0d7a9c60e83236da17e5917c201dfc612c72bd81
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:53 2015 +0200

    Automatic translation import
    
    Change-Id: Ib0d03cb90567d7ac6123c2c97be226ef65859ca7

project packages/providers/TelephonyProvider/
commit bda9e4d340743d1a68d01bec29a44cba756b8ee1
Author: Amith Yamasani <yamasani@google.com>
Date:   Thu Nov 6 09:01:20 2014 -0800

    Make TelephonyProvider a singleton across users
    
    Messaging apps need to access it from secondary users
    
    Bug: 18194892
    Change-Id: Ia7401c287f4b920ac4de5102f33ded22bbf0f5b9

project packages/providers/ThemesProvider/
commit 7320de5213287aa159a5a6695eaea47d3be15935
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:57 2015 +0200

    Automatic translation import
    
    Change-Id: Ic3e8aad4d67edc9afc8080e8c23aacd641ee5cfa

commit a6afd7e22df46a004d78ad2ed9ec3f1ab2c674b3
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 18 14:07:24 2015 -0700

    Fix icons with filters not being generated
    
    If a theme has composed icons that only use color filters, they
    would not get generated.  This patch resolves that issue.
    
    Change-Id: If9076eca8cce1a85beed54ce30f0dfb8bbcd3188
    REF: CHOOSER-63

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

project vendor/cm/
commit 1245bc273a1266f063860d7e7e4eb7f47c10c858
Author: Howard M. Harte <hharte@cyngn.com>
Date:   Fri Mar 13 17:58:42 2015 -0700

    Add APN for Smartfren
    
    Change-Id: I1553dad104c200822167baa3a33d6fe6dbd176da

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

commit 52bf318a9f616ef0b3bfe5099b8f3aceec86543a
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 00:48:20 2015 -0700

    Revert: sepolicy: Permissions for userinit
    
    Change-Id: Icaf9d191841a6214925729e40d84a61a2ebf2296 (reverted from commit dc699fb190a7249053c4f2fd280f9dc8a3096fe6)

commit 3fc3b8046be89bf90828a449c74fa93a8b11a86f
Author: Tony Layher <layhertony@gmail.com>
Date:   Tue Mar 10 20:01:56 2015 -0400

    vendor_cm: sepolicy: address sysinit denials.
    
      From the log:
      avc: denied { getattr } for pid=317 comm=run-parts
      path=/system/etc/init.d/90userinit dev=mmcblk0p24
      ino=65035 scontext=u:r:sysinit:s0
      tcontext=u:object_r:userinit_exec:s0 tclass=file
    
    Change-Id: Ib9983c2dac1e241cadb049d6bd966abcc5f18d4c

project vendor/cmremix/
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

commit ea15c9af8a86aa2b12288aba2dabc59d27eb4b5e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Mar 17 20:07:42 2015 -0700

    vendor: add CMRemix Weekly_Changelog

commit 4da61eeeec7c288ebbeb019cdf802d46d51f3b00
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Mar 19 00:51:03 2015 -0700

    disabled cmremix optimization for now

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
