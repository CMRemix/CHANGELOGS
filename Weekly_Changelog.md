project CMRemix/
commit a2495560cbac1ee9638580af00c7281dbe2cfa90
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:56:38 2015 -0700

    Revert: track bluetooth bluedroid (reverted from commit d349e86a2ddaa45c084023b2a90f3ae4aee2eee9)

commit 3d8b1da401d904860db678580d712776814711fa
Merge: a249556 02ce06c
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:57:28 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1
    
    Conflicts:
    	default.xml

commit f1df931400ad392a3732a384b1d41f1b30bb4fac
Author: Steve Kondik <steve@cyngn.com>
Date:   Fri Apr 17 01:12:21 2015 -0700

    Add LZ4 tools to the build
    
    Change-Id: Ib7346f85e31b9a8651a3d40c1ccb4c675e584b4c

commit 132c60ba810ca10192c469c4dbe77e0a3f0fd99b
Merge: 3d8b1da f1df931
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:42:03 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 0596b1a104b56dfe6c9fa749cebecb59f4028ecc
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 19 01:10:13 2015 -0700

    remove twrp

commit d344c5eb261213b49c4e2282adc544552ab8ddfa
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 02:39:21 2015 -0700

    track  Kernel Aduitor and add floating button support repo

commit 88248728f2683fae9405d5add328bb1934058471
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 08:02:11 2015 -0700

    remove performance control

commit 801833b840407eceda8e54aa54a2d905005908ac
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 21 23:11:50 2015 +0300

    5.1.0_r5 -> 5.1.1_r1
    
    Change-Id: I08bfa4e9147dc26b63cf14d12638591a67a94103

commit cf00dd903ca8a2566c3e789dacc2904783dbbe4f
Merge: 8824872 801833b
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 18:43:25 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project bootable/recovery/
commit c503cdf9f6aedece48bfc6dc6a06ffcc9a2130bc
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Wed Apr 15 02:45:38 2015 +0300

    sr: Add missing tool links
    
    Change-Id: Ic61f862c9edb31f6b7323e154e6b085afd15a947

commit a6ea0d0fcb04b2d00c03ea78385ab639e6faf94c
Author: Tom Marshall <tdm@cyngn.com>
Date:   Fri Apr 17 05:23:00 2015 -0700

    recovery: Add lz4 libs
    
     * Required by transparent compresssion in make_ext4fs.
    
    Change-Id: I566c9e1281cc0dd725e96db32da0a1c3c000030e

commit 04f21095b9793573ee81105e44313a147c368d82
Merge: a6ea0d0 0e5356a
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:25:04 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/bootable/recovery into HEAD
    
    Android 5.1.1 release 1
    
    Change-Id: Ie0c1f776db503e8903b1b44154240ade347dbcaa

project build/
commit e170efefb4d47d87236328074982c37a9b942e76
Merge: 74c4b2e 1e6e335
Author: ZION959 <ziontran@gmail.com>
Date:   Wed Apr 15 00:15:45 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit ab991744156063f1d016619da59eaa3bb4efa92a
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 12:14:30 2015 -0700

    ARM: Enable -fno-builtin-sin and -fno-strict-volatile-bitfields by default:
    
    No one uses anything less than gcc 4.6 anymore so stop using a
    redundant filter for it...
    
    Change-Id: Ib5cce3fe4d67f59a13542148de807487961cfcb3
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	core/combo/TARGET_linux-arm.mk

commit f43ab492818aa0c2f8f9977dff1a5d24eb62a2f0
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 12:21:25 2015 -0700

    extra sabermod flags binary mode: separate gcc from clang completely
    
    Change-Id: I90c9d143632126282c9c7dc72c7867442be23546
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	core/binary.mk
    	core/combo/arch/arm/armv7-a-neon.mk

commit afd984bb73c884969c475810a01ae27a27e8d51a
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 00:44:38 2015 -0600

    Add some basic host optimizations (2/2)
    
    This is mostly beneficial when used with -O3 optimizations
    
    Change-Id: I53bab4e9edba04046a6e5f726749bba483ed92a9
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit f9b2ba6f7a67422b7f70d4cf130941ca5e357ec0
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 21:28:55 2015 -0700

    [1/2] add force disable strict aliasing modular
    
    Change-Id: Ib5ddd7f2b16166bb562b69912306598782101b21

commit 127e72343df004abda3e660118062beb795f666f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Mar 19 23:47:55 2015 +0200

    build: Move bacon public key to device tree
    
    Change-Id: I50c780203f7ecdd3008ac07146b7c9db91f9a443

commit abc882d9ca5e442bef5344c998023daf056bb35f
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Wed Mar 25 18:14:46 2015 -0700

    releasetools: add compatibility for full ota functions with incrementals
    
    Some device-specific releasetool functions may expect that input_zip
    and input_version are set. For incremental OTAs, target_zip and
    target_version are set instead.
    
    Set input_zip=target_zip and input_version=target_version to add
    compatibility with these functions.
    
    Change-Id: I6a04f67440618d3652396656cc1fe223d4a6b195

commit 35b76065fd6a84af739d4d044c55a63133717150
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Thu Mar 26 16:32:34 2015 -0700

    ota_from_target_files: Fix path for SkipNextActionIfTargetExists
    
    Without the leading forward slash, the check always fails.
    
    Change-Id: I57320c20ca2b384713182082b1ad5321d78dbb2b

commit 5c3cd360000d64a2cd2bcae4bf552a59d15b8902
Author: Brint E. Kriebel <bekit@cyngn.com>
Date:   Fri Mar 27 20:53:59 2015 -0700

    ota: Include full boot images when imgdiff fails
    
    When generating a non-block based incremental, inclue the full boot
    image when imgdiff fails to generate a patch. This logic is already
    used for block based incrementals.
    
    Change-Id: Idae484ea8c2553a3480961dfa413724e61c52e5f

commit bfdab6fe38152553d84295d1e2016d9cc933eea5
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Wed Apr 15 12:00:43 2015 -0700

    build/core: Define find-other-aidl-files.
    
       Useful when utilizing relative paths that mention external
       projects. Mimics find-other-java-files, etc.
    
    Change-Id: I3df67f4f35a931facbb1de76936936b092a42bb2

commit f55a1fa1a4a3edf25c75d93d9ef3b1b1e5261dae
Author: Tom Marshall <tdm@cyngn.com>
Date:   Mon Mar 23 07:09:38 2015 -0700

    build: releasetools: Support transparent compression
    
    Change-Id: I339fe8dbf287ce7c88e133a5b3f5c502dc56dd3b

commit 1365b34463593820f6dbefb0769700e63352df29
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Fri Apr 17 23:36:27 2015 -0700

    Cleanup graphite:  LOCAL_CFLAGS will be used for CPP flags
    
    Change-Id: Ida6dd67dbfb257b8c86bda3a1ead320d68847643
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	core/binary.mk

project device/samsung/trlte-common/
commit aef8ca483073a3c50d500b393495b5103c1e92ee
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 12 23:52:59 2015 -0700

    trlte: Add call recording overlay
    
    Change-Id: I04b8cff9e545921383d8a1e17f673ed674cec3b0

commit 971eb7c4c45692d7151a2e1f057d4c2184572882
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 19 00:56:33 2015 -0700

    removed twrp
    
    Change-Id: I7a7b02fa64fddeb4d0ac6d308bbd658577f1ac85

project external/icu/
commit 57fc3598f6f0ebef70fd392df21cfe1a0fdec750
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Apr 4 02:50:56 2015 +0300

    icu: Fix Kurdish Arabic locale detection
    
    * Android 5.0+ supports ISO 639-2 naming but still doesn't support
      more complex locale naming like ku-sArab-rIQ
    * Add back the deprecated ku-rIQ locale from older ICU versions
      to workaround the issue, like we used to do in android 4.4
    
    Change-Id: Id1cc22e8cf3d7bd4a57affe401def1797a081289

commit 59c2e6e6e80fd34c9b90de1b6c0031994ecedfa2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 04:21:00 2015 +0300

    icu: Regenerate stub data for 5.1
    
    Change-Id: Ia91253a03b9f5d89ec0dc3e51267b33a38921893

project external/libpng/
commit e1b2e937ab4811a1a695ba2e08807e906523f321
Merge: bf497ca 7be36a0
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:17:40 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/external/libpng into cm-12.1
    
    Android 5.1.1 release 1

project external/libselinux/
commit 2e2f4ae0697745285fff29b89c031df8f2733e4f
Merge: 7e1e3d7 6608a18
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:17:47 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/external/libselinux into cm-12.1
    
    Android 5.1.1 release 1

project external/whispersystems/WhisperPush/
commit 64ed935dd2b6ac42b6a8cd1bb24e348fc9812412
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:33 2015 +0200

    Automatic translation import
    
    Change-Id: Iadb061cd812b5ac3af76d16a2ba0e6853f98e0d2

commit bd677b9a25e697093f1434f0f022d1605e0d16fd
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:03:15 2015 +0200

    Automatic translation import
    
    Change-Id: Iad0e85daeee224e47ecbf7eacd1367776fc275ad

commit 2de30fc65cef7e67dc496ff385fcdcfddf7c492c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:54:00 2015 +0300

    Automatic translation import
    
    Change-Id: If0ed51471157bebd0a3a8cef9b6554b848b27a6e

commit 194900df00a94cdb90541e5c43188b87eeaa4b46
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:37 2015 +0300

    Automatic translation import
    
    Change-Id: I4b409783a4393c09f1bd16ef3094a49f2f9edbb0

commit 816369585b2fa97b1907e05efac42cad660b319c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:22:11 2015 +0300

    Automatic translation import
    
    Change-Id: Ic46020dc2c5ca7d439770316a378d6adf8eb80fe

project frameworks/av/
commit 9d18eef08a351e898d98817efd159a1d51293be4
Author: Surajit Podder <spodder@codeaurora.org>
Date:   Thu Apr 2 12:57:58 2015 +0530

    nuplayer: Fix statistics profiling with buffering events
    
    Add pause and resume events profiling when initiated
    in buffering path during http progressive streaming
    
    Change-Id: If98a87812f4ecb3237e1731e1acbfb6007db5b42

commit 66d02344aa88d1c1f2ef3b4815f30c21d2d355c6
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Jan 24 23:26:47 2015 -0800

    nuplayer: Add cached lookup of track duration
    
     * After a seek in an HTTP source (such as Play Music), the duration
       ends up as zero due to multiple pending fetches.
     * This has a nasty side effect of breaking audio effects connected
       to the global mix (visualizer) after an offload fallback as the
       deep buffer stream wasn't selected either.
     * Cache the last known good duration and use it if the extractor
       isn't able to get it.
    
    Change-Id: I65f60323959455ec1ce45ae88b821d4227eeb14d

commit 72068fe33c14df5a5ff4545b169a27926bfa169c
Author: Leena Winterrowd <lenhardw@codeaurora.org>
Date:   Wed Apr 1 11:38:00 2015 -0700

    NuPlayer: Process time discontinuity separately for audio & video
    
    Whenever NuPlayerDecoder signals a time discontinuity to the
    renderer, both audio and video are affected. However, since there
    are two decoder instances (one for audio & one for video), this
    incorrectly signals two time discontinuities for each track which
    can lead to incorrect anchor times.
    
    Make the behavior of signalTimeDiscontinuity track-dependent to
    resolve this. Reset the anchor times only for audio time discontinuity
    and reset the video lateness only for video time discontinuity.
    
    CRs-Fixed: 809904
    Change-Id: I4f992f1901941daae251162f02b8044c51b1cee3

commit ac84c2782575dd8e83504e9acc6298476022017f
Author: Shalaj Jain <shalajj@codeaurora.org>
Date:   Thu Apr 2 13:01:06 2015 -0700

    nuplayer: Stop resume profiling after frame render
    
    Stop resume profiling after frame has been rendered and not just
    after videoQ is asked to drain, because that call might not
    render the frame right away if there is a delay due to audio.
    Also move the profiling start to begining of the function.
    
    Change-Id: I74391583bdfd8a6882c4e3c11483ce20bd5e2ef8
    CRs-Fixed: 815953

commit c5079e3fb1dc37f2b4c2637264f304a8b1245ebf
Author: Leena Winterrowd <lenhardw@codeaurora.org>
Date:   Wed Jan 7 19:55:47 2015 -0800

    stagefright: http: Skip invalid bandwidth measurements
    
    Measurements of 0 bytes downloaded can skew bandwidth estimation.
    If 0 bytes or an invalid delay are added as a measurement, do not
    add it to the bandwidth history.
    
    Allow bandwidth estimation with a single history entry since the
    total delay is now guaranteed to be non-zero for any entry.
    
    CRs-Fixed: 808563
    Change-Id: Ib68122302176f892989e37ba26e9848f0f4113d0

commit 1bdd2586cd790399d1fcd422f992376c6d96ecb5
Author: Apoorv Raghuvanshi <apoorvr@codeaurora.org>
Date:   Tue Mar 31 11:21:10 2015 -0700

    audio: Fix for Sound from handset leaks to speaker
    
    Greeting message leaks to speaker since touch sound
    (for stopping greeting message playback) is routed
    from handset to speaker. Fix by also checking
    againt primary output for new output device for
    inCall usecase
    
    Change-Id: Id2fd20de7a279f74e38a9aefe91e17b36cc9da6f
    CRs-Fixed:812723

commit 4b1ddb23480f04fe6ae632a8db7d11a17b60da46
Author: Mingming Yin <mingming@codeaurora.org>
Date:   Tue Apr 7 15:22:14 2015 -0700

    AudioTrack: initialize mUseSmallBuf in AudioTrack constructor
    
    - Initialize mUseSmallBuf to false in AudioTrack constructor.
    
    Change-Id: I6b04ff23380b850bf69bcef0af3d5ceec688f77c
    CRs-Fixed: 812444

commit 67ab408518e6b9740bf03e612609090a32d12650
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

commit a48153c254112c14ab9d0c5164cb56e47d4ea087
Author: Maunik Shah <mshah@codeaurora.org>
Date:   Thu Aug 15 17:11:15 2013 +0530

    Screenshots info is not updated when device is plugged in MTP mode
    
    When device is connected as MTP mode and user opens folder
    /sdcard/Pictures/Screenshots/ in windows system and captures new
    screenshot, image information is always shown as 0 KB
    
    Issue: https://code.google.com/p/android/issues/detail?id=56204
    
    Change-Id: I86d8e1ee54c0d8b2008b5f6bc0de2cac3faafc20

commit c888808ec297b1f78388848f1c230368df2de793
Author: Zhou Song <zhous@codeaurora.org>
Date:   Tue Mar 31 13:53:14 2015 +0800

    Initialize the start time if not specified in meta data
    
    If the start time is not specified in meta data, the start time
    will be assigned with latency of AudioRecord, it's calculated by
    allocated frame count which is not the real start time when the
    first frame received
    
    Initialize the start time to the current system time if not
    specified in meta data
    
    CRs-Fixed: 812379
    
    Change-Id: Ia007ca4592fe1f96e105d4ec48305c578b677bb1

commit af3be7de6bd25b9ad01b8d93ea47f9a68dedea67
Author: Sai Kumar Sanagavarapu <ssanagav@codeaurora.org>
Date:   Wed Apr 8 11:58:49 2015 +0530

    CameraService: Fix recursive lock acquire during client destruction.
    
    While trying to remove stale clients, service lock will be acquired
    recursively due to which deadlock will happen and eventually
    framework reboot. So, remove this logic.
    
    Change-Id: I93b64cf075d339180aa426d985123878975a0abb

commit bd5cf4aecf105b1979eef72e6eccc3abbe187c91
Author: Sharad Sangle <assangle@codeaurora.org>
Date:   Tue Apr 7 15:04:55 2015 +0530

    NuPlayer: Don't maintain timeStamp if state is running
    
      While offload playback is going on, if user seeks
      to new position and after playback for some time,
      pauses till offload tear-down happens then playback
      resumes with old seek position
    
      The book-keeping of seektime for start of playback
      mStartupSeekTimeUs is also done in running state,
      it should be done only if current state is paused.
    
    Change-Id: I2987b44ddb944a971cb57587dc0af1826465fadd

commit fb483fb56406840fe987eb3954f1ef289f6c8152
Author: Naresh Tanniru <ntanniru@codeaurora.org>
Date:   Wed Apr 8 12:17:04 2015 +0530

    audio: Fix for ringtone playback issue on USB AOA
    
    - RingTone is not played for 2nd MT call while playback
      through USB-AoA
    
    - Duplicate tracks in audio flinger are invalidating on
      voice call as a part of voice concurrency on Bear.This
      results duplicate tracks to change non active state and
      subsequently not accepting any PCM data for subsequent
      ringtone playback
    
    - Do not call invalidate for duplicate tracks using
      AUDIO_STREAM_PATCH stream type
    
    Change-Id: I323e80470e64b58a53d68ca57a29605768324e14

commit 1c31653f6fd0c33c12011a96d96af8575b1bc7f0
Author: Ashish Jain <ashishj@codeaurora.org>
Date:   Wed Jan 28 11:19:48 2015 +0530

    audio: Fix fast playback of Ringtone for SCO call
    
    A2DP output is in suspend state during SCO call,but
    becuase of incorrect logic in checkA2DPSuspended,
    'mA2dpSuspended' was not set to true, and hence A2DP
    output is selected during SCO call, resulting in fast
    playback of ringtone on speaker.
    This change reverts the commit
    a985bd576ad8642b1ab99cc3a4e8bfd18c33e133
    
    Change-Id: I6744d15688d33cbe7b8a1584cc779ebf305c75df

commit a8e014b099c360ede644d05bc44bb7d21a541f7f
Author: Ashish Jain <ashishj@codeaurora.org>
Date:   Tue Mar 24 13:09:33 2015 +0530

    audiopolicy: Fix Audio record permission CTS failure.
    
    -Check which ensures that the recording is allowed only for
    applications which have the required permissions was missing.
    -Add back the code which was removed while resolving
    merge conflicts
    
    CRs-Fixed: 808998
    Change-Id: I0060f52839dd27876801001184b67dee887fe99d

commit 188aa8db759bb97cbfc5061658145e53e928f2dc
Author: Manikanta Kanamarlapudi <kmanikan@codeaurora.org>
Date:   Thu Apr 9 11:13:47 2015 +0530

    libstagefright: Fix for testException
    
    Handled decoder configure call for encoder
    component and vice-versa in fallback logic
    
    CRs-Fixed: 891538
    Change-Id: Ibb0d2da829a0e0f907ad8265836bac0466de1b4d

commit 3c2a50dad153a18fa08f43ead06f4dbb94b7f130
Author: Sharad Sangle <assangle@codeaurora.org>
Date:   Fri Apr 10 17:08:17 2015 +0530

    audio: Fix for camcorder shutter playback issue on BT
    
    - Shutter sound is not played for BT when starting
      camcorder recording
    - Duplicate tracks in audio flinger are invalidating on
      music stream as a part of record playback concurrency on Bear.
      This results duplicate tracks to change non active state and
      subsequently not accepting any PCM data for subsequent
      playback
    - Do not call invalidate for duplicate tracks using
      AUDIO_STREAM_PATCH stream type
    
    Change-Id: Ib6f46bacd70da5de5958f65d921c7c219a5b0dc1

commit 7dadc6a7f5bdcaaa397ea45f4d803e89daa1c7cd
Author: Xavier Varricatt <xvarrica@codeaurora.org>
Date:   Tue Mar 31 10:39:14 2015 +0530

    nuplayer: Fix for persist.debug.sf.noaudio when resuming
    
    Since moving to lmr1, persist.debug.sf.noaudio did not work
    when clips are paused and resumed because of audio decoder
    initialization in onResume. This fixes the problem.
    
    CRs-Fixed: 815542
    Change-Id: I1a2204ede77c70afc4c83d1fe7ac004bcc604eee

