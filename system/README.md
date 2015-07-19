### NEC Terrain system and its components

I did some research and present here lists of apps which should be left in the system,
which I have disabled and which I installed in order to replce stock or add functionality.

These lists reflect my **personal** opinion and can differ with yours. You should not blame me for this.
Moreover, I'm not affiliated with any programmer/developer. Think for yourself before you disable and
especially remove packages.

Also note
that the information was taken from my personal digging inside the phone. Do not think
it is 100% correct, better check.


As an assurance, any statement below has been verified by me and not just copy-pasted from another internet source.
Currently in my phone all apps from the `disable` list below are indeed disabled and I confirm that:
* it boots
* it works normally
* it makes calls, receives calls
* the same for sms-s
* works with wifi
* data connection 4G works
* both cameras and microphone work
* charging goes as expected
* external sd-card is accessible
* syncing with google account does not produce errors
* etc

#### Apps from the stock rom which I left and why (raw list of packages in `apkensys`)

* android=/system/framework/framework-res.apk

  very system
* com.android.bluetooth=/system/app/Bluetooth.apk

  very system - bt
* com.android.certinstaller=/system/app/CertInstaller.apk

  very system - about certificates, seems important
* com.android.contacts=/system/app/Contacts.apk

  very system. This app is used not only to show, but also to add contacts. If you disable it, you cannot add contact to your phone storage anymore because
  even any replacement app uses the interface of this one. It provides some *service* to do this. Already stored contacts can be viewd, however. 
  If you still insist to disabel/remove this, you *will* have to install an alternative dialer at least
  as the stock dialer will disapper from any graphical view (but will be still enabled though).
  Note, that this program *does not start* if you disable/remove `com.android.att.settings.provider` but its part for adding contacts to the phone storage
  will still function properly if being called from a third-party program.
  
  I however wanted to avoid this app as much as I can because I'm fed up with the fact that anytime I start it, it communicates to the internet switching data connection on, at least
  for few secs, even if there is wifi and even if before the data connection was off.
  
  So, since I have failed so far to disable this app I did like that:
  
  * I installed **DW Contacts**, which has a diler as well
  * I disabled `com.android.att.settings.provider` and this automatically closed for me the full stock `contacts` (but not disabled them)
  * Now I use DW Contacts to make calls. The actual call is made using the stock `Phone` program internals, its pictures
  * When I add contacts in DW Contacts I see the interface of original `contacts`
  * BUT the data-connection has gone!
* com.android.defcontainer=/system/app/DefaultContainerService.apk

  very system, looks like
* com.android.keychain=/system/app/KeyChain.apk

  very system, looks like
* com.android.launcher=/system/app/Launcher2.apk

  very system, looks like
* com.android.nfc=/system/app/Nfc.apk

  I guess this and next can be disabled if you do not need NFC, which eats your bettery, I left for a moment, do not know why
* com.android.nfchiddenmenu=/system/app/NfcHiddenMenu.apk

  I guess this and previous can be disabled if you do not need NFC, which eats your bettery, I left for a moment, do not know why
* com.android.packageinstaller=/system/app/PackageInstaller.apk

  very system, if you disable it, you will have to stick to `apk` download, adb and `pm`
* com.android.phone=/system/app/Phone.apk

  You will not be able to make calls w/o this. It is not just graphics, also some binary internals to communicate with the modem, proprietary
* com.android.providers.applications=/system/app/ApplicationsProvider.apk

  Removing this will disintegrate your system. It may start, perhaps, but apps will not communicate one to each other. This is not that nice and causes many to stop with errors. 
* com.android.providers.contacts=/system/app/ContactsProvider.apk

  This is about the phone contacts storage, if disabled, no contacts in the phone can be stored
* com.android.providers.downloads=/system/app/DownloadProvider.apk

  Some settings for downloads, not sure it is really critical, but seems that some apps like playstore rely on it and do not bother themselve about where to store what
* com.android.providers.downloads.ui=/system/app/DownloadProviderUi.apk

  It is to see graphically, what and where has been saved, perhaps can be disabled/removed