commit 5188aa6f3aca5e17808f7183d6f9dc34c81610f2
Author: Apurupa Pattapu <apurupa@codeaurora.org>
Date:   Tue Dec 2 15:48:39 2014 -0800

    stagefright: httplive: Fix switching for HLS live use-cases
    
    Playlists can periodically update during HLS live streaming, and
    the first sequence number can change accordingly. When switching,
    this leads to a mismatch in first sequence numbers that causes
    selection of the wrong segment, as the passed segmentStartTimeUs
    value is relative to the old first sequence number.
    For a/v fetchers, pass the previous a/v fetcher's sequence number to
    each new fetcher to enforce continuity of a/v streams.
    
    Change-Id: I26d8118dbcb7300571a5b3fb5d0808c5a0c08aa6
    
    httplive: Dont resume old fetchers if switching down
    
    - When bandwidth drops, resuming an old high-bitrate fetcher
      can cause freezes in playback. To avoid this, stop the
      fetcher without checking for any timestamp gaps.
    
    CRs-Fixed: 771954
    Change-Id: I690f50322a64e0b2c493062388c4b490b71db146
    
    stagefright: HLS: Remove LiveDataSource
    
    Remove LiveDataSource as it is no longer used.
    
    Change-Id: I07d9b09358dcdd2cb9e54fb6351e1c9027ce8a0d
    
    httplive: Do not delay fetcher when resuming
    
    During a switch resumeUntil is called on old fetcher so
    that it continues to download until the timestamp gap between
    old and new fetchers is filled. If this is posted with a delay
    new fetcher is scheduled first and it continues to download
    second segment increasing the switch latency.To avoid this
    resume fetcher download immediately.
    
    Change-Id: Ibdde95e016d83286dceed3f001b9a1d8b56b0367
    
    stagefright: HLS: Increase granularity of segment download
    
    Current HLS logic requires downloading an entire segment before
    bandwidth estimation or any other scheduled message can be
    processed which hurts the effectiveness of the downswitch monitor.
    If a large clip is being downloaded and the bandwidth drops
    suddenly, playback can hang until download of the large clip
    completes regardless of the downswitch monitor's status.
    
    Expand onDownloadNext into a series of onDownloadBlock messages
    to allow increased potential for message interleaving, but ensure
    that segment downloads themselves are not interleaved as
    LiveSession reuses a single http connection.
    
    CRs-Fixed: 759591 771954
    Change-Id: I6a9ba27e22cc4e04419ce0128ad0193edac9c42b
    
    httplive: Start playback at the actual bandwidth variant
    
    Download ts segment from the first playlist variant to
    evaluate the actual bandwidth and start the playback
    with actual b/w variant.
    
    Change-Id: Iaf86eb0124c9511a6a2e3580a91f666e711e54b3
    
    httplive: the triggers to switch up and down should be asymmetrical
    
    - change the usage rate of the real bandwidth from 80% to 90% except
      the first time
    
    - in up switch case, only when the real bandwidth is 30% above the
      target bandwidth, the corresponding index would be changed to the
      target one. Otherwise, the corresponding index should move to one
      lower level of the target index.
    
    CRs-Fixed: 810277
    Change-Id: I35e871e8d7702274d7ef880b6744b2ab763d6967
    
    stagefright: httplive: Enable dumping of fetched segments
    
    If SAVE_BACKUPS is enabled, create a numbered backup file for each
    new fetchFile() connection and archive all received bytes within
    /data/misc/media. Increase the number for each new connection
    within a playback session to aid in debugging switching use-cases.
    
    Also immediately flush all data after each readAt() to allow
    debugging crashes/asserts without loss of retrieved data.
    
    CRs-Fixed: 771954
    Change-Id: I38cb9653ffff8e8c6253a8caa0a7ee4a0bc7816f
    
    httplive: avoid zero byte read request
    
    - In LiveSession, check whether maxBytesToRead is zero, if yes
      ignore it because zero byte read request is meaningless.
    
    - In PlaylistFetcher, check whether the read bytes is less than
      the requested block size, if yes, finish fetching the current
      segment file because it means fetching file already meets EOS.
    
    Change-Id: I150d4b147090dbd48d804ebd96ea909e5b6fdbcb
    
    httplive: Print name of segment being downloaded
    
    Add change to print name of segment being downloaded
    CRs-Fixed: 787126
    
    Change-Id: Ice204b9bb6778ba16962610df5cd4e8b18576fd9
    (cherry picked from commit eb822627e1219686860c07ea0ca4509125dc8174)
    
    HLS: Fix issues in hls
    
    Because of the merge conflicts while
    porting L-Mr1, live session is accessing
    the invalid buffer. Corrected the same.
    
    CRs-Fixed: 807394
    Change-Id: I60ff90ae7ef9ad4b6bcf0956e022289fb552d766

commit 13f41efdf5733190b35a0f70f1791ed812d3bbd1
Author: Ricardo Cerqueira <ricardo@cyngn.com>
Date:   Tue Nov 11 15:47:16 2014 +0000

    camera: Add support for mediatek cameras
    
    Change-Id: I69ea758645922c433844ab191a737de2ff2e1491

commit e5c48faa7b69b787b8c82a99cb76ec190306013a
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 01:53:25 2015 -0700

    stagefright: Be more tolerant of missing metadata for FFMPEG codecs
    
     * If these codecs are instantiated programatically and required
       metadata isn't sent, just set some defaults instead of crashing on
       an assert.
     * This fixes testAllNonTunneledVideoCodecsSupportFlexibleYUV in MR1 CTS
    
    Change-Id: I69bf6105a1be529298de574bd5d3b6813e7a4e8f

commit 9e0b0f94ca020a9eaaf770c3b9fd9d44575c4e9f
Author: Surajit Podder <spodder@codeaurora.org>
Date:   Mon Apr 6 12:20:24 2015 +0530

    Revert "NuPlayer: Disable widevine flag for L3 content"
    
    This reverts commit bc92162fafe1e46ce47d40c5d1e9a1604b03c3c5.
    
    Change-Id: I422c8c2a8752f8adf9a33fecf51998b44b245a0e

commit 627d3b4f83cec373c16d1b09378a8e8081d67644
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 13:14:25 2015 -0700

    Revert "audio: Fix issues during device switch"
    
    This reverts commit 756e75e7e8c5cf30629591574e068cd82b104b95.
    
    Change-Id: I358ad056cc3ae03e9914701d41414d7f9735d4a1

commit 3f2532fe0e827e2861a04197b665a4d3a92c35f2
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 18:41:48 2015 -0700

    Revert "Audio streaming error when playing a stream that contains "end of file"."
    
    This reverts commit 6e96de734491d5d017b1d560ed44deffd36cc9cb.
    
    Change-Id: Ic06b63af6321640638e4e46d9c4977f286cad729

commit a02a9ed5fd230f37a212b900bbd56864f8935088
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 18:48:36 2015 -0700

    Revert "nuplayer: Add cached lookup of track duration"
    
    This reverts commit 66d02344aa88d1c1f2ef3b4815f30c21d2d355c6.
    
    Change-Id: Ia611fdc4fec63e7a31736cc3fc37df0bccec5080

commit da6beba95b22d6695aaf95aeb0f8c76a2697ec13
Author: Xiaoming Yang <xmyang@codeaurora.org>
Date:   Mon Mar 30 18:05:45 2015 +0800

    nuplayer: Fix audio EOS notifiy on AudioSink not ready
    
    Audio EOS won't be notified by renderer if AudioSink is not ready
    and first buffer itself has EOS. Playback complete won't happen
    due to missing audio EOS. Hence, audio EOS needs to be handled
    and notified.
    
    Change-Id: Idc9949d9d2fe942db38b87fb25a13edb41732545
    CRs-Fixed: 801121

commit 30672c8f17038b20c4ca1949519c1fc7e47f40c8
Author: Naresh Tanniru <ntanniru@codeaurora.org>
Date:   Wed Apr 8 13:18:39 2015 +0530

    audio: Reduce device switch delay
    
    - Device switch values are high on changing
      speaker to headset
    
    - APM delay device switch twice to the output
      descriptor latency to make sure play left over
      buffer in previous device before route to
      new device
    
    - Reduce device switch delay to 3/2 instead of twice
      output latency if routing is intended for same HAL module
    
    Change-Id: Iefe3883fedfe41eb033524ba85c48185af3000b2

commit 043435e1c507e4e39936c7aca2c3632e8359eb1e
Author: Dhanalakshmi Siddani <dsiddani@codeaurora.org>
Date:   Fri Jan 2 11:46:32 2015 +0530

     audio: Fix ringtone mute issue
    
    - Voice call ringtone is muted after multi party call
    - Primary output suspend count is incremented twice during multi party
      call and decremented only once, which is causing the primary o/p not
      opening at all after ending the call
    - Fix is not to call close again on the closed output by checking the
      flag status
    
    Change-Id: I2bcdcb2591942f48eac4635a3b36ee575787ee92

commit c82c8622b1b585e1a41dfbb5c46a0c95772936ee
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 20:03:31 2015 -0700

    stagefright: Fix the unhappy path in ACodec configuration step
    
     * CTS is very unhappy that ACodec's unhappy path is not taken
       when MediaCodec sends some very unhappy configuration. Like
       trying to use a decoder to encode. Nobody is happy with this.
     * Remove a check left over from 12.0 which is no longer needed
       to make the test happy.
     * Overall, on a scale of 0 (unhappy) to 10 (happy), I would rate
       my CTS experience of MR1 as a 7.
    
    Change-Id: Ia798642e0fe0fed0bb1156328adb4c5bd9acf9c4

commit eda0f8102add73565081faf6caaf36d7f284dbf7
Author: Mingming Yin <mingming@codeaurora.org>
Date:   Fri Apr 10 10:41:50 2015 -0700

    Audiopolicymanager: handle incall sonification without checking output refCount
    
    - Call handleIncallSonification in startOutput and stopOutput without
      checking mRefCount to make sure ringtone mute/unmute is called for
      multiple active stream.
    
    Change-Id: I0eab939b32fe47388e2515ab56154d540e9df55c
    CRs-Fixed: 819294

commit 73b0e26f6d93a234d751064e9dbbbc671083979a
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:14:35 2015 -0700

    audiopolicy: Cleanup and fix compilation warnings
    
    Change-Id: Id7053daa5c4accf8cc90052cc2c866dc3ae889ae

commit 0ebbb749a2e261a0da1f0c7558bf3b715e7c0a75
Merge: 73b0e26 2241216
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:22:44 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/frameworks/av into cm-12.1
    
    Android 5.1.1 release 1
    
    Change-Id: I45f1bd92576618550f01abb2f9439ee4718b1a54

project frameworks/base/
commit 35b9341b88ef6f2f6f33ad4c1efaf6e59a64b548
Author: Greg Hackmann <ghackmann@google.com>
Date:   Wed Feb 26 12:22:13 2014 -0800

    Find wall clock RTC through sysfs
    
    Devices may have multiple RTCs.  By default the kernel uses rtc0 to
    store the system time, but devices may override this (or even specify
    that none of them should be used for system time).
    
    Userspace can indirectly find the designated RTC through sysfs.  During
    AlarmManagerService initialization, enumerate through all rtc class
    devices to locate the device with attribute hctosys=1.
    
    This is only done on devices without /dev/alarm, which has its own
    in-kernel mechanism to pick the RTC.
    
    Change-Id: Ife2b342c3590133ed316ddaf1799cbc1bfa6e6d9
    Signed-off-by: Greg Hackmann <ghackmann@google.com>

commit f18da1cffb2e253b25718c88a09ac2e0df427fb2
Author: longyu.huang <longyu.huang@ck-telecom.com>
Date:   Sun Mar 22 21:14:58 2015 -0700

    third part apps can disable the secret lockscreen
    
    [Preconditions]
    set password or patten lockscreen
    
    [operating steps]
    1.install the app (eg QQBrowser) and connected wifi
    2.wait a while,the weather notification will shown on statusbar
    3.turn off screen,the weather notification will shown on lockscreen too.
    4.click the search bar in weather notification,it will disable lockscreen.
    5.press HOME button or kill QQBrowser in Recent apps,you can operate the phone
    
    Change-Id: I377aa8fa288beea857e578c7665286032e7645e1

commit 195efa2d73479d7ec243efadea979c2c82c962d7
Author: UtkarshGupta <utkarsh.eminem@gmail.com>
Date:   Wed Apr 15 10:44:07 2015 -0700

    Allow screen unpinning on devices without navbar
    
    Change-Id: Iedfc08f4d95bbee3c8578c0d2450b90739e63603
    
    Conflicts:
    	policy/src/com/android/internal/policy/impl/PhoneWindowManager.java

commit 25a96ee9580cebd8aa5a4b60436c91aabc3a4ee4
Author: Stevespear426 <stephen.k.spear@gmail.com>
Date:   Wed Apr 15 10:52:19 2015 -0700

    Make Navring available to devices with no navbar
    
    - Modified to work with our navbar ring customization
    
    Change-Id: I17eae46576c0e397b096ecf1dd64c2ac1bb30001
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 9e4669c200af2cdaceac22cb174162e4e353adfe
Author: LorDClockaN <davor@losinj.com>
Date:   Wed Apr 15 12:45:53 2015 -0700

    Theme fix for statusbar - future proof
    
    Always run update() on theme change
    Recreate statusbar on qs color switch
    
    Change-Id: I6f50c3e6d68d0daf8f3194c4e2706eea08ad657c
    
    Conflicts:
    
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/PhoneStatusBar.java

commit 9cc07ec178bf0832381f9bd2fc0bc0ed9703bd67
Author: westcripp <korukaltan@gmail.com>
Date:   Mon Mar 9 18:19:26 2015 +0100

    QSColors: Fix empty notification alert after switch color option
    
    Change-Id: I9935864579c0d9a3ac7a0758cda076dc71e2c9b4

commit f9fd1a1528ee5a8dc4174c19572ec438c329d6e0
Author: BestPig <bestpig82@gmail.com>
Date:   Wed Apr 15 21:18:25 2015 -0700

    QS: Update usb tether tile
    
    Conflicts:
    	packages/SystemUI/res/values/cm_strings.xml

commit e3f031cf21dd34dd6f8dfb27fe1e9ef543cf57d8
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Fri Apr 3 17:39:41 2015 -0300

    Framework: always update volumes slider state
    
    Fix a bug when volume slider is not updated when toogling ringer modes or changing Zen mode with expanded volume panel from Media playback
    
    Change-Id: I3f6c01320a53b6ea37abae9145d7d520d3ea46e0
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/volume/VolumePanel.java

commit acbdcacd1bbe36062a4ac7af5273562d7d227521
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Wed Apr 15 21:21:20 2015 -0700

    FWB: Add music tile (1/2)
    
    picked from here: http://goo.gl/ehaoMU
    
    Adapted to lollipop from commit:
    
    Author: kufikugel
    Quicksettings customizations Slim style
    d85304fac9bde550beeeeca0dba2cd49686f20d7
    
    Adapted double click to open music app from commit:
    
    Author: Jubakuba
    SystemUI: Pimp-up Media Tile (1/1)
    5a14de5db237969607e0aabb9b8c04737b122dd3
    
    AICPfy:
    PS1: Gave proper credit to kufikugel for the original code
    PS2: Fix build by overriding all needed methids
    
    Change-Id: I1d93c207a74d04ae0f6ee3d3c9c7ccf5f1444123
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/custom_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java
    
    Conflicts:
    	core/java/com/android/internal/util/cm/QSConstants.java
    	packages/SystemUI/res/values/cm_strings.xml
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/QSTileHost.java

commit 273b865279b849b582b8e907993e29e0792bfe95
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 3 14:33:37 2015 -0700

    Forward port CM Screen Security settings (1/2)
    
     * Variable size pattern lockscreen
     * Toggle dots/error pattern visibility
    
    Change-Id: Ie109e82c1fb2fd96b07e977e1cd76ae3acb865ff

commit fd8f2f90ee3703428ca1b852bbd7ebccfaa54141
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Apr 6 12:50:22 2015 -0700

    Add static patternToString() with pattern size
    
    Sometimes we need to generate a pattern string when lock pattern utils
    cannot query the actual size of the pattern. Add a method which doesn't
    depend on LockPatternUtils and accepts a pattern length parameter to
    generate the string.
    
    Change-Id: If73334b7030800bed2eec0cd0934b762b10dcaa3
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit e3bb0618f570fe3e287369e302f166347f2111f0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Apr 4 07:27:29 2015 +0300

    Fix pattern visibility settings (1/2)
    
    Change-Id: Ic627953c5df854c442671a98b5da539b994da18b

commit 2098db4ffe771f8d6a8ff6ec11a578f6f8e743af
Author: tobitege <tobiasteschner@googlemail.com>
Date:   Wed Apr 15 19:06:04 2015 +0200

    Prevent NPE with mHeadsUpNotificationView being null
    
    Change-Id: I70e2fc123f8bbf42ba579bfbf7dfa9bb097a6b4f

commit 39e0d1a48c4de26a4e0aea8c1cac3ce6737e811c
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Apr 15 18:16:24 2015 -0700

    Do not check mHomePressed on HOME in interceptKeyBeforeDispatching
    
    Repro:
     - Open power menu
     - Press home
     - Observe: does not go home
    
    Change-Id: I56cb33b95e2b7d5ee378b0e1b8ce7bc6bbd5e757
    (cherry picked from commit d2c7133f52cd20ce6afcff3d36c528775a24bab2)
    (cherry picked from commit 5db942f0045a2b6e863aa9fb3e77d424d147c315)

commit ec6d9572dac44ee058b913de2b32159be7e7db5b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Apr 16 01:28:40 2015 +0300

    Restore AOSP translations
    
    This partially reverts commit 498b1f7469a57b0543c2045d0e2966df1181e35b.
    
    Change-Id: I12db3e38061684dea1d55635c19ed5a1a7b5dc80

commit af927b356b5dd683e4d0ca8e11de0b36771a4f12
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:25 2015 +0200

    Automatic translation import
    
    Change-Id: I460224ba9600de61f44fb9950ca1d80ed7a12d4e

commit 81bbc278a366177ef225c8f6eeffba9b67f37552
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:47:23 2015 +0300

    Automatic translation import
    
    Change-Id: Ic47cf41913b709defdedd3a5b74ff40e0d096a95

commit be731c148a8bbdb0dc3684b1abc86ca75fa9a073
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:48:57 2015 +0300

    Automatic translation import
    
    Change-Id: I58ab7351fee181a2aa292a65d4496f676b99cbe0

commit df1b5e75494d284a8d72e46ea4b819d848efcbca
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 16 16:36:56 2015 -0700

    frameworks: fix reading default pattern size file
    
    Change-Id: Iad64cc7c664465cf9091e744a1ae5ed65a7b4ed6
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 64d79c909143ec6b89aaa39a702b1e84c1170931
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Apr 16 16:29:47 2015 +0100

    Base: update volume link option for 5.1
    
    This aosp patch changed the handling of volume sliders which has broken unlinking in settings app
    https://github.com/android/platform_frameworks_base/commit/bcc1087af40a0e1bb35dbe8a39c830ecdea8280b
    
    Fixed with this:
    [1/2] base: allow unlinking ringer with notification volume
    https://github.com/omnirom/android_frameworks_base/commit/359481c7c351dd4b5c5739afe877f41d2f20ea8e
    
    Also volume link option doesn't seem to be working properly
    
    Fixed with this:
    base: fix init of ringer/notification volume linking
    https://github.com/omnirom/android_frameworks_base/commit/c0fae397998268dd34e01c78118852ede6bb31dd
    
    Change-Id: I53dd13441cccc7fc618aec1fb038f8be62502826
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/95040/
    
    Conflicts:
    	media/java/android/media/AudioService.java

commit f49b0e976defd2523a293afce9d32762fcc43f6e
Author: maxwen <max.weninger@gmail.com>
Date:   Thu Apr 16 22:19:15 2015 +0200

    base: change zen mode condition thresholds
    
    -next alarm condtion threshold set to 24h
    -downtime condition threshold set to 12h
    
    Change-Id: Ie85492fa3b75df9a7c216da2872c2c6f40d58911

commit 32c5dabdd6c370031eff23aea7dc0b9a29df6b04
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Apr 15 09:19:09 2015 -0700

    SystemUI: remind user flashlight is still on
    
    Post a notification which informs the user the flashlight is still
    enabled. But only do this when the user turns the screen off *while* the
    flashlight is still on, so they see it next time they use the device.
    Tapping on the notification will disable the flashlight.
    
    Change-Id: I3689ff6498b97b813ccc10dc7dca3527fc8455aa
    Signed-off-by: Roman Birg <roman@cyngn.com>
    
    Patchset: 3
    http://review.cyanogenmod.org/#/c/94683/

commit a2d1f9f3e92fc76b8863698e404b88bca9b1618e
Author: Erica Chang <echang@cyngn.com>
Date:   Tue Apr 14 17:43:10 2015 -0700

    frameworks: display: Added automatic brightness configs
    
    Change-Id: I71ad7e08b0be56de959bbf06851944a97a97f620
    (cherry picked from commit 8ae0ee8d13e2711f3d48cd55f33e306431ed37ab)
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/94981/

commit 51a0b5888f9dc7de369f649881bdd7e266c11dd1
Author: UtkarshGupta <utkarsh.eminem@gmail.com>
Date:   Fri Apr 17 10:31:34 2015 -0700

    Mobile data tile: open network settings
    
    Long pressing the tile open network settings.
    More settings under expanded tile open data usage settings.
    
    Change-Id: I47a6eea35a4d427c70fe3a6dee3c0d198a431082
    
    Conflicts:
    	packages/SystemUI/src/com/android/systemui/qs/tiles/CellularTile.java

commit 8774ae7f4e81b065802fdcacfe432d705355b6e4
Author: Clark Scheff <clark@cyngn.com>
Date:   Fri Apr 17 10:10:17 2015 -0700

    Remove legacy ThemesTest
    
    Change-Id: I142448bd24d4b78b7d86f3b9cc27a39166d44b68
    (cherry picked from commit 2302da499f97e2ce82ff55ffb23f67befd854090)

commit daaaaa33c246cc17cc2edf045c6efdc61662315f
Author: Richard MacGregor <rmacgregor@cyngn.com>
Date:   Fri Apr 17 09:26:36 2015 -0700

    WindowManagerService not propagating X and Y steps
    
    WindowManagerService received X and Y offset steps but failed to pass
    them off to the relavent wallpaperservice.
    
    Change-Id: I532dedf2db055e27d6eca813e30346e37f52dc65
    (cherry picked from commit e03ea68d0a7f7d7c60663feae587225cca3a3a5b)

commit f2f8b6b9748f2ac0fa1462499aafc40c75977b16
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:17:40 2015 +0300

    Automatic translation import
    
    Change-Id: I0b56b263cf94258d123ed14bd6570b169f603f88