* com.android.providers.drm=/system/app/DrmProvider.apk

  **not sure** what exactly this guy stores, but some databases look like mime-types identification
* com.android.providers.media=/system/app/MediaProvider.apk

  A centralized databse about where media files are, so that players see them all
* com.android.providers.settings=/system/app/SettingsProvider.apk

  **not sure** what exactly this guy stores, but looks important
* com.android.providers.telephony=/system/app/TelephonyProvider.apk

  The database which identifies a numeric gsm network id with the name
* com.android.provision=/system/app/Provision.apk

  People say, it is important and its data look so, but not sure, what is it exactly
* com.android.settings=/system/app/Settings.apk

  Your setting interface
* com.android.sharedstoragebackup=/system/app/SharedStorageBackup.apk

  **THIS IS NOT A BACKUP SOMEWHERE, THIS IS INSIDE YOUR PHONE APPS COMMUNICATION**
  
  If disabled/removed, some apps, watsapp and skype in particular *DO NOT* autostart, do not disable
* com.android.smspush=/system/app/WAPPushManager.apk

  It is said to be realted to tethering operation, did not check myself inside
* com.android.stk=/system/app/Stk.apk

  Looks system
* com.android.systemui=/system/app/SystemUI.apk

  Looks system, the graphiccal interface in fact
* com.android.vending=/data/app/com.android.vending-2.apk

  Looks system and is related to playservices
* com.android.vpndialogs=/system/app/VpnDialogs.apk

  Used for vpns and perhaps can be disabled/removed, if you are sure that vpn is not for you. Or may be there are better replacements
* com.google.android.apps.maps=/data/app/com.google.android.apps.maps-1.apk

  Google maps, I like
* com.google.android.gms=/data/app/com.google.android.gms-1.apk

  Needed for hangouts
* com.google.android.gsf=/system/app/GoogleServicesFramework.apk

  google-service-framework, sounds system
* com.google.android.gsf.login=/system/app/GoogleLoginService.apk

  google-service-framework addition, sounds system
* com.google.android.location=/system/app/NetworkLocation.apk

  Location service, needed for maps w/o gps
* com.google.android.onetimeinitializer=/system/app/OneTimeInitializer.apk

  Not used at all but one time when playstore is initialized, so if you will replay your system from zero, it should be in place
* com.google.android.street=/system/app/Street.apk

  Street view, useful
* com.google.android.syncadapters.contacts=/system/app/GoogleContactsSyncAdapter.apk

  Sync of your contacts to the google account
* com.google.android.talk=/data/app/com.google.android.talk-1.apk

  hangouts, I have to use it becasue of my colleagues
* com.ipsec.vpnclient=/system/app/VpnClient.apk

  VPN client, I can easily use it, but mey be it is crappy and replaceable, I do not know
* com.koushikdutta.superuser=/system/app/Superuser.apk

  *SUperuser, I need. Of course, it was __not__ in stock, but I put it before in the rom by hands*
* com.kpt_nec.adaptxt=/system/app/NEC_Adaptxt_Base_v1_2.apk

  Not sure it is useful, but I kept for a moment. Do not know why
* com.nec.android.ncmc.ecomode=/system/app/EcoMode.apk

  ECO-mode, nec specific. Seems it can be off here, but I kept, let it save battery, may. Not sure, it is useful, though
* com.quicinc.fmradio=/system/app/FM.apk

  Perhaps crappy and replacable but for me enough for the moment

#### Apps from the stock rom which I **disabled** and why (raw list of packages in `apkdissys`)

* borqs.soundrecorder=/system/app/SoundRecorder.apk

  It is the sound recorder, crappy and replaeable
* com.amazon.kindle=/system/app/KindleForAndroid-0.9.11-STUB.apk

  It is the kindle, why
* com.android.DeviceHelp=/system/app/DeviceHelp.apk

  I do not need this, better use my laptop for help
* com.android.apps.tag=/system/app/Tag.apk

  **unknown** but removing did not cause troubles