commit b6610300fbd01a0f4607613f27701ae3decb3b82
Author: abun880007 <tigger2014@team-ub.co.uk>
Date:   Sat Apr 18 02:18:51 2015 +0100

    PhoneWindowManager: Fix screen pinning averting soft reboot

commit c1a21a3d8b85e3a029dbc670ee26018909f89d24
Author: abun880007 <tigger2014@team-ub.co.uk>
Date:   Sat Apr 18 02:26:29 2015 +0100

    Bring back needsNavigationBar for compatibility

commit 272db9d86d5e0520aff808583f171735320c29c7
Author: Xiaogang Cui <xiaogang@codeaurora.org>
Date:   Thu Mar 19 17:10:39 2015 +0800

    restrict updateExternalMediaStatus to non-emulated storage
    
    The applications in emulated storage will be scaned by packageManager
    Service. Only updateExternalMediaStatus for non-emulated storage to
    avoid deadlock between MountService and PackageManager
    
    Change-Id: I53c8d269c478256abb8e397c0c2b3271e29e2ec7
    CRs-Fixed: 814188

commit 92ca4fb12ec9d99db21de06b43d93f799d0fd2cf
Author: Zhou Song <zhous@codeaurora.org>
Date:   Fri Mar 27 14:42:49 2015 +0800

    Avoid duplicated calling to isRestricted to improve performance
    
    isRestricted() is called every time in Play and setVolume API.
    Then it introduces some latency here, the perfromance can be bad
    especially when the APIs called multiple times.
    
    Initialize the permission check result in constructor to avoid
    calling to isRestricted.
    
    CRs-Fixed: 812386
    
    Change-Id: I1ce81d1723a6b29adf4117ac0ccb7a98850ef2dd

commit a5e52e33fde382a368207eaeeaa4c45f35b8c84b
Author: Tao Zhang <tazhang@codeaurora.org>
Date:   Mon Mar 30 12:07:47 2015 +0800

    Fix an apk icon animation corruption issue
    
    When several apk icons group together to a folder, the icons
    scale down to small icons first. Dirty region computation only
    respects the transformed small icons region. However, since the
    swap behavior is PERSERVED, the contents of larger icon region
    in previous frames are kept in the current frame, this region is
    not covered by the dirty region, thus contents of previous frame
    presents and it is corrupted. The fix is to include the in rectangle
    to enlarge the dirty region
    
    Change-Id: I546da255cf18b3c948e8491f3a513762d7dd4fea

commit 491604d6d3b15d87920bd718310b09d6b105484b
Author: Sandeep Kunta <skunta@codeaurora.org>
Date:   Thu Mar 12 18:56:30 2015 +0530

    Optimize IncallUI delay for voice calls
    
    In current implementation detectCountry method is called from telephony
    as many times as 34 for one MO voice call, causing increasing delay to appear
    incallui for user.  This fix ensures that there is only one call to
    detectCountry method per one voice call thus optimizing delay.
    
    CRs-Fixed: 803069
    Change-Id: Ia6e832476c7f7be2750f1c2d9a4c83f728c2131e

commit ed8bef8fb45ac88ce28f113cfa3ca6563342f4c2
Author: Paramananda <parama@codeaurora.org>
Date:   Tue Mar 24 14:40:01 2015 +0530

    frameworks : Extends mimetype list hence apps can view the media files.
    
    - MimeType of media formats (BMP, WAV, 3g2, m4a, mp3d) added in
      MediaFile, so the Gallery and Music application can view these
      media formats.
    
    CRs-Fixed: 804185
    
    Change-Id: Ibc43b9652e2886bba7838b0cab703c2474b21d6c

commit 0cd0073056d99cdabeab7867cb8fb634aff8a015
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Fri Apr 17 15:17:43 2015 -0400

    base: nat464X: Only update ipv4 pseudo-interface when it's connected
    
    On some devices, the network link state may go up even though there
    isn't going to be an active attempt to connect to the network
    due to other networks taking precedence.
    
    Currently, when this happens the network link is forced to attempt to
    connect due to notification sent to the ConnectivityService.
    
    Rather, let's wait until there is definitely an IP address and then
    notify it at that time.
    
    This solves a bad battery drain that occurs sometimes on victara
    when connected to WiFi due to the mobile data network going through
    constant connect/disconnect cycles.
    
    Change-Id: Iee390f948109b3412ec86d1b3c5fbc53a4859b7b

commit 217857a586b7fde017fcdef28e915e645f180a6d
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Tue Mar 10 15:10:25 2015 +0800

    SystemUI: Show operator name UI after getting valid operator name
    
    If phoneId is invalid, it will not set operator names. But the operator
    separator has been set when inflate CarrierText.
    
    Set the separator after operator names have been set.
    
    CRs-Fixed: 796371
    Change-Id: If6ab64105a2c6bcf040130c7b1c538936859a328

commit 7f77d0f7e6faa4a4bc76849d51d9e6b6125a7c87
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Thu Apr 2 17:44:34 2015 +0800

    media:Modify the display of system default ringtone when it is none.
    
    After we set the sound of calender use the default ringtone , if the
    system default ringtone is none, the sound of calender will show
    unknown ringtone.
    
    Make sound of calender not show unknown ringtone when the system
    default ringtone is none.
    
    CRs-fixed: 812323
    Change-Id: Idbc488748a81b88bb7a0df49e25d6a8cf6ba3826

commit ad43208f7d8758bd486e34da2a65f03600e78c87
Author: Maunik Shah <mshah@codeaurora.org>
Date:   Thu Aug 15 17:07:59 2013 +0530

    Screenshots info is not updated when device is plugged in MTP mode
    
    When device is connected as MTP mode and user opens folder
    /sdcard/Pictures/Screenshots/ in windows system and captures new
    screenshot, image information is always shown as 0 KB
    
    Issue: https://code.google.com/p/android/issues/detail?id=56204
    
    Change-Id: I46f3d72d275e164e40e305a3b5aafe685e6905f2

commit 122e010b4d4087f496bb963ab9222ed1acc97549
Author: elektroschmock <elektroschmock78@googlemail.com>
Date:   Wed Apr 15 21:45:11 2015 +0200

    frameworks/base: Zen mode add 10 and 12 hours downtime
    
    Change-Id: I80304c58e5e4bb23a556896aa9f6c325f313ad65

commit 3b1d8d5f5c59a0b749340b73100698167f38b3af
Author: Rama Vaddula <rvaddula@codeaurora.org>
Date:   Wed Sep 25 15:55:25 2013 -0700

    Remove opaque check in preparing dirty region
    
    Since preserve swap is enabled, we need to clear the color buffer
    when the scissor rect is prepared for a new process. This prevents
    garbage being present from the previous process in the color buffer.
    
    CRs-Fixed: 549755
    
    Conflicts:
    	libs/hwui/OpenGLRenderer.cpp
    
    Change-Id: Icd12ae388077b8c9ed329c37314e896500078543

commit 7c54f1c1ac07aefb4d7ac1436911c87cfed2197f
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Apr 20 14:48:38 2015 +0000

    Revert "third part apps can disable the secret lockscreen"
    
    This issue was fixed with 5.1 and is no longer needed.
    
    This reverts commit 672dca7fa64bb4122ae8a6d9ad815de38a4adf80.
    
    Change-Id: I9afd227b80c058ea22e44803c8410756e48ea3c2

commit 36fb965127cd60071283f0116f9eab63b8e5e600
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 16 17:27:56 2015 -0700

    AudioService: fix crash when no music player found
    
    Change-Id: I02a074a46a07384fef2ab6916663940214b62883
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit ee162c30b95f538c8d0817511c0ddbfa931d683e
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Mar 17 10:40:00 2015 -0700

    framework: add KillSwitch stubs
    
    Change-Id: Ie6cec065df0f821d9a5b8ab7bb3032fe7655389f
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 5734778b7fe5a3c999da67d722ceef97606dce86
Author: youngmin0822.lee <youngmin0822.lee@lge.com>
Date:   Fri Mar 20 21:22:32 2015 +0900

    Don't create unnecessary RenderThread's instance when executing 'dumpsys gfxinfo'
    
    To obtain the gfxinfo for each process, the static method of RenderProxy is used, which is named outputLogBuffer().
    In there,
    1. RenderTask is created for getting DisplayList Commands in RenderNode.
    2. staticPostAndWait() is called
    3. RenderThread's instance is created by 'RenderThread::getInstance()' in staticPostAndWait()
    
    In case of the service, they don't use HW Acceleration, so don't need RenderThread.
    But, by the process of No.3, RenderThread is created for all process.
    As we know, RenderThread never be destroyed while the process is alive.
    This patch checks RenderThread instance before the creation of RenderTask.
    And, there is no one, just return to prevent the unnecessay creation of it.
    
    Change-Id: I4fe29d83c9ced3e8b67177c0874c5d8ee62e1870

commit 44475334fd2341cca7b2d6ff96c0938eff77a59f
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 20 20:20:19 2015 -0700

    Revert: fix Notification volume slider linking
    
    Change-Id: I0f74485f5c8c2aa7698cf9ba1c60c2c8c967798d
    Signed-off-by: Roman Birg <roman@cyngn.com>
    Revert "Base: update volume link option for 5.1"
    
    This reverts commit 1542e7c65f8087191164b82f9824c2ed2243ea2a.

commit 1bcd001572000b9a44617199c7848383cf7b3574
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 20 20:20:46 2015 -0700

    Revert "Base: fix unlinking volume sliders (2/2)"
    
    This reverts commit 5c2f20cbd3d583292e8390e8d8972297d4ea2348.
    
    Change-Id: I796b8618d6f346787b0869ce9e92fbb61e526e1c

commit f1d7ef58d5882548f88f7e7bae94290a63f7c17c
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Apr 17 15:18:16 2015 -0700

    fix Notification volume slider linking
    
    Change-Id: I0f74485f5c8c2aa7698cf9ba1c60c2c8c967798d
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit ccb410bdc75e0b858f2c06f86ab81f4197b6e632
Author: Danny Baumann <dannybaumann@web.de>
Date:   Fri Jan 4 09:55:13 2013 +0100

    Fix HTC headset handling.
    
    HTC's headset driver adds additional bits to the switch state, which
    we're unable to deal with. Fix that by masking out those bits and
    keeping only the valid ones.
    
    Change-Id: I74b8091544fef518d142c4f5aea2eea48756f324

commit b02ac0d3e13c908bf623fab17c908e0a2e3c5d91
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Mon Apr 20 07:09:10 2015 -0400

    base: ConnectivityServer: Don't reap the new network
    
    When we add a network it may show up as unneeded while we are
    adding it and reaped as we are adding it.
    
    Reaping it immediately can happen before the captive portal
    check has completed.  This can then cause the network to get added
    again causing an unnecessary battery drain.
    
    Change-Id: I837f627c9f6d95bb8a021d2a58f5fc28564ef8b4

commit 1cb60243540f95205737ee2a88d4fd3ec4b30c6f
Author: Danesh M <daneshm90@gmail.com>
Date:   Thu Apr 16 20:00:24 2015 -0700

    ScreenCap : Add jpeg support
    
    Change-Id: Ibd5050c79774d06f30b2f668160cdeca75f1bc58
    (cherry picked from commit c1fd7edd8fc48f3308105df8cc845ec4b6652e17)

commit 8d6f7359cb90a3e2ebcbb6c7866c092c1e8e5fb4
Author: isimobile <corrie.meyer@gmail.com>
Date:   Sun Apr 19 16:59:47 2015 +0200

    Fix: In Afrikaans the unit name is not before size but after.
    
         We say 10MB not MB10
    
    Change-Id: I921f66b019321eb8cf608fef567031804d59c2a5

commit 9430decb4dae31f7f71e84381da73d8acba94641
Author: syaoran12 <adammfisch@gmail.com>
Date:   Tue Apr 21 00:31:46 2015 -0700

    Battery Bar [1/2]
    
    Change-Id: I6a12db17c61c7cc9a4b373a7cd8f810b5231309c
    
    	modified:   core/java/android/provider/Settings.java
    	modified:   packages/SystemUI/res/layout/navigation_bar.xml
    	modified:   packages/SystemUI/res/layout/status_bar.xml
    	new file:   packages/SystemUI/res/values/du_attrs.xml
    	new file:   packages/SystemUI/src/com/android/systemui/statusbar/policy/BatteryBar.java
    	new file:   packages/SystemUI/src/com/android/systemui/statusbar/policy/BatteryBarController.java
    	new file:   packages/SystemUI/src/com/android/systemui/statusbar/policy/Prefs.java

commit 8aa889cb519c804645039b5a74cf9b0bb7e08807
Author: darkobas <darkobas@gmail.com>
Date:   Wed Feb 4 11:31:15 2015 +0100

    make lockscreen weather fonts a bit smaller
    
    Change-Id: I7c1585541859385569893d7d67dfdc18845fa111

commit 8f7934e41ac6062f237c3576bc0a872b0818bd4b
Author: beanstown106 <nbenis106@gmail.com>
Date:   Fri Apr 17 20:57:52 2015 -0400

    Fix batteryBar on Navbar
    * this fixs the dual navbar battery bar when its supposed to be hidden and makes it work as intended
    * this also breaks statusbar tests need to spend some time solving this in java here https://github.com/PurifiedRom/android_frameworks_base/commit/39e80d24d28ac2026ff9dd3f7c832b6f489fe404#diff-ca2883aa3b534f5a1db5e0789780cf18R86
    * proper fix would be to have it look for xmlns:systemui="http://schemas.android.com/apk/res/com.android.systemui which is what the statusbar uses and xmlns:systemui="http://schemas.android.com/apk/res-auto which is what navbar uses
    * we dont run statusbar tests so it isnt a big concern at the moment
    
    Change-Id: I2d38abe449c7839b04278e8dfb965777554f6e5b

commit 649e4ddf5057cd04b8732f718f2bcf5495ca0c55
Author: Alexander Westphal <westphal.alex94@gmail.com>
Date:   Wed Jan 28 03:01:04 2015 +0000

    SystemUI: update quick settings profiles drawable
    
    Change-Id: I7063ef56f4e56ad4424ec6f8902f9f6755a3b1dd

commit a8e80f6e0525bd89f96a063d92697694eff48433
Author: Ruben Roy <rubenroy2005@gmail.com>
Date:   Fri Mar 13 21:20:48 2015 +0530

    SystemUI: update power menu profiles drawable
    
    Change-Id: I1dd24c0b3c26c4f3a6c5fafaf5d679906c8acce9

commit ab62ff53273eb3510e5727ad65aaf655cbba1459
Author: Marco Nelissen <marcone@google.com>
Date:   Wed Mar 11 09:59:49 2015 -0700

    Fix context leak
    
    Using an activity context with AudioManager could cause that context
    to be held on to longer than desired, for example if the caller
    acquired audio focus but never abandoned it. Fix acquire/abandon in
    VideoView, and use the application context in AudioManager to mitigate
    the issue for other misbehaving code.
    
    Bug: https://code.google.com/p/android/issues/detail?id=152173
    Change-Id: I0fb8390207422c784800dda25b1f2c03d4574bcd

commit 5badab5b2980c4f7de28a902c5deded5341dc352
Author: Marco Nelissen <marcone@google.com>
Date:   Fri Apr 17 09:50:56 2015 -0700

    Sometimes the application context is null
    
    when called from systemui.
    
    Bug: https://code.google.com/p/android/issues/detail?id=152173
    Change-Id: Ic7b98e39fd9ad2436b855cf9f7f53d3e7a1948c0

commit 03b64a22845d2af94fb38cc8f9335c8e5cc07724
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Tue Apr 21 15:51:13 2015 +0200

    AudioManager: update references to application context
    
    Change-Id: If458c17c44bc68f1a0c4172b11240e2053fad42e
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>

commit c57c19948ac7924f585b300d2932878e5afcd68a
Author: Evisceration <alexander.martinz@nameless-rom.org>
Date:   Mon Jan 5 22:20:05 2015 +0100

    PowerProfile: allow overriding default power profile
    
      * override it with ro.power_profile.override
    
    Change-Id: I2b229822b18a54060d577f25c0ddaf5b7e7563b7
    Signed-off-by: Evisceration <alexander.martinz@nameless-rom.org>

commit 5feb6ef93bfce895977b2f1ca74d7e01868c7258
Author: riddle_hsu <riddle_hsu@htc.com>
Date:   Thu Apr 16 11:36:23 2015 +0800

    [ActivityManager] Avoid unnecessary restart provider process
    
    Caller C accesses provider P. Both processes of C and P died
    before P publishes, P will still be restarted even there is
    no connection because P is in mLaunchingProviders.
    When device is low memory, the restarting provider process
    may be killed easily before publish because no caller to raise
    its oom-adj. Then device will busy keeping restart it.
    
    Solution:
    If there is no connection to the provider, do not restart it.
    
    Change-Id: If6f2d2258d78b6c0989c6e5f3e0cad14db821464

commit a4ace087ff05db6964d3e091498d1a402e0eb612
Author: Alex Klyubin <klyubin@google.com>
Date:   Mon Apr 20 10:11:57 2015 -0700

    Make MediaPlayer fail fast on UnknownServiceException.
    
    This makes MediaPlayer's network streaming code fail fast when an
    UnknownServiceException is encountered. This currently occurs when the
    application declares that it does not perform cleartext network
    traffic and tries to load media over cleartext HTTP. Without this CL,
    MediaPlayer blocks for 30 seconds because it treats this error as
    recoverable and goes into a ten retry loop with a three second delay
    before each retry.
    
    The result at MediaPlayer client level is
    MediaPlayer.MEDIA_ERROR_UNKNOWN error. This error code is used for
    non-recoverable situations such as when an invalid redirect is
    encountered or the destination is unreachable.
    
    Bug: 20026006
    Change-Id: I10f0dadb7740902f8c7c73d0df96cfff31f08ada

commit 97347f00e96484c66e16c50d15aa2e51447a4359
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Apr 21 14:11:20 2015 -0700

    SystemUI: option to disable lock screen shortcuts (1/2)
    
    Thanks to chezbel and LorDClockaN, inspired by these commits,
    
    https://github.com/AICP/frameworks_base/commit/b7ca169b52a78fdd63e437a26f4e89124e4f9fe3
    https://github.com/AICP/frameworks_base/commit/c530b66af323c6088caad76ef10304bfaeede8e5
    
    Change-Id: Ie05f148511324441db211f62d3007bf2c5249822
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java
    
    Conflicts:
    	core/java/android/provider/Settings.java
    	packages/SystemUI/src/com/android/systemui/statusbar/phone/KeyguardBottomAreaView.java

commit ff9b1f626c7d97400045d7e628314616eec013bc
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 12:21:41 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/frameworks/base into cm-12.1
    
    Android 5.1.1 release 1
    
    Change-Id: I8fc77b035286a4e21663b1dc1be774291e138035

commit 80a6a21d36b367ad7e2ce49d6bf2ecb94d523913
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Mon Apr 20 05:27:18 2015 -0400

    doze: Do not bother checking proximity for the DOZE_ACTION intent
    
    The intent is a desire to show the intent and trust the sender to
    determine whether or not it should really be shown.
    
    Change-Id: I1c613071b136de61f12bc0556283a80e1248a4a8

project frameworks/native/
commit 453e91c817b8a04367736aa11212cf7a5a854c29
Author: ywen <ywen@codeaurora.org>
Date:   Thu Mar 26 19:51:12 2015 +0800

    Fix a memory corruption issue when vector resize
    
    There is memory corruption in below code
    
    const Rect* prev = &dst[prevIndex];
    dst.add(Rect(prev->right, top, right, bottom));
    
    prev points to a memory of vector dst, when dst resize in add()
    call, the memory that prev points to will be copy to the new
    allocated vector memory and the old memory will become undefined
    
    Avoid pointer in this case, use a local copy instead
    
    Change-Id: I4d95ceedd00c8fb615ac153082ade1b1ce0d0fa8

commit 8d1ccdb92d401375f3b54b1647addcee9dcc2af8
Merge: 2d921f3 453e91c
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 00:10:03 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit eb229905b6d45dadfd2ab1891990e71c3b8cea55
Author: nadlabak <pavel@doshaska.net>
Date:   Fri Apr 17 00:55:53 2015 +0200

    Support WAKE flag in keyboard layouts
    
    This flag is used to specify the internal keyboard keys allowed
    to wake the device.
    
    Change-Id: Ic15aca1134206c9b006a4d97dded10bccae640d3

commit 521ce7b9075972a7e131d7f1fbab7f3a3c1a8b0f
Merge: 8d1ccdb eb22990
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:45:13 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project frameworks/opt/telephony/
commit 76e8804a224dbb13aeea0ad4df25ef8ac34fdca7
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Thu Apr 2 19:38:01 2015 +0000

    Revert "Telephony: DcTracker: Fix CDMA APN Data issues."
    
    This reverts commit 40126c0a4055ed3a467b8d878391a5b1c1c1de41.
    
    Change-Id: Ida9da3fafd4aa4896a50e2e17a2199adb71bdc02
    (cherry picked from commit 3a252149cbe75e5d28977e7f311bff329ba4fe10)

commit a4e187acedde8e2daa17c29263c763ce35f2be96
Merge: 0dff479 76e8804
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:15:24 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project hardware/invensense/
commit cd02255a2244eda445cd01f58f159acdc993d586
Merge: b155ab8 3c9a4d3
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:19:11 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/hardware/invensense into cm-12.1
    
    Android 5.1.1 release 1

project hardware/qcom/display-caf/msm8974/
commit ca83f3330e965a810feb8d35638d903f60c420ef
Author: Raj Kamal <rkamal@codeaurora.org>
Date:   Tue Oct 28 15:31:35 2014 +0530

    hwc: Try MDP composition eventhough skip layer is present
    
    * Explore cachebased and loadbased composition strategies
    eventhough skip layer is present in the layer list.
    
    * Prioritize loadBasedComp over cacheBasedComp in such case.
    
    * Invoke redraw of FB for every-frame as long as skip-layer
    is present to comply with the spec.
    
    Change-Id: If105ae8af4888a1e0b0fb824c526ef5a1adaedd8

commit f48658370b1f005cb58fe8367c1bba29fc85deca
Author: Saurabh Shah <saurshah@codeaurora.org>
Date:   Tue Feb 17 09:57:47 2015 -0800

    hwc: Integerize in the outward direction of rectangle
    
    Currently HWC integerizes float source co-ordinates (l, t, b, r) in
    the inward direction, mimicking SF from pre-HWC-1.4. In case of
    upscale where we need to create more destination pixels than incoming
    ones, this chopping off can lead to quality issues, especially given
    that the error magnification can be as much as 20x.
    
    This change integerizes the source rectangle in the outward direction
    which will help magnification cases. Downscale cases should be
    unaffected since reduction hides errors, unlike magnification.
    
    Change-Id: Ib72a1f8d52f4ec800387bfe2b91c9d3a65e6f557

commit 5c1f3ab565fac5845373341953d88cbdb93b7f7e
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 14 23:31:16 2015 -0700

    hwcomposer: Kill some logspam
    
     * Remove logspam when trying MDP composition with skip layers present.
    
    Change-Id: I76376e39a212c8ae8dd62e989a370357df16e622

project hardware/qcom/media-caf/msm8974/
commit 750f79f208a19f6cda469658ad28d425cc8067f1
Merge: 44a53e4 c61def6
Author: Linux Build Service Account <lnxbuild@localhost>
Date:   Wed Apr 15 06:47:40 2015 -0700

    Merge AU_LINUX_ANDROID_LA.BF.1.1.1_RB1.05.01.00.042.030 on remote branch
    
    Change-Id: I39efa9466b20553cfca6694ae0d41881da229199

commit fac0a22231a57a62007344ec84ea338b520b7b3a
Merge: c38861e 750f79f
Author: Steve Kondik <steve@cyngn.com>
Date:   Sat Apr 18 01:57:41 2015 -0700

    Merge branch 'LA.BF.1.1.1_rb1.19' of git://codeaurora.org/platform/hardware/qcom/media into cm-12.1

project hardware/qcom/media-caf/msm8994/
commit d062bc0fbb44b668de3649e0d4ce3a7596f9aa37
Author: Steve Kondik <shade@chemlab.org>
Date:   Tue May 6 03:22:11 2014 -0700

    media: Avoid collision with FFMPEG plugin
    
    Change-Id: Ica2cdf9f6572ec18f396d25758cbb2be1359ac0b

project packages/apps/AudioFX/
commit 6a73a02a70d8c352b4864be0a85a3421c9c85469
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:29 2015 +0200

    Automatic translation import
    
    Change-Id: Id5896de688909e7c308c741a1f7966292483edf4

commit 5269e1c2f7179a9fb5672fbd19acc24c3f685c12
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:41 2015 +0200

    Automatic translation import
    
    Change-Id: Ibddd44e05993457534b6bc9ec11c99767b54c641

commit 7d7975726aeb730efbc6589c396a846db5e3ae04
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:13 2015 +0300

    Automatic translation import
    
    Change-Id: I2ac8c8e442b1e904e7476e78e475eac7597c1de2

commit 6d9442fe4f548152fb337fbcaba212ddfc9bced7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:49:16 2015 +0300

    Automatic translation import
    
    Change-Id: I3bc96a51d3b6fcba3a17fb6997a35fdd85262d03

commit c0a4cfa0c11543e586c8bdc06e3bb67ab0cbd760
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:17:51 2015 +0300

    Automatic translation import
    
    Change-Id: I1aaf4bc1ca4e5b725383ec8c0d8105403efc749b

project packages/apps/Bluetooth/
commit d2f6cfa5c75bbe71eac16a28d55bc92b638bbbcb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:35 2015 +0200

    Automatic translation import
    
    Change-Id: Ie2675992cd5ba2d38202e46c658667e79837516e

commit 6d9183b67769770a3394d1085c71af97a418dafd
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:45 2015 +0200

    Automatic translation import
    
    Change-Id: I617de6eedc9236b34bc90d8873c093d53eb8ff0e

commit 58a28f74114b67d24ce02222deb61e6eab047064
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:17:55 2015 +0300

    Automatic translation import
    
    Change-Id: Idf8ec9dcb0ff1f2a8138111d4d779bebd7929f5f

commit 208cef99ca75cdeeba019f9c25d604e07c547f70
Author: Szymon Pusz <szymon@pusz.net>
Date:   Tue Apr 21 20:36:40 2015 +0200

    Bluetooth: fix StaleDataException when pairing with other device
    
    This fixes a crash when pairing for example with car audio that reads sms/mms
    FATAL EXCEPTION: BluetoothMnsObexClient
    Process: com.android.bluetooth, PID: 1944
    android.database.StaleDataException: Attempted to access a cursor after it has been closed.
    	at android.database.BulkCursorToCursorAdaptor.throwIfCursorIsClosed(BulkCursorToCursorAdaptor.java:64)
    	at android.database.BulkCursorToCursorAdaptor.getCount(BulkCursorToCursorAdaptor.java:70)
    	at android.database.AbstractCursor.moveToPosition(AbstractCursor.java:197)
    	at android.database.AbstractCursor.moveToNext(AbstractCursor.java:245)
    	at android.database.CursorWrapper.moveToNext(CursorWrapper.java:166)
    	at com.android.bluetooth.map.BluetoothMapContentObserver.initMsgList(BluetoothMapContentObserver.java:405)
    	at com.android.bluetooth.map.BluetoothMapContentObserver.registerObserver(BluetoothMapContentObserver.java:334)
    	at com.android.bluetooth.map.BluetoothMnsObexClient.handleRegistration(BluetoothMnsObexClient.java:238)
    	at com.android.bluetooth.map.BluetoothMnsObexClient$MnsObexClientHandler.handleMessage(BluetoothMnsObexClient.java:107)
    	at android.os.Handler.dispatchMessage(Handler.java:102)
    	at android.os.Looper.loop(Looper.java:135)
    	at android.os.HandlerThread.run(HandlerThread.java:61)
    
    Change-Id: Idea00c396c2512480befbf262571c8d8242e4af7

project packages/apps/BluetoothExt/
commit 8fa4753006de49d4eea43e2f8df1f81046bf6f6e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:39 2015 +0200

    Automatic translation import
    
    Change-Id: I0dbd3486f50f9c10cc9af3ea0b2dc353efa5d34b

commit 2c1c39e349d17bbcc6df097b7568aa6ca51ee532
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:50 2015 +0200

    Automatic translation import
    
    Change-Id: I9dff58e5a6f8bae8da50b4321c23689ddf87551e

commit 8c3e44fe5752f8367e53e4e9faac0c23e692db0b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:21 2015 +0300

    Automatic translation import
    
    Change-Id: I7683ee1bc96195e700c04e96f833cef5dd9f38aa

commit 15941923cf7d1b4244fd4d80f574e4b4c3028ee0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:49:22 2015 +0300

    Automatic translation import
    
    Change-Id: Iac4b1392dfe708534088450d5ccb420c2cc36be6

commit d153ec9dea28625673e805df49b71a5f55ce2ad7
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:00 2015 +0300

    Automatic translation import
    
    Change-Id: I14affc286912e6ada2c09e0808ccfac611ab3fa3

project packages/apps/Browser/
commit 1af979bc0bd53d9a0a35659483b05a606f5f6deb
Author: dcalandria <dcalandria@gmail.com>
Date:   Sat Apr 18 14:14:06 2015 +0200

    Enable immersive full-screen video playback
    
    Change-Id: I8ef22334c438b6b753e8e336af65f471446f80b4

commit 97ed99b6318e8db15339445be9e4309c122cf9b6
Author: chenghe.zhang <chenghe.zhang@ck-telecom.com>
Date:   Tue Apr 14 13:21:30 2015 +0800

    [BugFix][Browser]Can't download music from music.baidu.com
    
    [Solution Description]
        Can not download music from music.baidu.com
        The Referer is Empty
    
    [Other Info]
    
        modified:   src/com/android/browser/DownloadHandler.java
    
    Change-Id: If696c2ace282ec01f95476a9907fd6c7303bfb9c
    (cherry picked from commit 2db66392f651d0b306e9921a9b005c6ed1361428)

commit 7ae2b9299711d41f9f29b86253b501efd76fb6ad
Author: dcalandria <dcalandria@gmail.com>
Date:   Sat Apr 18 14:14:06 2015 +0200

    Enable immersive full-screen video playback
    
    Change-Id: I8ef22334c438b6b753e8e336af65f471446f80b4

commit c31db6266ea48bf053a411310afc614c0daff0b4
Author: chenghe.zhang <chenghe.zhang@ck-telecom.com>
Date:   Tue Apr 14 13:21:30 2015 +0800

    [BugFix][Browser]Can't download music from music.baidu.com
    
    [Solution Description]
        Can not download music from music.baidu.com
        The Referer is Empty
    
    [Other Info]
    
        modified:   src/com/android/browser/DownloadHandler.java
    
    Change-Id: If696c2ace282ec01f95476a9907fd6c7303bfb9c
    (cherry picked from commit 2db66392f651d0b306e9921a9b005c6ed1361428)

commit dd822c529daaeba0bdf652b54f28585000b24ca5
Merge: c31db62 97ed99b
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:52:08 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/CMFileManager/
commit d32899c3ee184b53001168113142e6a0ecf8850e
Author: jing.zhao <jing.zhao@ck-telecom.com>
Date:   Wed Apr 15 18:13:28 2015 +0800

    [CMFileManager] Always display searching progress after back to the search result view
    
    1.Go into the root directory, click the search icon and input the directory name(Such as: dlt).
    2.In Search results view, you can see the dlt directory, then click the directory.
    3.press back key, back to the Search results view, the lower right corner's searching progress has always show.
    
    After Seaching, the searching progress shouldn't show.
    
    Change-Id: Id1a3291effcebcd7c9536dec74175d6d019e83f1
    (cherry picked from commit 37e947a354edad76d4e91258b535c4658b54e2e9)

commit 52a26abf0ca6e671dcc2e1125640590f1816179a
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Tue Jan 27 15:27:12 2015 -0800

    Support RTL layouts everywhere.
    
    - Fix custom title text clipping.
    - Fix breadcrumbs
    - Remove FSO Dialog permission spinner width adjustment that did not
      function on RTL.
    - Fix history and bookmarks items to align properly.
    - Update layouts to function with RTL
    
    Change-Id: I3cd4032887371509ec2847bae6f889558664a356
    (cherry picked from commit d0d367d2d681e2372813a81246dea45eab572ce2)

commit 3274036619fc05be506226906bff0686c90cfd50
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:49:37 2015 +0300

    Automatic translation import
    
    Change-Id: I1bdbe31959ec6bf2c0bb4b56a61127b6e2ab3722

commit 21d641ccee97ee011ea2587808c2cb78c435144a
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Wed Apr 15 15:33:25 2015 -0700

    Implement a dialog that warns the user that we must expose the content of the file
    by copying it out to an unsecure location in order to allow the external applications
    to read the files.
    
    Change-Id: I163ccd21678f413170e44cf3e8d341cd4747b1ac
    (cherry picked from commit 58928e7facbdd63d4320748b277e94417fe402bb)

commit a09cb8fa69295e992c0ae9dadaa64260fd4cc82a
Author: jing.zhao <jing.zhao@ck-telecom.com>
Date:   Fri Apr 17 09:22:02 2015 +0800

    CMFileManager: Printing preview content is not show complete.
    
    fix the PageCount from int to double
    
    Change-Id: I72f1577f22b563456b43dded4058572d328009c3
    (cherry picked from commit ed63368d1d085d4021329d6720ab7a32765b7768)

commit 519978754ed72ca09926ad3e59a73782ace8fea0
Author: kai.cao <kai.cao@ck-telecom.com>
Date:   Tue Apr 14 16:42:27 2015 +0800

    CMFileManager: Fix CMFileManager display "sdcard1" and the content is null after adding a new user/guest
    
    step:
    - new user or guest in Settings
    - Go to CMFileManager and check
    
    Change-Id: Id6da696b8173f0544a022bc5e3d64d94b7123526

commit 59d323359657313659cb00bb59fefaef8e4d9f5c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:33 2015 +0300

    Automatic translation import
    
    Change-Id: I7afd40a46444c017c6dffbc9f8f5a057003c4d26

commit bc512126fba71e2f76d49e8a07cf0c353c4b1763
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Fri Apr 17 12:36:21 2015 -0700

    Make the new filename max length error message show.
    
    Change-Id: Ic997110fb78d253c7d3602a5b81157fceb9f73b2

commit 9fe55d253a619da925cfaedd34aeb0aff5eb641c
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Fri Apr 17 16:39:32 2015 -0700

    Enable ok button, filename is still valid.
    
    Change-Id: I38f3be02e60597a169850c2a47127dac5784236c
    (cherry picked from commit 16b30c40f8164c760d0e40c00e19bcc4dac67ccf)

commit 226460f8724fdc3f74e59e92862dd88087385b70
Author: kai.cao <kai.cao@ck-telecom.com>
Date:   Thu Apr 16 10:55:34 2015 +0800

    [CMFileManager] Fix the filemanager can copy parent folder to child folder
    
    Procedures
    1.Go into filemanager and select a directory(such as Music).
    2.enter the Music and copy the folder.
    
    The filemanager stay in "copying" interface.
    
    Change-Id: I9a765d1d89c4736b26d57bdf99237f04a810f254

commit 6e0bd517472876ddd47ed1a8aae8ba14a0d9982e
Author: jing.zhao <jing.zhao@ck-telecom.com>
Date:   Mon Apr 20 09:32:50 2015 +0800

    CMFileManager: After change language, the navigation view item summary doesn't change
    
    [The System Language is Chinese]
    1. open the CMFileManager Application.
    2. press home button and goto Settings to change the System Language from Chinese to English (can change the others).
    3. open the CMFileManager again, Click "All" , you can see the item's summary doesn't completely change.
    
    Open the CMFileManager, After change language, the item also will change.
    
    Change-Id: I40969d98718463996c34951effef50fa4e42c4ec
    (cherry picked from commit 10a073ee66dfe862804b2c2a39f93662bc554599)

commit fac93c143504c9f50899177e3660afc4433273d1
Author: jing.zhao <jing.zhao@ck-telecom.com>
Date:   Mon Apr 20 17:54:14 2015 +0800

    CMFileManager: when cancel coping, the dest file also exists and is incomplete.
    
    When cancel coping, will delete the dest file.
    
    Change-Id: I0acf7cc196dec82ed2156e9706c1364922581cdf

commit 34f4d1c880bd78482f6fa9dfc701692b8504ffd6
Author: kai.cao <kai.cao@ck-telecom.com>
Date:   Tue Apr 21 15:01:59 2015 +0800

    [CMFileManager] Fix the DrawerLayout don't disapper after press back key.
    
    Procedures
    1.Go into filemanager and enter a directory(such as Music).
    2.Open the menu Button in the top left corner and popup the drawerlayout.
    3.press the back key.
    
    The DrawerLayout don't disapper and the navigation view back to the next higher level.
    
    Change-Id: I13c78491e2be767e7611d57c2c513013d96465eb

commit 411c731b38559b1e76e795f3140ad8c19d471be1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Wed Apr 22 03:13:18 2015 +0300

    Improve string for crowdin
    
    * Unnecessary line wrapping appears bad on crowdin
    
    Change-Id: I75b4e81f85b2d3cf5aef960e3be4e3b4881dad91
    (cherry picked from commit 164c3d9e6e5a1a8fe5d82fc5027820655165cf77)

commit ebd0462a7320bf093d0209cfbbfa290df28cee69
Author: kai.cao <kai.cao@ck-telecom.com>
Date:   Tue Apr 21 15:21:01 2015 +0800

    [CMFileManager] Fix "File Manager isn't responding..." pops up after tapping "Secure storage" in File Manager
    
    Procedures
    1.Go to “File Manager”.
    2.Press "Menu" icon on upper left corner,and then tap "Secure storage".
    3.Select "CANCEL" when the note "Create storage" pops up.
    4.Repeat Step2 again,check the phone
    
    Have no response when pressing "Secure storage",wait about 10-20s,the note "File Manager isn't responding..." pops up.
    
    Change-Id: I8ce4b55002d6fc34f89c4a59404469e7f3637cbc

project packages/apps/CMRemixCenter/
commit c428bcd643eeb2553714f5dc1f2554eb37ed2c95
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 18:04:32 2015 -0700

    add cmremix icon

project packages/apps/CMWallpapers/
commit 6037263b138c555e4dc33d2e976aa5d4119810f9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:30 2015 +0200

    Automatic translation import
    
    Change-Id: I09dd54fae2276df2e6da5d3ac3516fcd91c5f376

commit b2000ea4a64b84269c294aa2564d72cf856a2c90
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:44 2015 +0300

    Automatic translation import
    
    Change-Id: I9637a678aa7cec42240ecbd257a56af5907de54f

project packages/apps/Calculator/
commit d5ec5ce2e8345738f51421e881f5b0b12edb34ff
Author: Roman Birg <roman@cyngn.com>
Date:   Wed Apr 15 15:45:15 2015 -0700

    Calculator: fix color lookups in GraphView
    
    Change-Id: I768b21cc4a1181a275a17b9e7d2bc7891e440afe
    Signed-off-by: Roman Birg <roman@cyngn.com>
    (cherry picked from commit b628c66d2337f468f147f250e2f5979325b875f7)

commit e1233e750e60f142d27aad97cf6898cf3d717bbb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:44 2015 +0200

    Automatic translation import
    
    Change-Id: Iea408b84d3ac9048ae0a9890ead56d8b270ef500

commit 70f3f8fd2cbdf95321524bf7a82ecbddf72d05b5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:54 2015 +0200

    Automatic translation import
    
    Change-Id: I0ba831e46e0d2ed6956e8cd8bb460f91e271f33e

commit 78a6e11ca5bd6621c2d563d1c7585437a9e0cf0c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:28 2015 +0300

    Automatic translation import
    
    Change-Id: I28cb2066b789d137530a09c60065c2837a4d614a

commit ed0ac3ed02ba9492f161239ead5bdc2d814fc931
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:04 2015 +0300

    Automatic translation import
    
    Change-Id: Iebb3c709aede752a60f6f0385800e5677d6f09dd

project packages/apps/Calendar/
commit ebccbe95a0a490cbd37138dc44665bd304251cd4
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Apr 14 17:52:24 2015 -0700

    Calendar: do not auto save events when importing
    
    Change-Id: Ia359592ef99becab0fda94a938e5cafd639eaebb
    (cherry picked from commit d276a6b69d1d1751176ed84a40d9b13ba63b476b)

commit 9217f73e25d469761c2219fb2c3793d5284b2e3f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:49 2015 +0200

    Automatic translation import
    
    Change-Id: I7890752036c3f6c12cf897c855303e39c8f162f9

commit ac3e7b88a03a0bf698cca2dcb8a99c94e9eb6a71
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 19:59:58 2015 +0200

    Automatic translation import
    
    Change-Id: Ib83a450f3a8b417a9605b4ec62d77994560b59ee

commit ff31c0c1662d81be0f5859fcbad8fe76c46dfdc2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:41 2015 +0300

    Automatic translation import
    
    Change-Id: I481b993408c8583b2d413e41bed2b38ad63c8afe

commit ff25d810b58fc6a03cdf2fa11ea391f2fb222ed1
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Mar 11 18:04:08 2015 -0700

    Calendar: add feature to select/deselect all events in delete view
    
    Change-Id: I1301d921474d848d6c877eb904bd7a00df13c48a

commit c1a1be68550f8d1248998ba0f20f8c96d887c222
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Fri Mar 13 16:53:39 2015 -0700

    Calendar: support ACTION_VIEW instead of ACTION_SEND
    
    Change-Id: I9b7608a9161b1370a4ee4ab520c0e0e9a0fd9c9c

commit 18fd6fcbf898c3490a4a93740e8462e5f0dacdd1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:12 2015 +0300

    Automatic translation import
    
    Change-Id: I2930b60170000312ab90a4a667fdde22171363c4

project packages/apps/Camera2/
commit 221eac31a16b5e953811af668c612c4372d09dac
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:46:55 2015 +0200

    Automatic translation import
    
    Change-Id: Ic0ffbc7f6a7198ea341425c966fc238d42721058

commit c7f1f8f60222e444a3c5e7bc2b435caf6629dd4f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:03 2015 +0200

    Automatic translation import
    
    Change-Id: Ic5c4377523ddce6ff54aed6032bb46cd3377f36b