* com.android.att.settings.provider=/system/app/ATTSettingsProvider.apk

  This **can** be removed but then ATT soft update does not work and stock `contacts` do not start. However, `contacts` **SHOULD NOT BE TOUCHED**, see in the list of still enabled apps why
* com.android.backupconfirm=/system/app/BackupRestoreConfirmation.apk

  Most likely related to a backup of *data*, not *settings* to your online (gmail) account. Not needed for me
* com.android.browser=/system/app/Browser.apk

  Stock crappy browser
* com.android.calculator2=/system/app/Calculator.apk

  Stock useless calculator
* com.android.calendar=/system/app/Calendar.apk

  Stock poor calendar
* com.android.chrome=/system/app/Chrome.apk

  Chrome, which I disfavor in view of Firefox
* com.android.contacts.map=/system/app/ContactMap.apk

  This to show a location of your contact given a zip code. Useless for me
* com.android.deskclock=/system/app/DeskClock.apk

  Crappy stock desktop clock
* com.android.email=/system/app/Email.apk

  Annoying stock e-mail
* com.android.facelock=/system/app/FaceLock.apk

  face-lock: I'm not crazy to trust it. Passwords only
* com.android.gallery3d=/system/app/Gallery2.apk

  It is the stock gallery, there are better and smaller around
* com.android.htmlviewer=/system/app/HTMLViewer.apk

  Not sure why, but removing it cause no issues
* com.android.magicsmoke=/system/app/MagicSmokeWallpapers.apk

  Wallpaper to eat you battery
* com.android.mms=/system/app/Mms.apk

  Stock sms/mms. The only feature it has compared to concurents - managing sim-card sms. Used to be the fact in around 1995-2005
* com.android.music=/system/app/Music.apk

  Stock music player. There is VLC
* com.android.musicfx=/system/app/MusicFX.apk

  Stock music player enhancement. There is VLC
* com.android.musicvis=/system/app/VisualizationWallpapers.apk

  Wallpaper to eat you battery
* com.android.noisefield=/system/app/NoiseField.apk

  Wallpaper to eat you battery, if I'm not mistaken, removal is issue-free
* com.android.phasebeam=/system/app/PhaseBeam.apk

  Wallpaper to eat you battery
* com.android.protips=/system/app/Protips.apk

  **unknown** but removing did not cause troubles
* com.android.providers.attxmlprovider=/system/app/ATTXmlProvider.apk

  ATT stuff but even w/o it `contacts` and connection to soft update worked
* com.android.providers.calendar=/system/app/CalendarProvider.apk

  Stock calendar. Not bad, but there are better
* com.android.providers.partnerbookmarks=/system/app/PartnerBookmarksProvider.apk

  **unknown** but seems to be sam advert, removed w/o issues
* com.android.providers.userdictionary=/system/app/UserDictionaryProvider.apk

  Your dictionary if you want to give new words to the phone, he is not smart initially
* com.android.videoeditor=/system/app/VideoEditor.apk

  Stock video edito, why
* com.android.voicedialer=/system/app/VoiceDialer.apk

  Stock voicediler, not for me
* com.android.wallpaper=/system/app/LiveWallpapers.apk

  Wallpaper management to eat you battery
* com.android.wallpaper.holospiral=/system/app/HoloSpiralWallpaper.apk

  Wallpaper to eat you battery
* com.android.wallpaper.livepicker=/system/app/LiveWallpapersPicker.apk

  Wallpaper picker to eat you battery
* com.att.eptt=/system/app/EPTTVPL.apk

  In particular *eptt* said in my native language means kind of "mother f&#ker", and it is
* com.att.myWireless=/system/app/myATT_VPL_v5.apk

  I think to connect to att hotspots, I'm in Europe
* com.borqs.camera=/system/app/BorqsCamera.apk

  Stock camera, crappy
* com.borqs.dm=/system/app/DeviceManagement.apk

  Some device management, perhaps to use borqs apps with camera and sd card. No camera soft - nothing to manage
* com.borqs.exif=/system/app/Exif.apk

  Used in gallery to decifer photo metadate. I removed this gallery, so no use