commit 41427a00cfad90f35bdfafecc2bb4970397eb70e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:48:51 2015 +0300

    Automatic translation import
    
    Change-Id: I685a9acbcc6a2c99e20bc0ab68db574000d488db

commit 013f3942d160f7338a268b61a84354355b23f96b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:18 2015 +0300

    Automatic translation import
    
    Change-Id: I297d6266012a7b7eb08d1f3f45db4b7687608625

commit 6ab7ff45d7d041d51a3cd1fe51da5e37feac638c
Author: maxwen <max.weninger@gmail.com>
Date:   Sun Jan 4 18:15:53 2015 +0100

    Camera2: readd storage selection support (1/2)
    
    Change-Id: Ic7ee42ea1128ff0537b457946ffcc9bbdaad6c9b
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/91147/

project packages/apps/CellBroadcastReceiver/
commit 298f2a3e0a4f407fe6157e0750a68454b382aba2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:00 2015 +0200

    Automatic translation import
    
    Change-Id: I12ec8301573c3bdf604571ea33d90f5e496dd1dd

commit ca08c5c2a107fea58ba362f20947a5b767cdd4d2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:08 2015 +0200

    Automatic translation import
    
    Change-Id: I5487203e5e040a4e09ccef8a61ab64e1960c2cfa

project packages/apps/Contacts/
commit cfab2871d81f90fdf485224a353af83094da003e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:49:45 2015 +0300

    Automatic translation import
    
    Change-Id: I29826c35f016619dc01d73618d4bfe9ab13e4380

commit 2f2ce950119c6bfc8cb72da91b743fb9e0aa0432
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:49:46 2015 +0300

    Automatic translation import
    
    Change-Id: I6582d6fe8f746e82770e3077157db895039f94a9

commit daa7f84469a152f0b56c005a97cbf252a161f343
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:48 2015 +0300

    Automatic translation import
    
    Change-Id: I7b3e3a3e7cb4330a516d6594c43b5424957f3687

project packages/apps/ContactsCommon/
commit 0e556861fd113847feca6cc0e4dd23485259a7a6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:54 2015 +0300

    Automatic translation import
    
    Change-Id: I16e141e16792eda3e6854fd9a77d3335465a43ce

commit 5dd21a4467ffa6fae7bd5cca12164553a51a9dd7
Author: linuxxxxx <joey@cyanogenmoditalia.it>
Date:   Fri Apr 10 16:19:03 2015 +0200

    [3/3] ContactsCommon: Smart Dialer
    
    Put on your ear, and this will automatically call current number in message or dialer
    
    Change-Id: I27b5d379400d7d00b3a07a411d66e319b456eb4d
    Signed-off-by: linuxxxxx <joey@cyanogenmoditalia.it>

project packages/apps/DeskClock/
commit 2ae629800ed051c02957b5ee2c443960150c6a63
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:37 2015 +0200

    Automatic translation import
    
    Change-Id: I213fee9f3009771a35b5a48c3ea4037b167b07df

commit f27d89b26d7e6612b78511eba2ea9f50e9d81795
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:45 2015 +0200

    Automatic translation import
    
    Change-Id: I2aa7ca953980f1983cbcb65a53dba4d03ee3cb70

commit a9164e0feec6c1a5e5f8239a5d645de228c9e815
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:49:54 2015 +0300

    Automatic translation import
    
    Change-Id: I61edf4f84b6955e0622923d25e3a793461da8bba

commit ec842069cd6b68f6e98a0bbe091003cef030a7d5
Author: Martin Brabham <optedoblivion@cyngn.com>
Date:   Wed Mar 25 15:31:42 2015 -0700

    Hide flip setting if the phone doesn't have the required hardware sensor.
    
    (╯°□°)╯ sʞɔolɔ
    
    Change-Id: Iba38e37bffe91d0d5bd9bb8922b4c168386ebfd9
    (cherry picked from commit 106cfa2bca37303a93e1826c04d88783aa15b52d)

commit afee1d050b0a445e681ec16064b59989440927b8
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:18:59 2015 +0300

    Automatic translation import
    
    Change-Id: Ic759c91e323fb7aca533d3146ad663c3c6c7c59f

commit 8ff1508c8245d3b74d0dbd6af68c1ea60228fc95
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

project packages/apps/Dialer/
commit 32e9729a5e668c4f253c2d356a282c2f505b141c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:49 2015 +0200

    Automatic translation import
    
    Change-Id: I605f1d3554f5ab476190ad63d6fd64bc89a26fe3

commit b085e7a35eaa31737d11a3745068006001e94e6a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:49:56 2015 +0300

    Automatic translation import
    
    Change-Id: I6d183d3b7b0520cf7a13ebb27055e385393812cf

commit 35baf2c50e5875e50a2e7cfcf87584e79af87418
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:01 2015 +0300

    Automatic translation import
    
    Change-Id: I2ae1cf87986b086f70a2b4dcbb965f155041f9fb

commit 01421b9179f6795d72aea7da3b693d8d4857ccb3
Merge: 6988778 35baf2c
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:07:17 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 04ec9ba373dedc490480ac567079916753c8eff2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:05 2015 +0300

    Automatic translation import
    
    Change-Id: Ib35707ea97155e5e08ef2e178a88e39de89e798f

commit d4bd2749cb7210cf3b57bd68ecf5d3469347f960
Merge: 01421b9 04ec9ba
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 17 22:59:49 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 1cd8b6ba713f3ff3b3c74fbfa2e447fb9b9981ac
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Tue Apr 7 18:54:50 2015 +0200

    [2/3] Dialer: Smart Dialer
    
    Put on your ear, and this will automatically call current number in message or dialer
    
    Change-Id: I424175181c3c71ae83d9605ce017506340c83ab2
    Signed-off-by: linuxxxxx <joey@cyanogenmoditalia.it>

commit 2d6c9935474a2850d8c54b403c2cecdfa578f223
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:38:08 2015 -0700

    Revert: Dialer: Direct Call (3/4)
    
    PS2: Change location of Proximity sensor java file.
    
    Change-Id: I6709f2a00852cb1021fc46114ee9810c03d86876
    
    Conflicts:
    	src/com/android/dialer/dialpad/DialpadFragment.java (reverted from commit 6988778d7bdfd7b50a2cdf9170e109711d9b675c)

commit 901f648658e4836c21fc7660ba91211babae62fc
Merge: 2d6c993 1cd8b6b
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:38:26 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/Eleven/
commit 65716f05f719016ec4593fa4767c92a4606076ac
Author: Bryan Owens <djbryan3540@gmail.com>
Date:   Thu Apr 9 17:14:00 2015 -0500

    Expose colors from array in Eleven player
    
    Signed-off-by: Bryan Owens <djbryan3540@gmail.com>
    
    Change-Id: I0524ee3c1425ff94c33147cf7a9978fb69f3cc04

commit b2ebdc93b53db5a6805a2fdc99574ecc9bedfbe5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:49 2015 +0200

    Automatic translation import
    
    Change-Id: I706ba0b421b725967fca66376be10a6a4027e4f1

commit 296bf299500406876faa1ae14ef2025e84073f16
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:54 2015 +0200

    Automatic translation import
    
    Change-Id: I57fb2e9ca94f3cf041da11897c015662bd4fdfdf

commit a64a8224aa5ef9f122e827be45ed44684cd3ee31
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:06 2015 +0300

    Automatic translation import
    
    Change-Id: I3146069beab8e56c5583ac8c3068b8f2ba65daa3

commit 8f4dedadcc0ae75e12c8dd32cb7f73bdc941589a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:07 2015 +0300

    Automatic translation import
    
    Change-Id: Iafb5430b416befbb68309e16bf2cf7a4984c7347

commit e8e1310e734b467430ad51951ce1538f510a155a
Author: Mikalacki Sava <mikalackis@gmail.com>
Date:   Wed Mar 4 16:18:14 2015 +0100

    Eleven: Show/Hide album art on lockscreen
    
    Added preference option to show/hide album art on lockscreen.
    
    Change-Id: Iea2173288fc279f15abe6675a0ffd582e35ad321

commit 4307cc8356ae199d3e20ff01ec3e25966845a788
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Mar 19 01:48:19 2015 +0200

    Eleven: Checkboxes to switches
    
    Change-Id: I41439cc69147db49b08cace87ba3513d34dbac6c

commit 19e506ba59b25008e4e361aa65f471bfb8aef3b2
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sat Mar 28 22:30:46 2015 +0100

    eleven: remove_ACTION_PICK from manifest
    
    We are far from support pick an audio file. This cause MMS to be able to pick an
    audio file with Eleven, which is currently not possible.
    
    Change-Id: I65192d1dccd0b98982d65c7743c51cda3860f7d5
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 693b80582cdbec25d795bdba57d08129fc106990
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:12 2015 +0300

    Automatic translation import
    
    Change-Id: I5bf81d21196cfbf74d7e1451ad9000e89a97d79e

commit 914b9d7a85838bc979bb587da075c1e6869d4eb6
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Apr 14 17:08:54 2015 -0700

    Eleven: properly send open/close session events
    
    These were being fired off at device boot and there was a session being
    held for the entire duration. Only request the session when playing.
    
    Change-Id: I37ebc5a6898453dd090cc68ee2126e9c5d08d892
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit ef800adc3d03bc5e96f414438113560bb497cd68
Merge: 914b9d7 e8e1310
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Mon Apr 20 21:23:52 2015 +0000

    Merge "Eleven: Show/Hide album art on lockscreen" into cm-12.1

commit 3de284785e1edab3280919206cc0cead63bc2322
Merge: ef800ad 4307cc8
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Mon Apr 20 21:24:01 2015 +0000

    Merge "Eleven: Checkboxes to switches" into cm-12.1

commit 4e906d96832882b802ea237611c35d776f1a46ee
Merge: 3de2847 19e506b
Author: Abhisek Devkota <ciwrl@cyanogenmod.com>
Date:   Mon Apr 20 21:24:24 2015 +0000

    Merge "eleven: remove_ACTION_PICK from manifest" into cm-12.1

commit 0c5e34543c027ed4d2cfc23966b770d00babac1f
Author: Linus Lee <llee@cyngn.com>
Date:   Fri Apr 17 17:33:40 2015 -0700

    Eleven: minor string tweaks
    
    Change-Id: If61a9fceb262d96418134a986a24ec7d79730333
    (cherry picked from commit 405d0d09ad8b3ecb24f3633695c034da2cec404e)

project packages/apps/Email/
commit 2e8e179c999772f3180b110a7744a19f8b0449c2
Merge: b754aa9 877904c
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:47:00 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

commit 7b9554c45d27ed167a347520173431479a9fce38
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Mar 27 00:57:30 2015 +0200

    Update strings for crowdin
    
    Change-Id: Ib59198e1321db5b3c6889432c842d42dd040cea4

commit c0f648d932d8cb61413674463c1c345a1e515f85
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:15 2015 +0300

    Automatic translation import
    
    Change-Id: Ifd737704c6917543e69c08bcf3800ecc309a0f4e

commit 4493eeffb1071025c7f1c9ff3ed3559d38eb1b8d
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:12 2015 +0300

    Automatic translation import
    
    Change-Id: I13324c929f272c36bc31650a508cbc1f4c874d08

commit df55f2a43c7971aa2ba403ab9c46229546679bac
Merge: 2e8e179 4493eef
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:07:45 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit cb099d4b88f8272a90cf7d5e6018a8337d985978
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:18 2015 +0300

    Automatic translation import
    
    Change-Id: I8bf6ec74fa7132f71554e88d390cc89feb02df15

commit e155b4fa081ba4d3271b19d5c8247a01f19fb3aa
Merge: df55f2a cb099d4
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:31:00 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 8dcea5657c7834a40678ad973ddd2c5bf4f64757
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Apr 19 10:36:09 2015 +0200

    email: finish the settings activity after delete its account
    
    Change-Id: I540f1fe9dc874093ad0067cd56c9f0920620ece1
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 2b69c4736e2f3f8c36ec2bc667c8ffbe321209aa
Merge: e155b4f 8dcea56
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 20 20:41:53 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 7451d260d6d3ed5bd8b9f107d134ff965ace0cc0
Author: tobitege <tobiasteschner@googlemail.com>
Date:   Mon Apr 20 15:50:44 2015 +0200

    Fix NPE in getHierarchicalFolder
    
    Fixes exceptions like this:
    java.lang.NullPointerException: Attempt to read from field 'java.lang.String com.android.mail.providers.Folder.name' on a null object reference
    at com.android.email.activity.setup.MailboxSettings$MailboxSettingsFolderLoaderCallbacks.getHierarchicalFolder(MailboxSettings.java:377)
    
    Change-Id: I2c5dda84439caa5d894f5706c9c6a07079cda69c

commit 3080c4d17eca27b0355518a8a7ce437f785361e8
Merge: 2b69c47 7451d26
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:53:15 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/Exchange/
commit ea5130df470a4e65e4040453531ee674a42c591f
Merge: d2cd05e d08d855
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:47:35 2015 -0700

    Merge remote-tracking branch 'github/cm-12.1' into cm-12.1

commit 98f7ac87ba27c5119735e4f67addc4b46edad725
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Tue Apr 14 23:59:34 2015 +0200

    exchange: fix typo in switch case flow
    
    Change-Id: If2793cd4dbcb9152fdc13be47cbac098467f7a10
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit ff984196d8aee55077029093e7c3b507b7d75e1a
Merge: ea5130d 98f7ac8
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:08:12 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/Gallery2/
commit a79ff727e418e32e0ad65e13a0b3cbbb0cc351cf
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:47:54 2015 +0200

    Automatic translation import
    
    Change-Id: Ib1edaf2f04c5cec7840daa33701ca2dffb4d7226

commit 7cbe584cde4dd97424155d72c5e563107cdae41b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:00:59 2015 +0200

    Automatic translation import
    
    Change-Id: Ibd7d5773bd695c757cd77b35f0b8df1c119e8754

commit 2ee214594895a9694e961c98e635adfc496cf1c3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:24 2015 +0300

    Automatic translation import
    
    Change-Id: Iaa89ae9514149bc83e12c34fc8e200532adbccca

commit f7e04f5d1f28780c03f4d6bdaf88096c196e19eb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:17 2015 +0300

    Automatic translation import
    
    Change-Id: Ifa6c8d665d25ddee7d4cad1f8019833f3edcbdf3

commit f2c3fe02acd9d9fccafe2c18b66b71b6856e19d0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:23 2015 +0300

    Automatic translation import
    
    Change-Id: Ia8a3817d7d07c085c800b276c1411855b69bf758

commit 158791beb63b3be747c4eda2deb961867a7c55f2
Author: maxwen <max.weninger@gmail.com>
Date:   Sun Jan 4 18:16:42 2015 +0100

    Gallery2: readd storage selection support (2/2)
    
    Change-Id: I82cece40813aed511d9effbcbf36e559de7962ad
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/91148/

project packages/apps/InCallUI/
commit 6b6c9119a3e4020c50ea43c22020c7eb4d3ba319
Merge: 7930fe3 e01b345
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:48:35 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit a42ce0603f4bdb272289ec8b9e5ea09cf910e7bc
Author: Danny Baumann <dannybaumann@web.de>
Date:   Sat Apr 4 21:40:23 2015 +0200

    Clean up call button handling.
    
    Now that AOSP has added an overflow button, there's no need for us to
    add a second one, so merge the two into one.
    
    Change-Id: I2865a8dc37ba44b9bb4ce647508982a035d77291

commit b772e5c675dcdcc45a41941436319b75bba9cd12
Author: Danny Baumann <dannybaumann@web.de>
Date:   Sun Apr 12 13:39:21 2015 +0200

    Clean up volume boost button logic.
    
    Change-Id: Id96b5085bf4fe810fa2d05326ff01a91450f0e09

commit 0625f13b3426a9cfea49eaed4ae47133fcd5e2ba
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:04 2015 +0200

    Automatic translation import
    
    Change-Id: I83557061426f246ae9dbd532a6509841843ff022

commit cebba3d4e3bb31671394ca3d28ec3624b881628d
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:31 2015 +0300

    Automatic translation import
    
    Change-Id: Ie8bc55494250d5ccae3efa590d2f37eefce0c92d

commit 2443a99a63bab3ec832fd7e09c366b30c7db0edf
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:22 2015 +0300

    Automatic translation import
    
    Change-Id: I96f4221430a666e5a8c0c5f9d281582a57ca76d0

commit 67da828ade100c415aae09077f235161f70ec048
Merge: 6b6c911 2443a99
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:08:42 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit bf5bae2dfa0e155fd18b9d716ddfaf4c38c5da62
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:30 2015 +0300

    Automatic translation import
    
    Change-Id: If52ffbda0f25d7d629e56869cf7fa8dd1afdbbd6

commit be0d27632b2e0a548b0a4446967bb836ad4d0afc
Merge: 67da828 bf5bae2
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:32:20 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/KernelAdiutor/
commit 29bb8745016bdcf10c7600763a2a34549e761b5b
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Wed Apr 15 20:00:47 2015 +0200

    AndroidStudio: Own configuration
    
    Change-Id: Icd1b327c04f198133c0fb8c4f7a9094a659af986

commit 9a185a49acc378c42b68450cde806243d6223f43
Author: Willi Ye <williye97@gmail.com>
Date:   Thu Apr 9 21:24:30 2015 +0200

    Add Yorici Calibrated Alpha

commit 71d15b21ad8e5d0496e625dc3c7db6dbb6ed8401
Author: Willi Ye <williye97@gmail.com>
Date:   Sat Apr 11 16:32:11 2015 +0200

    Decrease card's height

commit b913c3a4e591b96ddff03f84aaa51f8a54919cfc
Author: Willi Ye <williye97@gmail.com>
Date:   Sat Apr 11 17:07:01 2015 +0200

    Add HBM control

commit 02138b6db8f19d731fdb2e551a5b6649267fc28c
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 12 18:59:55 2015 +0200

    Add gammacontrol additional profiles

commit 2899e320ecad90caa12843f69b069a8435c04274
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 14 14:27:58 2015 +0200

    Import translations from crowdin

commit 6f0562bc1b19306460a3c82b1989d64ace3acf37
Author: Willi Ye <williye97@gmail.com>
Date:   Sat Apr 11 15:24:59 2015 +0200

    Replace PathReaderActivity with ViewPager
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/PathReaderActivity.java
    	app/src/main/java/com/grarak/kerneladiutor/fragments/RecyclerViewFragment.java
    	app/src/main/java/com/grarak/kerneladiutor/fragments/kernel/CPUFragment.java
    	app/src/main/java/com/grarak/kerneladiutor/fragments/kernel/IOFragment.java
    
    Change-Id: I335591df3b2d2f4f7425dbd7be4368d0c7e240b6

commit fe5b83f8b3304091a64fd1a7bac7a974a2755cd3
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 14 14:22:08 2015 +0200

    Add unfinished recovery controls
    Remove selinux options
    Add PCC support
    Some icon changes
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/fragments/RecyclerViewFragment.java
    	app/src/main/java/com/grarak/kerneladiutor/fragments/ViewPagerFragment.java
    
    Change-Id: I52ff6eb1f14decdd38595aaf04b42693e3f005e1

commit a2264ae5e3da2cbc55c80854f57504bee9a45393
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Wed Apr 15 21:37:51 2015 +0200

    Add back SELinux option
    
    Change-Id: Ib0f2719044291670db377b7bdebc4d3c10bb8d49

commit 3df52abc7e03b4df3af9a80453464238c6a75779
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 14 21:11:48 2015 +0200

    Finish recovery
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/fragments/tools/RecoveryFragment.java
    
    Change-Id: Ib8ff339b5a4136678e9cb196165211466cd05d1c

commit b877611f3f0d9902cb7e577e60b4f4df5a7b8be0
Author: Willi Ye <williye97@gmail.com>
Date:   Tue Apr 14 14:29:42 2015 +0200

    version 0.8.9.5.2

commit d3a7c6c015a4cca33699c4aba44cd1a312159096
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Wed Apr 15 21:43:45 2015 +0200

    Bump version to 0.8.9.5.2
    
    Change-Id: I85c4b166ead2e7f284a43c3b2b12d4f59dfd662b

commit 7b7c46e0044438a11ebd0046e1322604997d4c4c
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Wed Apr 15 23:20:19 2015 +0200

    libs: Use prebuilt android support API 22
    
    The android support from ROM gives some issues, use prebuilt instead
    
    Change-Id: I858ba1b335952cefb46c352b040adf3a6dc37a38

commit cdf5f6ec1d3e8465317bde31b5ccb59167b244cd
Author: Zhao Wei Liew <zhaoweiliew@gmail.com>
Date:   Wed Apr 15 21:25:18 2015 +0800

    Add power saving workqueues toggle

commit 586e13a70bd66675b160e1b115a500b1e7d8d90b
Author: Zhao Wei Liew <zhaoweiliew@gmail.com>
Date:   Wed Apr 15 21:36:08 2015 +0800

    Add exponential backlight toggle

commit b73e8ff5e354bc590e72d9be47e4920e7d794f65
Author: Willi Ye <williye97@gmail.com>
Date:   Wed Apr 15 21:47:38 2015 +0200

    Replace SQL with JSON
    SQL is evil, fuck it

commit 19902591f4ade969f1cb69b266d814e3669486b2
Author: Willi Ye <williye97@gmail.com>
Date:   Wed Apr 15 22:01:05 2015 +0200

    Add new features to arrays (for apply on boot)

commit 6d9737f5b79bc6fd933341ded879219d19267223
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 16 19:06:16 2015 +0200

    Fix compile error
    
    Change-Id: I3bf438248111cccc0cd265bf557f85d11a9e4d70

commit 7f6d63c7fbc20b84ad6e4c90463f7cc27f8795de
Author: Willi Ye <williye97@gmail.com>
Date:   Wed Apr 15 22:04:13 2015 +0200

    version 0.9 beta

commit f2e182bc39166e7340f40767a7b6ac6fa0b0d54e
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Thu Apr 16 21:11:43 2015 +0200

    Bump version to 0.9
    
    Change-Id: I2e822503adf3a386597a5ec174c4b8d9b8a6d347

commit 7e92313bf443d24a27252d6fedd49caa21ff8a00
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 12:57:48 2015 +0200

    FC fixes
    I don't know how people still manage to FC the app
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/fragments/PathReaderFragment.java
    
    Change-Id: I5d111f87d835b4cf3ae4e97d59f1128af18acccc

commit fede965d0a4c607754d247d945264de97c1ef740
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 15:19:46 2015 +0200

    Use LinkedHashMap instead of Map
    keep things in order

commit 310fd09bdc5c7af66fa6dee48db9b6bbfe68cb09
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 19:14:39 2015 +0200

    Add all LCD Backlight settings
    some clean up
    
    Conflicts:
    	app/src/main/res/values/strings.xml
    
    Change-Id: I14d27e95fa19de6042a6a65e1b390299984c73ec

commit f7fe61d134516bcabd3fd10837db70ac466f3a5e
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 20:45:03 2015 +0200

    Add CPU temp

commit b3aba18d8564fdf3ad73e6ce35aed24e70ff6c70
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 21:54:15 2015 +0200

    Add hostname editor
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/fragments/kernel/MiscFragment.java
    	app/src/main/java/com/grarak/kerneladiutor/utils/Constants.java
    	app/src/main/java/com/grarak/kerneladiutor/utils/root/Control.java
    
    Change-Id: I604d15ff60a67179f1e2d8c6399a4fd425c150d0

commit a310011c274e611635a581c55fe512115793270a
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 22:02:05 2015 +0200

    Add Fsync control
    
    Conflicts:
    	app/src/main/java/com/grarak/kerneladiutor/fragments/kernel/MiscFragment.java
    	app/src/main/java/com/grarak/kerneladiutor/utils/Constants.java
    	app/src/main/java/com/grarak/kerneladiutor/utils/kernel/Misc.java
    	app/src/main/res/values/strings.xml
    
    Change-Id: I07a4fe287a5df62aa256e20f6c7f833d71797372

commit 507b09bc3c872091f3ae57a9a168986998c94965
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 23:09:00 2015 +0200

    Add franco sound control

commit defad7c28c1edadd5a232901e3b18383d36f4178
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Mon Apr 20 21:58:30 2015 +0200

    Add missing selinux_items
    
    Change-Id: Icd911c1e5d658d1a652bf110bebb341d1cb9b318

commit 409b03cc603b1fed87e89e1aaf173f4edf3b536e
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 23:10:09 2015 +0200

    version 0.9.1 beta

commit 39e850c3d6beebdd77d4f92ca5817fef359a1456
Author: Willi Ye <williye97@gmail.com>
Date:   Sun Apr 19 23:15:37 2015 +0200

    Import translation from crowdin

commit 1d5c0ace5e046d973619a406e49eaa4a898be535
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Mon Apr 20 22:03:20 2015 +0200

    Bump version to 0.9.1
    
    Change-Id: I9d5ab80587f69f53a352f2649fba34448ca82f9c

project packages/apps/LockClock/
commit 83c8b07355deb19acaf986bcb312197307939721
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:05 2015 +0200

    Automatic translation import
    
    Change-Id: I1c97c5a6355c325f24b67cc9bdd9e9b3d588d8ab

commit c9e70426972c019b19334d7d16251dd0d22b1d97
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:09 2015 +0200

    Automatic translation import
    
    Change-Id: I3a2f9d1e57f5b0b6f3fb3975021389c44b4b638b

commit 35defa1792ad23cdcfad100af44af3cb79292081
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:40 2015 +0300

    Automatic translation import
    
    Change-Id: I6293d07ab2144e1169e14dcdf4f2ef2bcf2d0940

commit d3fa458cdac1d5ec7261c3da01c39679eaf19790
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:28 2015 +0300

    Automatic translation import
    
    Change-Id: I781656460f62639d1d8b533e664955f624d1f5ad

commit 69c9e6539729ab0adccc503b4ffafef9918c1c7a
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:35 2015 +0300

    Automatic translation import
    
    Change-Id: Iffbf9426d2bf080e5fa4ce7a0a003786afc116f0

project packages/apps/Mms/
commit 7322cf586bb0d5afd00e8c26b5fa4cfe4aaa7d4d
Merge: 15a07cc 4b33fba
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:49:45 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 28ecc19200ce2fa39383b0e9d07be735d752d53a
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 14 08:36:54 2015 +0200

    Improve subject editor layout.
    
    Properly center the cancel button, make its sizing consistent to the
    'add contact' button above it and fix its ripple.
    
    Change-Id: I1107cc80a66e6d6f36a89e434d5cca7373451bef

commit bc91cdeb2e16b2e09b953843bb579bddf88255fd
Author: Danny Baumann <dannybaumann@web.de>
Date:   Tue Apr 14 08:35:06 2015 +0200

    Properly populate subscription ID column when sending MMS.
    
    Populate the DB column, and feed the correct value into it for the !MSIM
    case. Also clean up the code a little to make the subscription ID value
    flow a little more readable.
    
    Change-Id: I1bf791d4c0e70c73db8d5bc1a11a1338930caf7d

commit 06ee0c50c9a22b0736925b06e21756dd8aaaaadc
Author: Danny Baumann <dannybaumann@web.de>
Date:   Wed Apr 15 08:21:49 2015 +0200

    Kill off some debug spam.
    
    Change-Id: Id7855254d9927fbf9212345639217e0d5309ff40

commit a18b4ceb81f81973045c56bb6ee26b92c6d6cc4d
Author: Danny Baumann <dannybaumann@web.de>
Date:   Wed Apr 15 08:41:27 2015 +0200

    Minor logic cleanup.
    
    Change-Id: Ic79beabdd8836fcb6b05d9c369960a86d97beefb

commit 657697ce2a42e5633aeb86fca49b3f30d3c684a0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:50:46 2015 +0300

    Automatic translation import
    
    Change-Id: I21f4284af735d645ebbb1c4e2b2cd58ad03c07e6

commit 0a5ec850509450318607c5e9f758fecf66c88c71
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:33 2015 +0300

    Automatic translation import
    
    Change-Id: Idfa37d0c2bb821fb6536ac2a5df17c95feb776c1

commit cb29b731fbdde73eda9bfdb7826c52ee76524276
Merge: 7322cf5 0a5ec85
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:09:27 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit de1bfe580c6cebf451d3a5c3b8fca11ba73e1aff
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:40 2015 +0300

    Automatic translation import
    
    Change-Id: I3fdd461c934004d5ed7dfa12635f96ecb49ace7a

commit 3affa0fc86ed3578fed71df5866fbf863702a6b2
Merge: cb29b73 de1bfe5
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:33:29 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit cca4f658a99537bf9d3826079dbea83cc0a6d225
Author: Yanuar Harry <ai.the.smarties.physics@gmail.com>
Date:   Fri Mar 14 20:32:31 2014 +0700

    [1/3] Mms: Smart Dialer
    
    Put on your ear, and this will automatically call current number in message or dialer
    
    Change-Id: Id05b8cb6b869c7a31c55cd60eb03963994d16131
    Signed-off-by: linuxxxxx <joey@cyanogenmoditalia.it>

commit 08aa08e6d4e9e0e70ebd181208ce845672a064a5
Author: Bryan Owens <djbryan3540@gmail.com>
Date:   Tue Mar 31 17:31:12 2015 -0500

    Expose hard coded background colors from layouts for search activity.
    
    Signed-off-by: Bryan Owens <djbryan3540@gmail.com>
    
    Change-Id: I2246e017e93c14069244dfb10bdab8c66893d805

commit ccc96c439adf588bf7681f52e7228a735c5cd5bc
Author: Craig Schmitt <craigschmitt@cmshome.net>
Date:   Mon Jul 7 18:26:29 2014 -0500

    MMS: Add feature to auto-enable mobile data for MMS send or receive.
    
      Feature is default overlayable via "enable_data_for_mms".
    
    Signed-off-by: Adnan <adnan@cyngn.com>
    Change-Id: I1b79d42fb7ef16de4aedf5557ae6f3f82dd3a7c3

commit 2cb8dc593cdba731daaacd3b20fa75d78e096797
Author: Danesh M <daneshm90@gmail.com>
Date:   Thu Mar 26 19:44:03 2015 -0700

    Mms : Dismiss compose activity, if deleting last message and no text
    
    Change-Id: Iedfbddec88e30cb3aa4f76a8c59c44c24603671c

commit 243ffee5a5efd211073b587923251889ad563a40
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Wed Mar 25 01:23:07 2015 -0700

    Mms - remove Subject listener first when remove the subject
    
    epro:
    - Go to messaging-> add subject ->add an attachment
    - Delete subject and then delete the attachment
    
    Result:
      Still show Mms,Can not converting to text message
    
    Change-Id: I410f018385807862a80be48d4dfeb6cb513f5a1b

commit 06be6ecb57442f4a44acc642b0295b8579a4614e
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Mon Mar 30 06:03:55 2015 -0700

    Mms-add Calendar event type of loading Calendar draft
    
    Repro:
    - Go to messaging-> add subject ->add an Calendar
    - back save as a draft->then type it->the Calendar cant see
    
    Change-Id: I1a54e5712a9ab4e16b9d3b793cff617e5d60218e

commit aeff12260def66916d9b39a1fab91ce87eebb5c6
Author: Danesh M <daneshm90@gmail.com>
Date:   Mon Mar 30 21:35:12 2015 -0700

    Mms : Only exit after deleting last message
    
    Fixes bug where compose message (from action_view) and
    opening drafts auto-close
    
    Change-Id: I17c7a1f6062597f383fda5104de416de43d59639

commit e78462080d96436d36448e6fd09207489d46bc1a
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Mon Mar 23 16:13:00 2015 +0100

    Backup: close cursor
    
      * when exporting the sms backup a cursor did not get closed and the system
        complains about it (Cursor finalized without prior close())
    
    Change-Id: Icfb2def9aaef11f12511a2f127965d1bfc6a75dc
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    (cherry picked from commit aab4511c3c140de1d6558637cadf04112b59c93a)

commit 210d155b938f3c6017773dd6d0c12720b1d6a1ba
Author: Joe Zhong <joe.zpf@gmail.com>
Date:   Thu Apr 2 11:24:15 2015 +0800

    Mms: Recipients field is cleared when returning from SelectRecipients
    
    Repro:
     - Create a new conversation
     - Select some contacts
     - Pick contacts with "add contact" button
     - Swith to "Pick contacts" screen
     - Click home action bar in the top left corner.
     - Observe: in Compose screen, the previous information is gone
    
    Change-Id: I9c4765efecca86df7d2f233b6dc75b5a61d596c9

commit 3e576f2f270b93fcce97dbb533d7ee7022ffd818
Author: Bryan Owens <djbryan3540@gmail.com>
Date:   Tue Mar 31 17:31:12 2015 -0500

    Expose hard coded background colors from layouts for search activity.
    
    Signed-off-by: Bryan Owens <djbryan3540@gmail.com>
    
    Change-Id: I2246e017e93c14069244dfb10bdab8c66893d805

commit 2dfa423e8136e737ceaf5b71e1fea32df8a54b27
Author: Craig Schmitt <craigschmitt@cmshome.net>
Date:   Mon Jul 7 18:26:29 2014 -0500

    MMS: Add feature to auto-enable mobile data for MMS send or receive.
    
      Feature is default overlayable via "enable_data_for_mms".
    
    Signed-off-by: Adnan <adnan@cyngn.com>
    Change-Id: I1b79d42fb7ef16de4aedf5557ae6f3f82dd3a7c3

commit ee0724a8e2ab3a022a4a16b06dd1a64a29d9e581
Author: Danesh M <daneshm90@gmail.com>
Date:   Thu Mar 26 19:44:03 2015 -0700

    Mms : Dismiss compose activity, if deleting last message and no text
    
    Change-Id: Iedfbddec88e30cb3aa4f76a8c59c44c24603671c

commit fb630992b7cfce027b7b0f88f529bbb8a5dba35d
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Wed Mar 25 01:23:07 2015 -0700

    Mms - remove Subject listener first when remove the subject
    
    epro:
    - Go to messaging-> add subject ->add an attachment
    - Delete subject and then delete the attachment
    
    Result:
      Still show Mms,Can not converting to text message
    
    Change-Id: I410f018385807862a80be48d4dfeb6cb513f5a1b

commit 2515453be2af7284e43f056205193e9f9b4bddca
Author: xiao.hu <huxiao0816@gmail.com>
Date:   Mon Mar 30 06:03:55 2015 -0700

    Mms-add Calendar event type of loading Calendar draft
    
    Repro:
    - Go to messaging-> add subject ->add an Calendar
    - back save as a draft->then type it->the Calendar cant see
    
    Change-Id: I1a54e5712a9ab4e16b9d3b793cff617e5d60218e

commit bf1ec627ec5e75eee11bdbce4714ea1b415dbfc5
Author: Danesh M <daneshm90@gmail.com>
Date:   Mon Mar 30 21:35:12 2015 -0700

    Mms : Only exit after deleting last message
    
    Fixes bug where compose message (from action_view) and
    opening drafts auto-close
    
    Change-Id: I17c7a1f6062597f383fda5104de416de43d59639

commit 2af5da67e081f4062e872ed88647561f7f87ce2c
Author: Alexander Martinz <eviscerationls@gmail.com>
Date:   Mon Mar 23 16:13:00 2015 +0100

    Backup: close cursor
    
      * when exporting the sms backup a cursor did not get closed and the system
        complains about it (Cursor finalized without prior close())
    
    Change-Id: Icfb2def9aaef11f12511a2f127965d1bfc6a75dc
    Signed-off-by: Alexander Martinz <eviscerationls@gmail.com>
    (cherry picked from commit aab4511c3c140de1d6558637cadf04112b59c93a)

commit eb1afb55c1b1e230d551fa1d2877eee521282d59
Author: Joe Zhong <joe.zpf@gmail.com>
Date:   Thu Apr 2 11:24:15 2015 +0800

    Mms: Recipients field is cleared when returning from SelectRecipients
    
    Repro:
     - Create a new conversation
     - Select some contacts
     - Pick contacts with "add contact" button
     - Swith to "Pick contacts" screen
     - Click home action bar in the top left corner.
     - Observe: in Compose screen, the previous information is gone
    
    Change-Id: I9c4765efecca86df7d2f233b6dc75b5a61d596c9

commit 0053cc1d2e8e451370ad4ace31968bf92b171dfe
Author: kaiyiz <kaiyiz@codeaurora.org>
Date:   Mon Nov 3 13:44:00 2014 +0800

    Mms: The Slideshow time display incomplete on Edit Slideshow
    
    text_preview_bottom is too long and push a part of duration_text
    out of screen. And the "android:ellipsize="marquee"" is not working
    because text_preview_bottom can't get focus.
    
    Use RelativeLayout to Make sure the duration text be displayed
    completely and use android:ellipsize="end" instead of 'marquee'.
    
    Change-Id: I58ee87dc4fa6edd0502dd91bd5814196583344d2
    CRs-Fixed: 745995
    (cherry picked from commit 8b253cc3b6efe99734ca16b5ed8975d97b6c1ff1)

commit a5a3bf6e1365d8f88cc2f1ef160bcd9e94729ec1
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Wed Apr 15 11:19:04 2015 -0700

    Mms: add vcalendar as a saveable content type
    
    Repro:
     - Send/receive a Calendar MMS
     - Long press on the MMS message
     - From the overflow menu select "Save attachment"
     - Observe toast: "Couldn't save attachment"
    
    Change-Id: I098a9e1e1ad539771908920773a1ef29b3637955
    (cherry picked from commit fbb4a40047ea2e25d60ead64910b879548ab0d1c)

commit d9cf56a6c0a9e899955abd2d544200aa8ac63a8b
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:40:07 2015 -0700

    Revert: Mms: Direct Call (4/4)
    
    Change-Id: I2d3807150c12349bdcf2eda10904faf28f42169e (reverted from commit 9cdc5d5b704800aa9d35fc33f2e21df355accb77)

commit 4c25c328254ef63c5971a0fc28f4963188c67e9a
Merge: d9cf56a a5a3bf6
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:40:26 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/PhoneCommon/
commit 40bdf1cfe3fe127fe8d0089e2d05511a8ae9eefd
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:18 2015 +0200

    Automatic translation import
    
    Change-Id: I3f164e5d4df8d3c92debf2878132f5f42649f2fd

commit 1d4b66fb169d66d146651a3f7c830f34013478c1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:19 2015 +0200

    Automatic translation import
    
    Change-Id: I1d4eed32385a970b13788fbb8303f83bb4a99e67

commit d69a3c295f3f3c72f5433c7193098d14d86053da
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:48 2015 +0300

    Automatic translation import
    
    Change-Id: Id97f7de2d10eae9c7d962e6406ee1e39e6f18030

commit 1c225a1866f773bff3e42c41cfd0cf0baa4502e2
Author: Linus Lee <llee@cyngn.com>
Date:   Mon Mar 16 18:18:22 2015 -0700

    PhoneCommon: Adjust dimens for hdpi
    
    The spacing for the dial pad is too small, so
    create some more space by decreasing the whitespace
    between the dial pad at the top bar
    
    Change-Id: I2775ce417b53f7a69abeb3b8919169024a7714dd

project packages/apps/Settings/
commit 63699184af00a9cc084da193f2a544a6e916ae23
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Wed Apr 15 21:23:52 2015 -0700

    Settings: Add music tile (2/2)
    
    Change-Id: Ie36994028ce5c827e31cbc9d17161be5eee2894f
    
    Conflicts:
    	src/com/android/settings/cyanogenmod/qs/QSTileHolder.java

commit 14128ae66fa6cc5710376920d27cab23a1459989
Author: Roman Birg <roman@cyngn.com>
Date:   Tue Apr 14 10:33:31 2015 -0700

    Settings: fix volume link notification preference
    
    Change-Id: I8ad241c73158a5230ab79a003392222809aa3904
    Signed-off-by: Roman Birg <roman@cyngn.com>
    (cherry picked from commit dcadedc034cbb908cbc88f1f95305b1413c7b8aa)

commit b27e1252daaf2bee1143db3394a97b0d5afd7e58
Author: heydabop <heydabop@gmail.com>
Date:   Fri Mar 27 01:18:01 2015 -0500

    Remove duplicate strings
    
    Change-Id: I708c8093cbaf9df734bc9d9d0cff2fa920882af0

commit 9cc4e0c5466b3a4c941703320b331a7350da0430
Author: cretin45 <cretin45@gmail.com>
Date:   Wed Apr 8 16:30:12 2015 -0700

    Settings: Restore proper ringtone for msim
    
    Change-Id: I4dc5a44e7c820cfbba8dcb10afe624e828f2eab2

commit d8177e039d1f33619502e328a4a16acb4e00b59f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Feb 3 08:46:11 2015 +0200

    Settings: Remove more unused resources
    
    Change-Id: Iab89d1cc9ee3dfc07bbeebd34fa309004ef52a5a

commit 64de007b94f2eeb3db90f791d919d470a4d3389e
Author: Tamás Tóth <syman@babulus.hu>
Date:   Mon Mar 23 10:16:21 2015 +0100

    Settings: Set untraslatable
    
    Change-Id: If13991f0daf9a02cd3e3c25ff512a956ed9720c7

commit d158d3105cd41dfbebeaff4e086e1779add23bca
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Thu Dec 12 05:40:54 2013 +0200

    Settings: forward port lock pattern grid size (2/2)
    
    Change-Id: I7078d703c218cd096d9b77c003a94b52fbce6322

commit 439c08381a402c9ea917aeccaa4c578d58f533dd
Author: Roman Birg <roman@cyngn.com>
Date:   Mon Apr 6 12:20:33 2015 -0700

    Settings: handle decrypting larger pattern sizes
    
    Change-Id: Id24d46829063171fa87cabb23a7da378726d7548
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit c1fe183665f8e5df41b78c127eeb6aa2907a657c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sat Apr 4 04:43:43 2015 +0300

    Forward port pattern visibility settings (2/2)
    
    Change-Id: Ic627953c5df854c442671a98b5da539b994da18b

commit b023fc66bd55c41ea0617f86e0b88f8c464cce9f
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Wed Apr 15 21:30:34 2015 -0700

    Create general lockscreen settings category
    
    * Owner info, lockscreen shortcuts & visualizer aren't security settings
    
    Change-Id: Ia1c435abb94cc9a23b2f683e96572f21569a7d05
    
    Conflicts:
    	res/xml/security_settings_chooser.xml
    	res/xml/security_settings_password.xml
    	res/xml/security_settings_pattern.xml
    	res/xml/security_settings_pin.xml
    
    Conflicts:
    	res/xml/security_settings_pattern.xml