* com.borqs.facebooksyncadapter=/system/app/FacebookSyncProvider.apk

  Send your photo to facebook, but no camera soft from borqs already
* com.borqs.filemanager=/system/app/BorqsFileManager.apk

  Perhaps, to list photos in the gallery which I removed, no other use found
* com.borqs.flickr=/system/app/Flickr.apk

  Send your photo to flickr, but no camera soft from borqs already
* com.borqs.gif=/system/app/Gif.apk

  Make unimated gifs, or play them, I do not care, there are better apps for this
* com.borqs.hotspot=/system/app/hotspot.apk

  Some collection of us-based hotspot addresse, I'm in Europe
* com.borqs.movie=/system/app/BorqsVideoPlayer.apk

  To play your clips. There is VLC
* com.borqs.sdaccess=/system/app/DeviceManagementSDAccess.apk

  sdcard access to manage photos, only for this, other apps do it on their own - remove
* com.borqs.tasks=/system/app/Tasks.apk

  task lists for you, quite poor. This app demands `ExchangeService` to be. Why?
* com.borqs.twittersync=/system/app/TwitterSyncProvider.apk

  Send your photo to twitter, but no camera soft from borqs already
* com.borqs.weatherwidget=/system/app/Weather_Widget.apk

  Widget is fine with me but it gets weather from an us-based system. I'm in Europe with other meteo facilities nearby
* com.cequint.ecid=/system/app/CityID-release.apk

  Say, in which sity you are. Are you so drunk?
* com.drivemode=/system/app/DriveMode_1_0_2_3.apk

  To stop your phone from calling if you drive. And even if you are not, but just in a train
* com.google.android.apps.books=/system/app/BooksTablet.apk

  Books, in Terrain case on a screen less then your bankcard
* com.google.android.apps.plus=/system/app/PlusOne.apk

  G+, not for me
* com.google.android.apps.uploader=/system/app/MediaUploader.apk

  To upload your media to google drive, not for me
* com.google.android.backup=/system/app/GoogleBackupTransport.apk

  It is about *data* backup, not *settings* or contacts backup.
* com.google.android.feedback=/system/app/GoogleFeedback.apk

  It is to say, how crappy is google for you
* com.google.android.gm=/system/app/Gmail.apk

  Not for me
* com.google.android.googlequicksearchbox=/system/app/GoogleQuickSearchBox.apk

  Serach widget on your screen
* com.google.android.marvin.talkback=/system/app/talkback.apk

  If you are alone and want someone speak to you, phone in this case
* com.google.android.music=/system/app/Music2.apk

  Play music, there is VLC
* com.google.android.partnersetup=/system/app/GooglePartnerSetup.apk

  Advets for google partners
* com.google.android.syncadapters.bookmarks=/system/app/ChromeBookmarksSyncAdapter.apk

  Sybchronize chrom bookmarks, but I do not use chrome
* com.google.android.syncadapters.calendar=/system/app/GoogleCalendarSyncAdapter.apk

  synchronize your calendar with google, but I do not use google so much
* com.google.android.tts=/system/app/GoogleTTS.apk

  text-to-speach, if you cannot read. But then anyway, Terrain's screen size is not for you
* com.google.android.videos=/system/app/Videos.apk

  Video player, there is VLC
* com.google.android.voicesearch=/system/app/VoiceSearch.apk

  Search with voice. I'm not crazy to talk to my phone
* com.google.android.youtube=/system/app/YouTube.apk

  Youtube, firefox plays youtube, so why
* com.matchboxmobile.wisp=/system/app/WISPr_58_Android22_postpaid.apk

  Some adverts for us-based service providers, I'm in Europe
* com.moxier.eas=/system/app/Exchange_mx.apk

  Exchange server interaction. Stock `Tasks` do not start without it
* com.mtag.att.codescanner=/system/app/ATT_code_scanner_vpl_1.2_aligned.apk

  att codescanner, maybe it works in us better, but here in Europe not at all
* com.qo.android.sp.oem=/system/app/Quickoffice_Casio_SP_5.0.114_EC.apk

  Quick office discontinued, there are alternatives