commit d51617db110df3bb21d236eb70c00b57bf5eda51
Author: AragaoAnderson <andersonaragao@me.com>
Date:   Thu Apr 16 09:23:28 2015 -0300

    Settings: Fix Sound & notification FC on Settings shortcut widget
    
    Correct SoundSettings fragment is com.android.settings.SoundSettings
    instead of com.android.settings.sounds.SoundSettings
    and com.android.settings.sound.SoundSettings
    
    Change-Id: Ie770eb1577b88e57e12a0d2899f13cda5c551e22

commit fb834ba85aeb5d68667f19a124051981dc31562f
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 30 17:56:01 2015 -0700

    Profiles: play Ringtone when setting volume overrides
    
    Change-Id: Ibd171f9fcbf96aa0dae9a1dafb6fb07105b2f4c8

commit f660b195f623409457ab3d62577468615900f473
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:23 2015 +0200

    Automatic translation import
    
    Change-Id: Ie9f171ed938af04d9012582a39a99ea9cc393ca7

commit 8c5386c1a2e1faa1375c3f6a97e04d52e02af717
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:24 2015 +0200

    Automatic translation import
    
    Change-Id: I3df9393551ebf117cc6461f799e778ad3d660116

commit eef0e158bd94b04e7d1f36764c5d9964946c7c4c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:51:02 2015 +0300

    Automatic translation import
    
    Change-Id: Ic3cafebaebe350005c1662d95d4a82dbc5d73a99

commit de98ba6c8e4a2de9d426698b2b8f4d1730f5cba8
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:50:45 2015 +0300

    Automatic translation import
    
    Change-Id: I9a86d2c513c6b317f8cf138c578547e4df47212d

commit eea177de060e9e41249b525c692824e4449aca7d
Author: Matt Garnes <matt@cyngn.com>
Date:   Wed Mar 25 16:25:26 2015 -0700

    Fix incorrect ManageApplications options menu order value.
    
    Change-Id: I5c9b7d1ce9e03fa0efe593efd76b4ad2899a126a
    
    Patchset: 1
    http://review.cyanogenmod.org/#/c/94735/

commit 67d10862fea78537885570be13ba559fbf4e60a7
Author: Dave Kover <dkover@cyngn.com>
Date:   Sat Mar 14 17:18:32 2015 -0700

    Themes: Allow switchbar text color to be themeable
    
    Better exposing the color of the switch bar text so that a theme
    can handle this assignment separately without having to touch
    framework theme colors.
    
    Change-Id: I81e3430e188f1ee0a22e92aea50878980f9cc61f
    (cherry picked from commit e36cc807b50176839a499831a98ee24e23e1c1a8)

commit 8dbd7a03f29ac80e0d5461277ec3769afa3e8028
Author: Dave Kover <dkover@cyngn.com>
Date:   Thu Apr 16 18:47:24 2015 -0700

    Break out the add icon to be separately themeable.
    
    If Settings is using the accent color for app bar, the add icon
    is also colored with this value typically and will cause readability
    issues. Adding a new drawable name that can be referenced to allow
    separate theming.
    
    Change-Id: I20512091e7a36c510399cbc5caa73aa8817fe393
    (cherry picked from commit 62c457ae955fc3b76041ae7c418cc1507ce46e8c)

commit 14c790ad526f934798252e7ccea6c5c145b5c406
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:19:52 2015 +0300

    Automatic translation import
    
    Change-Id: Id17d47bd3fb8d4931010f4a2557399d27ff69ab3

commit eff908386694a8f71fe837acfc68e46fbce77d84
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 19 19:51:54 2015 -0700

    Revert: Display SaberMod gcc info in About Phone
    
    Change-Id: I026cb7e140d460a8edabfd83f6757d6437a2ce00 (reverted from commit a4c353eb45f0fe76b5c10c7a1d4d634981a58ff5)

commit 148206882339b25b930857d68dbecf755909b96e
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Sun Apr 19 19:56:23 2015 -0700

    gcc and gcc flags info (2/2)
    
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    Signed-off-by: Chet Kener <Cl3Kener@gmail.com>
    
    Conflicts:
    	src/com/android/settings/DeviceInfoSettings.java
    
    Change-Id: I258d6ed5e82d622249aa4a731b3a0ea7f6dcb72a

commit 100bf687428e08054ce01dfe08e212ad802d3c2b
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 20 20:28:01 2015 -0700

    Revert "Sound settings: fix unlinking volume sliders (1/2)"
    
    This reverts commit 974520271370dd6a6b2fb6025bdb246860215108.
    
    Change-Id: I2ace5ad40ddc29678dfad072d23a943f85870afc

commit 384d92b226ff2549371fd9291ddbe770240b5ec5
Author: Brian Larsen <brian@chezbel.com>
Date:   Fri Dec 19 15:18:47 2014 +0800

    Add a 45 second timeout option for Screen, Dream and Lock timeouts.
    
    The following languages don't use Arabic numerals, e.g. "45", so the
    text for the "45 seconds" entries are just copies of the text that
    already existed for "30 seconds". It's easy to fix these... if you
    know those languages
     - values-bn-rBD
     - values-fa
     - values-km-rKH
     - values-my-rMM
     - values-ne-rNP
    
    This language is missing a lot of items and doesn't even have the
    normal timeout entries
     - values-ky-rKG
    
    Change-Id: Id4252eb38f5137ab493da4263c66b82c8c01924d

commit df2e843e4c9c7464fd92d15757a7b1a9871ea913
Author: tobitege <tobiasteschner@googlemail.com>
Date:   Thu Apr 16 13:25:24 2015 +0200

    Fix screen timeout exception in Display Settings
    
    Exception was: java.lang.ArrayIndexOutOfBoundsException: length=7; index=7
    This happens when non-English languages files do not have
    all values, i.e. a commit e.g. adds a screen timeout value
    but does not add it to all language files.
    
    Change-Id: Ic7b1abf8b7cac3997412afd2b27bd1c70db34877

commit 316d41b7e309648bf1170b451b028b77119ac878
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Wed Apr 15 00:32:41 2015 +0200

    settings: fix RTL layouts
    
    Change-Id: Id2db07908a37401ac17c2f206807813b3a0b1874
    JIRA: NIGHTLIES-1023
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 3591dff388e71402774c0ad3bf98fef881ebf206
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 16 17:45:42 2015 -0700

    Settings: fix search key not opening search
    
    Change-Id: Ied84a73ab2c1c32a0187276593f34915b0daa86c
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 920c56ff422548ab9c9a3e638ae76e65364a1274
Author: Roman Birg <roman@cyngn.com>
Date:   Thu Apr 16 18:24:32 2015 -0700

    Settings: re-index search after setting new lockscreen
    
    Some keys are removed/added dynamically. They need to be updated when
    the lock type changes.
    
    Change-Id: I365633ae5333bc6164f993f122d56409ea31df10
    Signed-off-by: Roman Birg <roman@cyngn.com>

commit 2b7d3091bab8610dc4bc0483e004cb08bf4bfc90
Author: Alex Cruz <mazdarider23@gmail.com>
Date:   Tue Apr 21 02:06:40 2015 -0700

    Battery Bar [2/2]
    
    Could not find syaoran12's email so i stuck Mazda because i got it from du
    
    Change-Id: I94a27fd31da07af6aca952796ca329bc8da6dca4
    
    Conflicts:
    	res/values/liquid_arrays.xml
    	res/values/liquid_strings.xml
    	res/xml/liquid_statusbar_settings.xml
    
    Conflicts:
    	res/values/cmr_strings.xml

commit 67a0de7973ae81fb136de66e332b0bdf1feedd8e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 02:42:41 2015 -0700

    [1/2] Kernel Auditor Tweaker
    
    Change-Id: I571b7f25b20f8edac31434317e6b76ebb3e6d6df

commit 5a5ef29148f4aa257cdbf55e34f8224d6d98e7cb
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 07:57:40 2015 -0700

    Revert : settings: Add PerformanceControl [1/2]
    
    Change-Id: I06b0815208041dd00f34ce01ca6b468cf54d26dd
    (cherry picked from commit ab15edf99742bad8ddd2384534941fcaf6088b60)
    
    Conflicts:
    	res/values/pac_strings.xml
    
    Conflicts:
    	Android.mk (reverted from commit 4b04fdb8aaab30952b04abf55578db80eae75569)

commit ffb916413481802e649f043547bedfac4ab166c5
Author: Alexander Westphal <westphal.alex94@gmail.com>
Date:   Wed Jan 28 03:01:04 2015 +0000

    Settings: update profiles drawable
    
    Change-Id: I61601b94231ab8668feebaf833968647a0beeba1

commit 1e77e2f64874b14b8507bd2b8718e2ae57cebf1a
Author: Janson Kang <temasek71@gmail.com>
Date:   Wed Apr 22 01:00:12 2015 +0800

    Revert "Skip Misc/Overcounted battery stats in builds"
    
    This reverts commit b00d8f5cf7ff99b2393146380532067d1e4c5aa1.

commit d8b12d46fc95ee3606668ee4b98284d648173b93
Author: Lars Greiss <kufikugel@googlemail.com>
Date:   Thu Dec 11 18:20:40 2014 +0100

    Settings: make unaccounted and over-counted battery usage configurable
    
    Google disabled it for release builds here:
    
    https://github.com/SlimRoms/packages_apps_Settings/commit/e6793771cedb47aed72f1c64f870b70357746938
    
    well but it is enabled for whatever other type of builds beside the official release builds. That said it should
    be a developer option so or so and not build type dependent.
    
    Whatever added an option into developer settings to control it. Default value is false.
    
    That said.....finally no complain about misc battery stat in battery settings xD
    
    Change-Id: I7549b1c796d5d9413b4af5d80a31d6efeaf0352a
    
    Conflicts:
    	src/com/android/settings/fuelgauge/PowerUsageSummary.java

commit e629ceffc3cb9c25ae9793ab77a896347ae2bbad
Author: fusionjack <dogfight60-fusionjack@yahoo.de>
Date:   Tue Apr 21 15:37:59 2015 -0700

    Settings: option to disable lock screen shortcuts (2/2)
    
    Change-Id: Ia080a57e71c7e489350b4a5a588dd7b34339db12

commit ea9add4a8497ab72581372d90334d817e34d5f92
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 12:22:24 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/packages/apps/Settings into cm-12.1
    
    Android 5.1.1 release 1

project packages/apps/SoundRecorder/
commit 0e7ddcfa0ce1a5a5a002cd18c55b115e180f733d
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:44 2015 +0200

    Automatic translation import
    
    Change-Id: I9a45be5d27dd6e3d347b87c4c1d7ae9fa1374b37

commit 085330244000c535a7f726655bc65aab2d920cbb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:41 2015 +0200

    Automatic translation import
    
    Change-Id: Ie5e0e6460ef83fac94c6f9baa7d2f30b66393fee

commit d67f0d026eefaaa7c86ecb64701d414ba663dcf4
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:20:13 2015 +0300

    Automatic translation import
    
    Change-Id: I05732d61f1644e98f9d6d973862c4524c1ceb032

project packages/apps/Stk/
commit 2f97d8e23d497a2edc7101705d9c8575bd4bc506
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:49 2015 +0200

    Automatic translation import
    
    Change-Id: I16c007fc2872023bcc03cd48953343ccf6c55dab

commit e0d37d6cabf2ec7912ac9cf649e769adb8fb38ad
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:45 2015 +0200

    Automatic translation import
    
    Change-Id: Ib13ee0aa08e14de66393164262a3b9716870e5c4

commit 86b38f5dc7139d6dc8b8bb11013d010936a38586
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 02:30:50 2015 +0300

    Revert "stk: Remove duplicate resources"
    
    This reverts commit 756400abec166b2898196f348621d21318202efd.
    
    Change-Id: Ie3f1528cd608d8c3a8320a4ee1d971c47a9d2d07

commit 903904373a8f97ab819b68f0cbdf3f29fae70491
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 02:32:03 2015 +0300

    stk: Remove duplicate resources
    
    Change-Id: Ic081ed2b252dfa3b9d93215662d6ae50652ba885

commit 605e08f243b3188b9364600547216ee1735301d3
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:20:19 2015 +0300

    Automatic translation import
    
    Change-Id: Ifd4a7300fe5c533c8a649f76ab1c41055ce53211

project packages/apps/Terminal/
commit 07e85c9d8fc8ee6ec3813a0436272ecdee22d8b6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:48:54 2015 +0200

    Automatic translation import
    
    Change-Id: I4b294562545b9035562c97c3433270ea4ef1775d

commit 7d4c476fe2cb314a59d4ad1e110e0dec1a9de496
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:01:49 2015 +0200

    Automatic translation import
    
    Change-Id: Id0557f8c7ec6cb06351d44e4ab7d445162eea070

commit f67dd9aa6f15e57a674809faaa05676a1f124156
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:51:07 2015 +0300

    Automatic translation import
    
    Change-Id: Ie2739f6746d9e49fc4e62f8c028df1bdb56f786d

commit 4f4808e5e69c7e555c16867c695c39a5bb5363e9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:20:23 2015 +0300

    Automatic translation import
    
    Change-Id: I7c89e0a02563895066cc173793735028f0182e47

project packages/apps/ThemeChooser/
commit d758c5e81a74b6e62af6601dcae2c222b5a49a36
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:51:11 2015 +0300

    Automatic translation import
    
    Change-Id: I1e150f00f1eec05b7607b8a29d493836a99a4ef0

commit 294da1724e47055d9376ba5783b088adf7ff3e17
Merge: 87096d5 d758c5e
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:15:45 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit cec5670fe94960bb082cb02f6c1ded53174268b0
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:20:28 2015 +0300

    Automatic translation import
    
    Change-Id: Id5818c86d05fd15922da7ed5f047732339eb59d7

commit 8ebc84c90fc639df424f8515a004a1ab7d6aaa86
Merge: 294da17 cec5670
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:57:54 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/apps/TvSettings/
commit 83e6512e1a5c152abad620bc459f619761c51277
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Fri Apr 17 05:05:32 2015 -0400

    Add CyanogenMod version to the About screen
    
    Change-Id: I9b8fe822865352d32bc8d7cfa8b567dc395cef95

commit bb701bfb58e79f8afa86266575543ce37b1fccd7
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Sun Apr 19 00:16:09 2015 -0400

    About: Add CyanogenMod Updates
    
    Change-Id: I6deccd35cf1d22e51115e17fc1b94073f8fd8d3f

commit 277577521090fb717e54fed5afd1b8c8e0015762
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 00:03:52 2015 -0400

    CM PlatLogo: CyanogenMod version preference
    
    Binds the CyanogenMod version preference to launch CM easter egg
    upon multiple clicks.
    
    Change-Id: I35a909fcaf04030d4d757fcea11e2d65b29516fb

commit 2dfcba24e3804b1e39691e5928e6ecc92f0ea36a
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 00:21:16 2015 -0400

    One does not simply become a Developer
    
    Change-Id: I4e5f89496d40a04cbc6242d8580334f039d251f2

commit 8659c8df6932d15d35ab178845a6855e1dc8bc92
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 00:28:43 2015 -0400

    Add build date (ro.build.date from build.prop) to About screen.
    
    Change-Id: I695e5a8b01616cddf865223d3b037f594da35224

commit f0e8aecf46869c4928926111733a9a8897b02013
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 00:59:39 2015 -0400

    About: Show the kernel version
    
    Change-Id: Icb5059523b2064f43bf15c230cc3a983b4549c12

commit 46cbf36d1c71e37c5ed4dc92838286e231e24ee5
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 01:01:03 2015 -0400

    About: Fix greyed out titles on certain settings
    
    Explicitly setting enabled(false) causes an item to be non clickable
    and "beep" when clicked, however it also causes the title to be greyed
    out, which is inconsistent with the UX of the other items in the menu.
    The UX is consistent in this manner, but it does make the item clickable
    it just does nothing.
    
    Change-Id: I33e56a76d75b508e904ca081b3ebc81d057de595

commit 5c4f41e479f191031ca228eeda79d6e628c17361
Author: dhacker29 <dhackerdvm@gmail.com>
Date:   Tue Apr 21 02:41:30 2015 -0400

    About: Add SELinux status
    
    Change-Id: I29dab1e9dd4c718ffe442f00f6bc48a7e8c867fb

commit d72c07fc63eb6d5ff2c3cdba918ae19ccc51bd25
Merge: 5c4f41e dcd9bca
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:20:12 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/packages/apps/TvSettings into cm-12.1
    
    Android 5.1.1 release 1

project packages/apps/UnifiedEmail/
commit 6fb64f4e9506ffdaf4708c816f63df28b2d0fda9
Merge: d44ec61 5ab9abe
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:53:24 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 23eb3665b6539ddbd0d10bf47667948c4754490c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:51:24 2015 +0300

    Automatic translation import
    
    Change-Id: Iee719a7a989317772a03928684a23155167c1ce0

commit 14fb05cfcae884c81cbf3d0c68dcb0d7b8c357fb
Merge: 6fb64f4 23eb366
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:17:59 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 7a1081dd07514bdeecaba313402ff87798063ea2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:20:42 2015 +0300

    Automatic translation import
    
    Change-Id: If79e79ce58345aa89b7dca7b5869d530ca9bfbda

commit 2128ba610902a9aac3b20953ebfb44a3bf9dc8f5
Merge: 14fb05c 7a1081d
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:36:28 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 85f5d282b0bd7de601eb32074f2c4292a16dc922
Author: Jorge Ruesga <jorge@ruesga.com>
Date:   Sun Apr 19 23:50:53 2015 +0200

    email: linkify urls in plain text emails
    
    Change-Id: I44470b6b5a1ec7787e8876e2ec74ac6c8508dbe6
    JIRA: CYAN-2925
    Signed-off-by: Jorge Ruesga <jorge@ruesga.com>

commit 2bba20c8356e8aae265b72c4c02cc6e0724c79a9
Merge: 2128ba6 85f5d28
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:58:33 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/inputmethods/LatinIME/
commit 434b5fdf53a3dca09ed3f916d6dbb7b0af253b2e
Merge: 6d1c8e9 4585f32
Author: Steve Kondik <steve@cyngn.com>
Date:   Tue Apr 21 11:20:19 2015 -0700

    Merge tag 'android-5.1.1_r1' of https://android.googlesource.com/platform/packages/inputmethods/LatinIME into cm-12.1
    
    Android 5.1.1 release 1

project packages/providers/DownloadProvider/
commit 5036c4f70e561051afa359955a063d464132111e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:53 2015 +0200

    Automatic translation import
    
    Change-Id: Ib0d03cb90567d7ac6123c2c97be226ef65859ca7

commit 023cd3869e6a5cddb32ff2121b40b23382a4e1d1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:36 2015 +0200

    Automatic translation import
    
    Change-Id: I15637e50c23af7f4e60a791983923ae65329cb66

commit 7fd50d60fe05d9d9729c53e55ffd0a8600f67aec
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:26 2015 +0300

    Automatic translation import
    
    Change-Id: Ibbc67e28ce7e312fc66deb7b60f9e69716f14524

commit 145c95cd8c30be7880351a556c1f7f74e299b092
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:05 2015 +0300

    Automatic translation import
    
    Change-Id: I78657e7160bf1ca60271984d56344a588ffbf0ae

commit b1e932c6d0e1b52ac084ad7531d08a51d003d4bf
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:21:45 2015 +0300

    Automatic translation import
    
    Change-Id: Iaff268dcb9907a46702dfeaf106c0263a15e31d1

project packages/providers/MediaProvider/
commit ecd7d551ca8e1099978936a38e1c39f3d5540c8b
Author: wjiang <wjiang@codeaurora.org>
Date:   Wed Sep 10 17:52:27 2014 +0800

    MediaProvider: don't delete entries of secondary storage on shutdown
    
    All rows on external SD card will be deleted by fault due to eject
    intent on shutdown is received. Don't proceed under this circumstance.
    
    Change-Id: I7de7d3cdedcd5512f1f3f9541184d099ce7bfd9f

commit 9ec4be05106a07accd906d7113190b0e030b675c
Merge: e6041cd ecd7d55
Author: ZION959 <ziontran@gmail.com>
Date:   Mon Apr 20 20:44:15 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/providers/ThemesProvider/
commit c6b89d89897e62d959bc55934490913704054934
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:49:57 2015 +0200

    Automatic translation import
    
    Change-Id: Ic3e8aad4d67edc9afc8080e8c23aacd641ee5cfa

commit 66f360cc1fba7e6f5126df41c556e734058f7871
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:40 2015 +0200

    Automatic translation import
    
    Change-Id: Ia8f6a673434b345a4d9a6d8e903f936587d20737

commit 8e2b36126617748c20dad975d0c1f8facaa3d11e
Author: d34d <clark@cyngn.com>
Date:   Wed Mar 18 14:07:24 2015 -0700

    Fix icons with filters not being generated
    
    If a theme has composed icons that only use color filters, they
    would not get generated.  This patch resolves that issue.
    
    Change-Id: If9076eca8cce1a85beed54ce30f0dfb8bbcd3188
    REF: CHOOSER-63

commit d6c69145c554db81855d7c72f69d2008b7f21417
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

project packages/services/Mms/
commit 0cf722245a56adef45f6c70fafecf7491ad40332
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:03 2015 +0200

    Automatic translation import
    
    Change-Id: Id569ae5e8f5048a2de22bd94c0bbfb6a76309c72

commit c207f1230eefd991f6a281926326f05bf29a1a72
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:45 2015 +0200

    Automatic translation import
    
    Change-Id: I3b02c952dc57ddab8ffa1648cac8bbf9c2b58728

commit 0852a23f582a7b962765e6b264e18cf1a5b4c470
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:21:49 2015 +0300

    Automatic translation import
    
    Change-Id: Ia51fedea37ed1c11bceea89d76939a8c47d37cad

project packages/services/Telecomm/
commit 72d80db457cde0eeceb69e254a6b3cd0b8e75cf0
Merge: 51eb0a9 2f70b20
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 14 23:51:40 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 085ea0143c63b29bb05c0d7c3c775fbbe360e452
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:07 2015 +0200

    Automatic translation import
    
    Change-Id: I62eee2d91dae9d4f8b81255bc75f761c69459710

commit c7b91d47336846adeb55f88837c3c6e5e198cb5b
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:48 2015 +0200

    Automatic translation import
    
    Change-Id: Ic50787a9931bbaf4d1c3917dd3c57a27ce380f15

commit b14ff4d5423f547952d584e987dc0e302cae9316
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:11 2015 +0300

    Automatic translation import
    
    Change-Id: I69de8d051c907107437ca42092d4184d0ab3505e

commit bbefc63dacfc541b055ec0e8a66c40b60fe14463
Merge: 72d80db b14ff4d
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:14:36 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/services/Telephony/
commit a6c4d57cc607ad3fd15fd5903f693e5e6d395522
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:53 2015 +0200

    Automatic translation import
    
    Change-Id: I4845cdb26200b756e304485d692501295f42e226

commit 18c68f9fa92de0f7e81628fbf35b90067294e1d5
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:32 2015 +0300

    Automatic translation import
    
    Change-Id: Ibca17b4acd084e5f7dc44ef23284117db9a28e82

commit 509e3e912d8232366e97f5d75769e2b9eb7ea56e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:16 2015 +0300

    Automatic translation import
    
    Change-Id: Ia779a7f3248af501310fe92aa89dfe8f4e28e09d

commit b38a6c5ea740855ff7c49e7b42bd953624ae6c76
Merge: 6290b31 509e3e9
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 22:15:01 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 982add75c7d920fd29bae7c87d187686ed6176a2
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:21:53 2015 +0300

    Automatic translation import
    
    Change-Id: I497b8fdc8ef4cec5d28f0ff51a8a156298a7e58d

commit a7818484ecca1b87040d54ae42c2c28f65877e85
Merge: b38a6c5 982add7
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 22:35:20 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit d63de10ca52c828c2681c75326c907a1be146d3d
Author: Lin Ma <lma@cyngn.com>
Date:   Tue Mar 24 21:09:27 2015 -0700

    TeleService: Set mode to 2g on other sim(DSDS) prior to change
    
    * Fix a bug where other SIM slot gets changed when
    user wants to change the preferred network type.
    original commit 69efa99f1cd4afdaeec4554475594bc6a2900338
    
    Change-Id: I69fde842b1c27601752cd3a1078664eb26d86fe1

commit 34c31332e62482ff1a08b60c30ec510a9c26a467
Author: Adnan Begovic <adnan@cyngn.com>
Date:   Mon Mar 23 13:32:29 2015 -0700

    TelephonyService: Don't change preferred network type on multi RAT capable devices.
    
      69efa99f1 introduced setting the preferred network type to 2g on the other
      sim on a DSDS. However, on a CDMA/GSM multisim device, this should be
      avoided.
    
      Thus we introduce ro.ril.multi_rat_capable to discriminate against
      mutli rat capable devices.
    
    Change-Id: I16524a52e0d350a03f48d7d4cb8307fce556979d

commit 75f71223d15e83bfccce6570d3f38659c0f12dd3
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Mon Mar 30 19:22:44 2015 -0700

    Telephony: KK upgrade path to re-enable components for MSim
    
    Change-Id: Ie21b80d9b6b39ba30fddd6fd268d80cca7f6cb10

commit 7acd2cc413581e3f9660c917ffffce2ffa1157d4
Author: Raj Yengisetty <rajesh@cyngn.com>
Date:   Tue Mar 31 13:34:56 2015 -0700

     Telephony: check equality when verifying enabled state
    
    Change-Id: I2dea47a180e30abb0423d8b20395e08d3406bca8

commit 1ba1f5a239580fab44879ad6e9b81e95630a2fff
Author: Lin Ma <lma@cyngn.com>
Date:   Wed Apr 8 10:49:06 2015 -0700

    Telephony: Allow customizing display name for different phone
    technology
    
    * 3G modes such as EV-DO, WCDMA etc are currently displayed as
    "3G" in mobile network settings. Some customers want to display
    the actual technology name instead of "3G".
    * To maintain backward compatibility, the default strings for all
    3G technology are still "3G" (same for LTE and 2G), but the names
    can be overwritten in overlay files
    
    Change-Id: Ia1cc6c73300ff15ff9b28a6db054c6ba9adfa890

commit 5177d6972037c321e8844e665b86918cf2c1331c
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 14 01:39:26 2015 +0300

    Set untranslatables
    
    Change-Id: Ifbdc16ac450d3ec117ec69d132012580043f499c

commit 354092e1804bb80e7474151badb3a0616892dc8f
Author: cretin45 <cretin45@gmail.com>
Date:   Thu Apr 16 14:06:14 2015 -0700

    TeleService: Don't show video calling switch if not supported
    
    Change-Id: I2b9fa5afc3f5badcc836736cf79e24ca46dc1a9d

commit f39838eda5d9225ac2d460af052af72c502751ab
Author: Altaf-Mahdi <altaf.mahdi@gmail.com>
Date:   Tue Mar 31 16:06:25 2015 +0100

    Telephony: make call waiting option a switch preference
    
    Change-Id: Idb46fbe8a338c8ae6df3e5c218cfc5c0921327fe

commit f3b8de459257888eb1d575f0e48f186ec9821de7
Merge: a781848 f39838e
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 13:57:24 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project packages/wallpapers/Galaxy4/
commit 8d0fcb70755ae5d583b4cee3512e2e1c0014d3d6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:22 2015 +0300

    Automatic translation import
    
    Change-Id: I057c77f49ba6edb3ce513d3402698f203bc7a200

commit 2453b7eaf0c9017d4b6f7c8f9a2e733d9b2a2c13
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:18 2015 +0200

    Automatic translation import
    
    Change-Id: Id45661d16d340f3801c92c01ec38cb0eb5071ea6

commit 5f1b78ac70fb8f5f2003eeb78c91f55e847a1d0e
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:02:58 2015 +0200

    Automatic translation import
    
    Change-Id: I1f255675c812ca6ccd94f26bd7ed177bc9e26919

commit 010e98f2c0676f606818ab0db29b465f70331134
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:41 2015 +0300

    Automatic translation import
    
    Change-Id: I108e5cfe9f6fc0da0930c60c49b5a80368362faa

commit 12e1dd59bfc7e0f16a2431683c4119dd7a65fa91
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:21:59 2015 +0300

    Automatic translation import
    
    Change-Id: I5aa22419cd26ea75addbf0ca90cf5a5fe186edde

project packages/wallpapers/PhaseBeam/
commit c1cdb045f49141c8e9c80cf19bdb76ee1e5b77ef
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:28 2015 +0300

    Automatic translation import
    
    Change-Id: I094f9036bfe787f4cabb9e464559aee29ffd6439

commit 57ea23911828fad60e10b702ec0a83dcb6200c46
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:23 2015 +0200

    Automatic translation import
    
    Change-Id: I0d2533e714b93d7224eb9599c1bb7297c8dc8230

commit b1f701a03eb2d1e99b46b96471e7da7271f683c6
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:03:06 2015 +0200

    Automatic translation import
    
    Change-Id: I5dfb1357529c4d7c8a63e4932c886e663f914dd2

commit 241d0631028c9f99935167142df89b7300e43c82
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:47 2015 +0300

    Automatic translation import
    
    Change-Id: If1a3c8cacaff9d9df8eee74cb594e0411290a849

commit b2b24cc7863ce94e09dc7da0c87c5b05116e6ca9
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:22:03 2015 +0300

    Automatic translation import
    
    Change-Id: Ia9cabd509a1a0b378555903590bd15754dafbe41

project packages/wallpapers/PhotoPhase/
commit e18fc24f3e191a72fe5fafc0602e016473e20db1
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 15 01:50:28 2015 +0200

    Automatic translation import
    
    Change-Id: I21241d7958cd14d847de18fe324e6206e257b56c

commit 0fb8dcc47ff1ce3d534eb7e2cdf8c24e04155ceb
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Sun Mar 22 20:03:11 2015 +0200

    Automatic translation import
    
    Change-Id: I89413b87402cfd6f09638e1f6ad2beebe4a5a969

commit 8cc52f78f054b55a2c0e9f3aa5071af52a0a24da
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Mar 31 01:53:53 2015 +0300

    Automatic translation import
    
    Change-Id: I787229f334517816307e7371d82a8e5d2a1e437a

commit 65cf58ddfff33381eb36f5322276143426e98f14
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Tue Apr 7 00:52:33 2015 +0300

    Automatic translation import
    
    Change-Id: I0365a713741f2e964be5671bb33bbaf5b6fd4d96

commit 3488b629836456166f8c95b911be2e9f908ed5db
Author: Michael Bestas <mikeioannina@gmail.com>
Date:   Fri Apr 17 22:22:07 2015 +0300

    Automatic translation import
    
    Change-Id: Iccc87dc2ed862341bb2580fc7394eba18b4df572

project system/core/
commit 52c51f96b57572babcd12984a0f67bb71faf6877
Author: Christopher R. Palmer <crpalmer@gmail.com>
Date:   Wed Apr 8 20:45:22 2015 -0400

    init: Add a new keywork "log" that logs a message
    
    Change-Id: I41264fa6768d3c3720a55c9820073047d3fb1349

commit f60137983c07bd297cf102b57c1153644bac744f
Merge: 25f103c 52c51f9
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 17 10:48:59 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

commit 68248e178eaf12793d1976af211653ca156176c8
Author: Tom Marshall <tdm@cyngn.com>
Date:   Fri Apr 17 05:25:03 2015 -0700

    fastboot: Add lz4 libs
    
     * Required by transparent compresssion in make_ext4fs.
    
    Change-Id: I408b5374524b5b8abaf008cf8f4c10ff90376d3e

commit 3e859ca6bf30ad3ea22f6e919ea7297396aa3f78
Merge: f601379 68248e1
Author: ZION959 <ziontran@gmail.com>
Date:   Sat Apr 18 00:05:22 2015 -0700

    Merge remote-tracking branch 'CM/cm-12.1' into cm-12.1

project system/extras/
commit 3ba17afa88e3380c8108de666f9e7b3fb5ee6484
Author: Tom Marshall <tdm@cyngn.com>
Date:   Wed Mar 25 06:16:52 2015 -0700

    make_ext4fs: Transparent compression support
    
    Add the following options:
    
    "-M" specifies the compression method.  Supported methods always include
    zlib, and will include lz4 if available.
    
    "-Z" specifies a comma separated list of file extensions to be compressed.
    Compressed files are indicated in the filesystem by setting xattrs
    user.compression.method and user.compression.realsize.
    
    Change-Id: I459cb0284841a860630458835e56246e58f7f3f3

commit c98abe03be9a2ce772ce705655783bdf4beb8425
Author: Steve Kondik <steve@cyngn.com>
Date:   Fri Apr 17 18:25:24 2015 -0700

    make_ext4fs: Fix buffer allocation for lz4 compressor
    
    Change-Id: Ic43505b3cdbce6dd32ce30ba7bba49ff9cf04f03

project vendor/cm/
commit fd6bfe7bf005d551286a7e77d2b1dd09f2272162
Author: Ricardo Cerqueira <ricardo@cyngn.com>
Date:   Mon Mar 16 12:22:11 2015 +0000

    Remove userinit from user builds
    
    /data is supposed to be inaccessible to begin with, and we don't
    want the init sequence tampered with for user builds
    
    Change-Id: If3eb5573248956a14ad56516a9871758f4c00989
    (cherry picked from commit a9d772166365a27181a7441c10a6c60a2bab7dab)

commit 8e9b0ac1fdb3e39a7eafbe01b19b0f4bffcbb79d
Author: black <blackzigong@gmail.com>
Date:   Wed Apr 15 09:19:49 2015 -0700

    Remove SPN configurations for Japan
    
    These configurations has been causing problems since Android 5.1:
    A docomo SIM card is regarded as no service.
    A Y!mobile SIM card is regarded as Softbank.
    
    Change-Id: Iead54ef9eff1d4bf0d472eb588fcda000cb228ad
    (cherry picked from commit d60d2fd669aa75b49f7dba6a141008e1d9ea414c)

commit 206c46e8e04d48fda340a9ba10da2636d399a535
Author: Dušan Šušić <dusan.susic@gmail.com>
Date:   Sun Apr 19 08:59:20 2015 +0200

    We are at CM12.1 now
    
    Change-Id: I357a379546c97a341e68affc26b60aebd1e94663

commit 785c50ad3f55c8bbcacdd48d00dbff76c68447d7
Author: Roman Birg <roman@cyngn.com>
Date:   Fri Mar 27 11:42:11 2015 -0700

    vendor: add sepolicy entry for killswitch service
    
    Change-Id: Ib3c44c50138f5715d92addbf8df7ed591785b550
    Signed-off-by: Roman Birg <roman@cyngn.com>
    (cherry picked from commit 2ca5d3999b35d328f0969a264009bffe0faf889d)

commit 365ed9bd65dcefd13e7f2a6dfaa5485aa4229ab0
Author: Brinly Taylor <uberlaggydarwin@gmail.com>
Date:   Sun Apr 19 16:55:09 2015 +0930

    vendor:cm: update contributors
    
    * Add PatrikKT as a Desire 601 (co-maintainer)
    * Add Desire Eye & Moto MAXX & Oppo N3
    * Fix formatting for an Xperia Z3 Tablet
    
    Change-Id: Ic477056991ad82f9ec8746f698c0732987fdf027

commit b02640c228f7b019fb229a28a1cac41357cef624
Author: heydabop <heydabop@gmail.com>
Date:   Sat Apr 18 17:55:22 2015 -0500

    Add hipri to ATT Phone APN
    
    per http://www.att.com/esupport/article.jsp?sid=KB424489&cv=820
    
    Change-Id: Ib6552dd6358e2198f9e1da8420cc72da1664c606

commit a99128f1b0a2bed5e61b4b2d48b447e0ee6a62f5
Author: Maxime Auvy <maxime.auvy@utt.fr>
Date:   Tue Apr 21 11:32:58 2015 +0200

    Updated Free Mobile APN
    
    Change-Id: I60ea016bfc840c0aaf4b8a0bbde026ebd68beb3e
    (cherry picked from commit 81bd45a8bef18c7c1570b657c0bde122eeb6feb6)
    (cherry picked from commit d7aa97853e33a4315563751431e10f611c20c2f5)

project vendor/cmremix/
commit e8cded6f57eb684b957bb2025e3e898c41050092
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 11:31:03 2015 -0700

    Saberize for all support device

commit 6b5d217c920751c1a246f08005013878e6660e76
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Tue Mar 31 07:34:31 2015 -0600

    Add -floop-nest-optimize to graphite kernel flags
    
    -floop-nest-optimize is a isl based flag, so it is
    considered a graphite flag.
    
    Change-Id: I1ae81d3daab7b196f781cc518185269df70c988c
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit aaacadc909ebead143e1eb71f5854891fa510dc8
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 11:34:45 2015 -0700

    Remove TARGET_LIB_VERSION and change lib path to just lib
    
    TARGET_LIB_VERSION is no longer needed since the graphite libs are
    in lib of the toolchains.
    
    Change-Id: I83ee5bc8ea73f121039a6b7a6d0619b476a39c56
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	products/sm_hammerhead.mk

commit 6838da5456de12c3c60a3b39dd43db05c48f9692
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 11:44:03 2015 -0700

    MOAR SaberMod flags (1/3):
    
    This patch was tested on hammerhead, may need adapting for optimal
    performance on other device.
    
    Change-Id: I6db033258698dad10c95c810ddc3ad710e578a0d
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	products/pa_deb.mk
    	products/pa_flo.mk
    	products/pa_flounder.mk
    	products/pa_grouper.mk
    	products/pa_mako.mk
    	products/pa_manta.mk
    	products/pa_shamu.mk
    	products/pa_tilapia.mk
    	products/sm_hammerhead.mk

commit e88366512bc29abf1083ad4a119225ab31c3345a
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 11:46:56 2015 -0700

    extra sabermod C flags:
    
    Use thread sanitizer intead of address sanitizer.
    The thread sanitizer scores a little better performance than address.
    
    Change-Id: I4fbaff059c71e55ae0ac5b946b1431a2131fbdc6
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit a45163c90d392ee4546c92fa9fcd70e28f7500d0
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Wed Apr 15 17:26:15 2015 -0600

    enable graphite and -O3 form libwebviewchromium
    
    Change-Id: I99c066f45d543e642496dbd6e18ca8733a7e20d0
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit f4b56ad8b4abe3ed0d20fc820f382c2ab4298da6
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 00:42:31 2015 -0600

    Add some basic host optimizations (1/2)
    
    This is mostly beneficial when used with -O3 optimizations
    
    Change-Id: I3c894ffdd0cfb97dab5532b7dc5bb31c7ecb1af9
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>

commit 57c508f6d133d3bf89f61160dffe4aedd6af3b05
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 11:54:00 2015 -0700

    update sm.mk:  cleanup graphite flags
    
    -Allow graphite flags to overrided by device.
    -Remove -floop-parallize-all.  This isn't useful without -ftree-parallize-loops="number of threads"
     Since not all devices have the same number of cores or threads this should be device specific.
    
    Change-Id: I5e03a6b2136d7efb786894357304fff40800bfbd
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	config/cmremix_sm.mk

commit 5f642a1119a04f495e586759a02954141b5e5e63
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 12:04:29 2015 -0700

    sm.mk:  Don't add when exporting
    
    Change-Id: Idd8f2a9574543f43a97a71623a7e4864c1c28d6a
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	products/sm_hlte.mk

commit caeaa56d000c350083ae84f845310e06943b9868
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Thu Apr 16 12:09:33 2015 -0700

    Move shell unset variables outside of device makefiles
    
    Change-Id: I49e7c8325de7fa78ea5462e67eeaf4999d184532
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	products/AndroidProducts.mk
    	products/pa_deb.mk
    	products/pa_flo.mk
    	products/pa_flounder.mk
    	products/pa_grouper.mk
    	products/pa_mako.mk
    	products/pa_manta.mk
    	products/pa_shamu.mk
    	products/pa_tilapia.mk

commit f836b859f78c8682e71de6036bfe94608e7f3ff5
Author: ZION959 <ziontran@gmail.com>
Date:   Thu Apr 16 18:43:18 2015 -0700

    Target arch is arm and compile ROM and KERNEL with SM 4.9

commit 75863a629592aee0ad3e3751cd5f2abb26f0992c
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 17 08:23:55 2015 -0700

    [2/2] add force disable strict modules

commit 933408b5c95c98ebf3b2bdd9b3dbea71563a5e9d
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 17 10:25:47 2015 -0700

    back to SaberMod Gcc 4.8 for rom & 4.9 for kernel

commit 52efba7f74eab55b3ec870212c35b85d8a2e45f1
Author: ZION959 <ziontran@gmail.com>
Date:   Fri Apr 17 22:43:23 2015 -0700

    remove opencamera

commit 62f37e007c431a3acee3abeb589d3c2e6c8c3c4a
Author: Paul Beeler <pbeeler80@gmail.com>
Date:   Fri Apr 17 23:18:00 2015 -0700

    Fix build for hammerhead, create sm_clear_vars.mk and add -pipe
    
    Change-Id: I12f6c5e14cab25752fab4eda297afe12eb8dcff4
    Signed-off-by: Paul Beeler <pbeeler80@gmail.com>
    
    Conflicts:
    	products/AndroidProducts.mk
    	products/sm_hlte.mk

commit b969641635c8db8b0c78f569ddf9676ac60a7a91
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 19 17:58:54 2015 -0700

    clean up

commit 92c6856079648e31de3abf247e9851da673a3288
Author: ZION959 <ziontran@gmail.com>
Date:   Sun Apr 19 18:38:49 2015 -0700

    add opencamera again

commit ec824f684cd429d0f6d956644e9f5329ae620bc1
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 02:18:23 2015 -0700

    build KernelAdiutor and floating button

commit b991b59dcda8dff697919ad69d2ac6487dd62261
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 07:59:36 2015 -0700

    remove omni performance control & screen record

commit 0ecd20df14cd0f60e4ee94614f07dd20fe625fc4
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 15:12:37 2015 -0700

    clean up changelog

commit db53e2795b1b9d9df214475a585f5a805740f0c7
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 19:37:00 2015 -0700

    move weekly change from build script to tools

commit 7dabb072a23d1e3411dbc0ab24768659eef9dc39
Author: ZION959 <ziontran@gmail.com>
Date:   Tue Apr 21 18:47:26 2015 -0700

    bump cmremix to android lollipop-5.1.1_r1