* com.synchronoss.dcs.att.r2g=/system/app/ATT_Ready2Go.apk

  This is to help you screw up your phone
* com.telenav.app.android.cingular=/system/app/tn74-android-att-7400094.apk

  Some strange app in view of totally free navit
* com.wildtangent.android=/system/app/ATT_AndroidGames.apk

  I do not play, but would I, not these games
* com.yellowpages.android.ypmobile=/system/app/YPmobile-P-V3-8-1_B3539.apk

  yp for us mainly, as I got. Anyway, I can type `yellowpages` in firefox
* org.simalliance.openmobileapi.service=/system/app/SmartcardService.apk

  Some smartcard service, usage **unknown**. Some sources claim it is a part of scurity interaction in the phone.
  I checked: I could change PIN and use PUK with this app disabled, my android password active and works. So what?
* search.borqssearch=/system/app/BorqsSearchApp.apk

  **unknown**, but perhaps used by other borqs stuff, removed w/o issues
  
#### Apps which I **put to replace to improve** the stock, which and why (raw list of packages in `apken3`)

* be.irm.kmi.meteo=/data/app/be.irm.kmi.meteo-1.apk

  Weather - Belgian meteo institute
* com.adobe.reader=/data/app/com.adobe.reader-1.apk

  Adobe reader instead of quick-office pdf
* com.alensw.PicFolder=/data/app/com.alensw.PicFolder-1.apk

  Better gallery
* com.andronicus.ledclock=/data/app/com.andronicus.ledclock-1.apk

  Nice clock, can play alarm to the music strem and make it **LOUD** via external speakers
* com.andropenoffice=/mnt/asec/com.andropenoffice-1/pkg.apk

  openoffice for android instead of quick-office
* com.andrwq.recorder=/mnt/asec/com.andrwq.recorder-1/pkg.apk

  Nice voice recorder
* com.dw.contacts.free=/data/app/com.dw.contacts.free-1.apk

  DW contacts to eliminate data-connection withh the stock one. And it is MUCH better
* com.flavionet.android.camera.pro=/data/app/com.flavionet.android.camera.pro-1.apk

  camera, paid, but just for me
* com.flavionet.android.cinema.pro=/data/app/com.flavionet.android.cinema.pro-1.apk

  video, paid, but just for me
* com.fsck.k9=/data/app/com.fsck.k9-1.apk

  e-mail, does it ALL
* com.jb.gosms=/mnt/asec/com.jb.gosms-1/pkg.apk

  ALL what you can imagine about sms/mms
* com.skype.raider=/mnt/asec/com.skype.raider-1/pkg.apk

  skype
* com.socialnmobile.dictapps.notepad.color.note=/mnt/asec/com.socialnmobile.dictapps.notepad.color.note-1/pkg.apk

  very nice note-taker
* com.whatsapp=/data/app/com.whatsapp-1.apk

  watsapp
* jackpal.androidterm=/mnt/asec/jackpal.androidterm-1/pkg.apk

  terminal emulator - the must for me with android
* joa.zipper.editor=/data/app/joa.zipper.editor-1.apk

  nice text editor, a la gedit
* jp.co.johospace.jorte=/data/app/jp.co.johospace.jorte-1.apk

  extremely nice calendar+tasks organizer
* org.joa.zipperplus7v2=/mnt/asec/org.joa.zipperplus7v2-1/pkg.apk

  extreme file manager, including everything
* org.mozilla.firefox=/mnt/asec/org.mozilla.firefox-1/pkg.apk

  firefox
* org.navitproject.navit=/mnt/asec/org.navitproject.navit-1/pkg.apk

  navit - offline navigator with absolutely free and extreme quality daily updated maps
* org.videolan.vlc=/mnt/asec/org.videolan.vlc-1/pkg.apk

  vlc - plays everything what can sound or be viewed
* uk.co.nickfines.RealCalc=/mnt/asec/uk.co.nickfines.RealCalc-1/pkg.apk

  Nice and quite scientific calculator

Perhaps, to be continued ...