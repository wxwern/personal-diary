# Personal Diary Changelog
Version history for all stable releases (and the most recent beta) of Personal Diary.

## Version 3.0.10

- Fixed: Hyperlinks and Strikethroughs did not save until other unrelated modifications have been done to trigger autosave.
- Fixed: Importing photos taken directly from the Camera within the app did not do anything.
- Fixed: Some users may have had troubles installing the app on the Apple Watch.
- Fixed: Images may be stuck "loading" - they are caused by previously deleted images of which the app still thinks exists and is trying to load.
- Fixed: Dragging and dropping images to export images out of the app, or copy images to multiple entries, may cause the app to incorrectly use low resolution thumbnails of the image.
- Fixed: Images may flicker upon selection of an entry, upon autosave, or upon scrolling through lists or pages with images.
- Fixed: Smart Search did not correctly account for search terms consisting of the day of the week (so searching for "Saturday" did not work).
- Improved: Added more hints of Safe Mode and direct shortcuts to exit it.
- Improved: Disabling image previews will now show a placeholder image instead of a blank space.

## Version 3.0.9

- Fixed: Storage Location preference settings may not update correctly after a background iCloud login update. This may have caused unexpected confusion as to why storage locations randomly switched.
- Fixed: Journal Picker headers may not appear correctly on macOS.
- Improved: Information about storage location differences of a journal are now clearer. The app also now prompts to automatically change settings for you if you want to access journals in a different location without migrating.
- Improved: There are now double-confirmations for journal storage location migrations to prevent accidental migrations.

## Version 3.0.8

- Fixed: On recent versions of iOS, iPadOS and macOS and Personal Diary, there is a chance where you would frequently get scary iCloud access denied errors. This is because the system temporarily removed access to iCloud for whatever reason. It has now changed to a "waiting for iCloud access" indicator, which automatically dismisses once iCloud is ready.
- Fixed: Some miscellaneous crashes that do not appear to have any reason should be resolved.
- Fixed: Depending on luck, you may occasionally find a warning of an "unavailable" entry, which does not acutally exist.
- Improved: Entries which have data load issues are now ordered beyond the latest entries in the list.
- Improved: When you are in the Timeline and you have written data in iCloud in the past, but no data is downloaded (making the Timeline appear blank), and system configuration permits, the app will more aggressively poll for iCloud updates and refresh the Timeline in order to retrieve your data.

## Version 3.0.7

- Fixed: On recent versions of iOS 16, iPadOS 16 and macOS 13 (Ventura), the app may incorrectly assume all your diary data is downloaded from iCloud, and attempt to load them before the download is complete, causing extremely slow loading times in the Timeline.
- Fixed: Some links in the app (like FAQ) were moved, and are thus updated.
- Improved: The Data Availability section in Storage Location & Usage now shows an estimated percentage of data downloaded locally.
- Misc: Removed legacy code and updated dependencies.

## Version 3.0.6

- Fixed: Page Curl Animations added tap-to-flip-page tap targets that conflict with button taps on images and text, making it impossible to edit text or add a new image in some situations. This is now removed.
- Fixed: Strikethrough option was missing in recent versions of the app.
- Fixed: Strikethrough and Hyperlink keyboard shortcuts were missing in recent versions of the app.
- Fixed: PDF and Printing Export Cover Page might not be removed even if you turn it off.
- Improved: For PDF and Printing exports, they might crash when merging large numbers of pages due to running out of memory. This is mitigated through transferring partial exported contents onto storage and improved memory management.
- Improved: For PDF and Printing exports, you can now specify the starting page number, so you may merge PDF parts from the past outside of the app and do not need to reexport everything to get the page numbers right.

## Version 3.0.5

- Fixed: Mood and Weather cannot be removed if already set.
- Fixed: Biometrics Unlock may be displayed even when it is not supported or enabled on your device.
- Fixed: In some cases you might be able to "import" inline images into the text editor. Though it looks like it worked, the action isn't supported and it is not saved. The text editor will now correctly reflect this and not show inline images.
- Improved: Closing the Journal Picker (available when Multi-Journal Mode is on) will now lock the app as well (if a passcode is set).
- Improved: Entry data now internally tracks a version number, so future version incompatibilities can be marked with an appropriate warning.
- Attempted to Fix: Personal Diary might crash on older versions of macOS.

## Version 3.0.4

- Fixed: Notifications stop working after 14 days in the newer versions, claiming that you have never opened the app even if you did.
- Fixed: 'Something went wrong' alerts may appear on app launch even when nothing is wrong.

## Version 3.0.3

- Fixed: Searching with multiple words may not work in certain languages.
- Fixed: Search terms with only the month and year now correctly shows results (again).
- Fixed: Delete button was missing in the image attachment panel.
- Fixed: Image thumbnails may appear in the wrong orientation in previews on iOS 14 and below.
- Fixed: A transition animation may unexpectedly occur which "transitions" to the same entry.
- Improved: Added a section to perform basic customizations for VoiceOver prompts.
- Improved: Date Format options for the Timeline view has been rephrased for clarity.

## Version 3.0.2

- Fixed: Search terms with only the month and year now correctly shows results.
- Fixed: Searching contents were incorrectly case sensitive. That is fixed and are now no longer case sensitive.
- Fixed: Tags now show up correctly in PDF exports.
- Fixed: Editing an entry while entries are refreshing may cause edits to be undone and reverted.
- Fixed: A rare crash that may occur when the number of entries loaded changes while the UI is being updated.
- Fixed: When mood and weather are turned off for new entries, auto mood detection should not have kicked in automatically.
- Fixed: Raw Data Archive now outputs folder names with the corresponding timezone the entry is written in.
- Improved: The timezone indicators for entries with timezones different than your current one can now either be hidden or ignored.
- Improved: Clarified in-app explanation for legacy iOS version warnings.

Note: The search engine in version 3+ now searches text by considering only individual words in whatever language you're in. If you want to search an exact phrase with arbitrary words and symbols, surround the phrase with double quotes (").

## Version 3.0.1

- Fixed: Toggling the Multi-Journal Mode switch may crash the app.
- Fixed: The app may crash when creating a new entry.
- Fixed: Some other miscellaneous crashes that may occur.
- Improved: Images in PDFs should be less likely to fail to export.


## Version 3.0

Personal Diary has been massively revamped behind the scenes and is now on version 3! Enjoy vastly improved app launch times, lots of new features and compatibility with all new operating systems and devices released so far.


Background Entry Data Loading
- You can now use the app, browse, edit and create diary entries, even while the app is still in the middle of loading your existing data in the background. No more long loading times at the launch screen!
- Note: Some actions, like searching through all your data, are unavailable until all entries are loaded.

Multi-Journal mode
- You can now create multiple journals to organise your info, such as separate ones for Personal and Work entries.
- You can choose a preferred journal for your own reference, for which the app may auto-open if no other journals are open.

Large Screen and App Window Optimizations
- On larger landscape displays and window sizes, the timeline and entry can now be shown in split view, making better use of available screen space.
- A maximum width may now be set for the entry page, so it doesn't span the entire width of a display (which would become ridiculous in cases like an ultrawide display).
- Full compatibility with the all new Stage Manager on iPadOS and macOS.

UI Revamps
- An updated Timeline design now allows for dynamically sized table rows and entry image previews.
- Timeline and Entry contents can now be displayed in split view.
- Settings page organisation and VoiceOver accessibility has been improved.
- Image attachment panel design has been updated with a simpler floating design, new context menus and improved VoiceOver accessibility.
- Apple Watch app UI conventions have been updated with some design cues used in watchOS 7+.

Calendar View in Timeline (coming soon)
- Quickly look through a calendar for at-a-glance info of your entries!
- Calendar view has separate view modes, like week view and month view.
- Jump to any day quickly with just a few selections.

Miscellaneous
- New sorting order options now has the ability to sort in chronological or reverse chronological order, jump to current entry, and more!
- Apple Watch app now uses the watchOS full system on-screen keyboard on Series 7 and newer instead of FlickType. Older devices still default to FlickType. (If you still want to use FlickType on Series 7+, it can still be accessed with a tap-and-hold in the editing panel)
- Entry tags are now supported, which allows for faster and more precise search results.
- Timezone information are now tracked in entries and displayed if there's a mismatch with your current timezone.
- You can now import multiple images by once on iOS 14, iPadOS 14 and macOS 11 and later through the photo and file pickers.
- Image attachment viewer now supports Live Text and Copy Subject provided by the system when on a compatible device running iOS 16 and iPadOS 16.
- Themes have been revamped to allow for more customization. No longer are you forced to pick vibrant colors in the app, you can also choose pastel and minimal ones!
- An updated machine learning model for Auto Mood Detection is now included and used on iOS 14, iPadOS 14, macOS 11 and above, which should yield improved precision and accuracy.
- The search engine has an updated algorithm that now works better with most languages, even if the app isn't translated to them.
- New option for page curl animations to emulate a physical book.
- New shortcuts are now available directly in the Timeline.
- Improved syncing with other devices reduces the chance of conflicts and data overwrites from multiple devices at once.
- Data migration to and from iCloud Drive will no longer automatically happen and must be manually initiated. This prevents unintended automatic data migrations.
- Resolved lag issues when displaying large amounts of data in the Timeline.

Thank you everyone for using and supporting Personal Diary to this day!



App Support and Compatibility Notice

This release drops compatibility for iOS 9 and iOS 10 (Apple dropped support for them - it is no longer possible to support them while including support for iOS 16 features).

Furthermore, while this app can still be downloaded and used on devices iOS 11 and up, it will now officially only be designed for iOS 13, iPadOS 13, macOS 10.15 and up, and work best for iOS 14, iPadOS 14, macOS 11 and up. Notable incompatibilities include:

- Updated Auto Mood Detection model is not available on iOS 13, iPadOS 13, macOS 10.15 and below.
- Modern context menu design is partially unavailable on some places in iOS 13, iPadOS 13 and macOS 10.15.
- Modern context menus are not available on iOS 12 and below.
- Dark theme is no longer available on iOS 12 and below.
- Modern button icon designs are unavailable on iOS 12 and below.
- Modern UI transitions and popup overlay styles are unavailable on iOS 12 and below.
- 3D Touch support is no longer available on iOS 12 and below.
- Some keyboard shortcuts are no longer available on iOS 12 and below.
- Reordering of images via drag and drop is not available on iOS 10 and below.
- FlickType on the Apple Watch app is no longer supported on watchOS 6.

## Version 2.6.6
This is likely to be the last bug fix update before version 3.0, which will involve a rewrite of the full codebase to make it easier to include new functionality as many of you have requested.

Right now, this build provides the following changes:
- Updated to work with the latest iPhone, iPad and MacBooks.
- Minor UI behaviour patches in an entry.
- Improved diary reminder notification handling.

## Version 2.6.5
- Fixes an issue where content auto-scrolls back to the cursor while editing in an entry on macOS (again).
- Resolves an issue where if Dark Theme is set to Auto, it may not work correctly on macOS, where it randomly switches to Dark Mode even in undesired situations.
- Updated minimum window size on macOS.
- Fixed settings window size being unnecessarily tiny on macOS.
- Fixed a bug where long footer text is truncated in the settings window and submenus, causing one to be unable to read the text in its entirely.
- Improved password recovery identity verification process, with many bug fixes and accuracy improvements.
- Stopped unnecessary background updates for dark mode, so the app should now not waste as much power doing nothing.

## Version 2.6.3
- Fixes an issue where content auto-scrolls back to the cursor while editing in an entry on macOS.
- Resolves an issue where the passcode screen may be prompted twice.
- Passcode input when using VoiceOver now follows VoiceOver settings and input methods set up.
- Entry configuration page has improved VoiceOver navigation.
- The app now blurs the screen in addition to locking itself when navigating away from the app (if a passcode is set) on iOS/iPadOS.
- Multi-journal support (experimental) improvements - now in a fully usable state with hierarchal navigation, plus proper VoiceOver compatibility.

Note: On macOS, the app's settings page window in this release may glitch out and be quite small, which was why this macOS release is delayed compared to iOS/iPadOS/watchOS. This version is released anyway to resolve more severe usability problems, and the settings page will be resolved in a future update.

## Version 2.6.2
- Added support for iOS 14.2, iPadOS 14.2, and macOS Big Sur.
- Personal Diary is now a Universal Mac app, supporting Macs with Apple Silicon natively.
- Resolved an issue where passcode screen may not block the entire app.
- Patches a bug where the search bar is invisible in dark mode on macOS.
- Re-added the button to export images which went missing in the last update.
- Fixes a bug where exporting might miss out on the latest entry.
- Fixes an issue where printing cannot be done on the Mac app.
- Fixes an issue where the search bar does not take in spaces when typing with a physical keyboard.
- Significantly improved responsiveness and performance of the Timeline for large diaries with more than half a thousand entries.
- Fixes an issue where resizing the window while in the Timeline pane on macOS may cause the app to freeze for a few seconds.
- Reduced some AI functionality temporarily as it was discovered to be causing too much of a hit in performance.
- Improved app performance on macOS Big Sur.
- Reduced data export size limits.

## Version 2.6.1
- Fixed an issue where scrolling may not work while editing an Entry.
- Patched a bug where pasting content might cause erroneous auto-scrolling.
- Added an edit button in the Entry page that provides hints on how you can edit all aspects of an entry.
- Added an indicator on macOS to press 'esc' to finish typing when Focused Editing Mode is enabled in Personal Diary settings.

## Version 2.6
- Personal Diary is now available on macOS 10.15 and later.
- Optimized for iOS 14, iPadOS 14 and watchOS 7.
- Fixed an issue on iOS and iPadOS 14 where your data on iCloud does not automatically download.
- Resolved a bug on iOS and iPadOS 14 where images are stubborn and can never be downloaded, no matter what you do.
- Updated UI for mood, weather and date selector for an entry on iPad and macOS.
- Added image reordering support, so you can now reorder images within an entry with a simple drag.
- Image reordering works only on iOS 11 and later at the moment.
- If you're using the add button to insert images, they are now correctly added in the order they were added in.
- Updated Settings UI on iOS 13, iPadOS 13, macOS 10.15 and later, so it now appears as a pop up window rather than a full screen page.
- Fixed an issue where the app may freeze for a second or two on large journals every single time you enter the Timeline, especially on older iOS, iPadOS and macOS devices.
- Added experimental multi-journal switching support, allowing you to switch between different books or profiles. To try it out, enable it in Experimental Features.
- Added drag and drop support - on iPadOS and macOS, you can now drag and drop images directly into the Images panel.
- Added the ability to choose export date range for bulk exports.
- PDF Exports (in bulk) can now be customized.
- Added an option to disable grouping by month for PDF exports and Printing, which may cause exports to halt completely for large diaries on older devices.
- Added the option to insert images and export via the Files app on iOS/iPadOS and Finder on macOS.
- Fixed an issue where importing data does not work on macOS.
- Resolves an issue where selecteing the "Export or Print Data" option in Personal Diary settings will crash the app when low on storage.
- Navigation bar colors are now more consistent throughout the app.
- Fixed a bug where the app continuously refreshes the view waiting for theme changes and wasting resources.
- Updated watchOS FlickType SDK. Now, you can type your entries on your watch more efficiently than ever - with swipe-typing, custom character input and more, all from your wrist!
- Personal Diary for watchOS now works with the FlickType watch app on watchOS 7, so FlickType can now update separately from Personal Diary app, and custom FlickType settings automatically work.
- Fixed some issues with prompts provided by Recovery Mode.
- Updated App Support & Information page.
- Updated some troubleshooting prompts.

## Version 2.5.11
- Updated with support for the latest iOS, iPadOS, and watchOS versions.
- The app is now available in beta on macOS 10.15 or later.
- Added mouse and trackpad support, suited for iPadOS and macOS.
- Increased default font sizes and switched displayed font to Arial.
- Fixed an issue where formatted text on PDF exports have a 62.5% chance of being missing or corrupted.
- Resolved a bug where an image in a PDF export may be split into two on two different pages.
- Resolves issues with PDF exports where pages are not split up properly.
- Patched a bug where images could be duplicated and injected in PDF exports if a certain string of characters are present in their entry text.
- Fixed a problem where PDF exports may fail for large diaries due to running out of memory, causing the app to crash, freeze, or have missing images. Caveat: PDF exports will now be slower as they are now done in chunks and rendered in storage instead.
- Fixed an issue where nothing happens when editing a hyperlink.
- Fixed some bugs and glitches that may occur when operating with keyboard shortcuts.
- Resolved crashes and UI glitches that occur when you perform actions too quickly while a search result is active.
- Fixed a crash when you press the 'x' button to clear search phrase, then immediately press the add entry button.
- Resolved UI formatting inconsistencies when searching in the Timeline.
- Full Screen Editing has been renamed to Focused Editing Mode.
- Fixed a bug where the Focused Editing Mode (Full Screen Editing) toggle resets after an app relaunch.
- Resolved some problems where detection of whether content is fully downloaded is not correct when migrating to/from iCloud Drive, and exporting/printing data.
- Resolved an issue where text formatting, specifically text formatted only in italics, may not preserve its style.
- Bulk data export options are revamped. Notably, they now show their progress, so you'll know whether something is happening or not when exporting to ZIP, PDF or printing data.
- Some minor UI updates to settings screens.
- More preparations for multi-journal support.

## Version 2.5.10
- Added acknowledgements within the app.
- Minor bug fixes.

## Version 2.5.9
- Fixed a critical bug where resetting a forgotten passcode, running diagnostics, and other parts of Recovery Mode that just doesn't seem to do anything as a subsequent alert does not pop up.
- Added ability to check purchased tips.

## Version 2.5.8
- Made significant changes behind the scenes to prepare the app for multiple journals and custom attachments (video, audio, files etc) support. Stay tuned!
- Updated App Store screenshots.

## Version 2.5.7
- Fixes a bug where the Plain White theme renders text and buttons in white, making them look invisible on a white background.
- Resolves an inconvenience where overriding light or dark themes won't necessarily update throughout the app until the app is completely restarted.
- Improved the phrasing of the entry deletion alert to warn about the fact that deletion will sync across devices.
- Removed some animations as they have a small chance to glitch out and cause entries in the Timeline to "fly away".
- Some internal code changes to improve future compatibility.

## Version 2.5.6
- Fixed an issue where 'Title' labels interfere with the search bar on older iOS versions.
- Fixed a bug where iPad users using iOS 13.2 or later would have issues exporting data as the app would freeze a little and not show the share sheet.
- Performed minor updates to the 'Welcome Back' heading.
- Minor phrasing changes to the error prompt that appears after the crash.

## Version 2.5.5

- A prompt now confirms that diary data is ready for export, before showing the Share Sheet to select where to save your file.
- Hopefully the bug where some users aren't able to select a location to save their exported file is resolved.
- Fixes watchOS app UI glitch where the Show More or Load More button is visible and sometimes interactive while data is supposed to be loading.
- Slightly refreshed the Dark Theme in the Timeline view.
- Fixes a bug where the Images heading does not update its counter after adding a new image.

## Version 2.5.3

- Added the ability to check for app updates from within Recovery Mode.
- Improved phrasing and handling of the error prompt after crashing.

## Version 2.5.2

- Rebuilt the app with Xcode 11.2.1. This fixes a critical issue where users using iOS versions older than iOS 13.2 are not able to use the app normally, as the app crashes when you try to add an entry, among other areas.
- Fixed an issue where unlocking with biometrics is always possible regardless of switch position.

## Version 2.5.1

- Re-added the latest FlickType SDK in the watch app. Type away with the new version of the award-winning keyboard, right from your wrist!
- Added the ability to trigger biometric authentication (Touch ID or Face ID) from the password view directly if the automatic authentication fails.
- Improved data sync mechanism in the watch app, so now you can view your entries and create new ones while the synchronisation is taking place.
- The passcode will now be confirmed twice when setting a passcode for the first time.
- Fixes a bug where iPad users cannot import data.
- Fixes autorotate not working while keyboard is visible. Previously, you could only type in landscape mode on your phone if you rotated to landscape before typing.
- Changed the 'error' prompt when you type an incorrect passcode to 'incorrect', so as to avoid confusion.
- Added haptic feedback in minor areas of the app.
- Updated the AI for automatic mood selection.
- Fixed some bugs and glitches on the UI where it shows conflicting information in the watch app.

## Version 2.5
- Added full iOS 13 support.
- Dark Mode now properly reflects system settings if 'Auto' or 'System' is selected. This was not working in prior releases.
- Added compatibility with the latest iPhone & iPad.
- Added import functionality, so you can restore any backups you made in the past as a \*.zip file exported by the app.
- Fixed a date corruption issue if you restore an iOS 13 backup or transferred data to an iOS 13 enabled device, like the new iPhone 11. However, this version of the app needs to run before iOS 13 is installed, otherwise it would be a little too late. Any corrupted data unfortunately cannot be recovered unless you have a backup.
- Fixed some bugs regarding data migration and data export.
- Removed FlickType SDK temporarily as it is not yet compatible with watchOS 6.

## Version 2.4.30

- Fixed an issue regarding changing themes will not update until you restart the app.
- The app should now function properly on iOS 13.
- Added haptic feedback to some areas of the app.
- Updated FlickType SDK to version 2.2, allowing for faster keyboard input than ever before.
- Added 'thinking emoji'.

## Version 2.4.28

- Fixed an issue where in certain conditions if you swipe left or right to load neighbouring entries, the images do not reload.
- Fixed an issue where if text formatting (bold, italics etc) are applied at the start of any entry, the exported content would have messed up styles.
- Hopefully fixing the issue where "apologies for the crash" prompts occur even if a crash never occur. I hope.
- Improved Dark Mode auto switching such that it performs less unnecessary work in the background.
- Cleaned up some of the app's source code.
- Performed some preparations for iOS 13.

## Version 2.4.27

- Added support for the award winning FlickType keyboard on the Personal Diary Apple Watch app. You can now create entries faster than ever before and with ease, all from your Apple Watch! Read more below.
- You can now modify a portion of an entry or continue writing an entry that you’ve made in the past, without replacing the text completely from scratch. (Only supported with the FlickType keyboard)
- Hopefully I fixed the issue where on some devices you may keep encountering the message “Apologies for the crash” even when the app never crashed.
- Slightly increased maximum font size supported.
- Some other small glitches which hopefully you never noticed are fixed.


## Version 2.4.26
- This update contains a quick bug fix which should fix the issue where some users were not able to properly import images from their Photo Library.

## Version 2.4.25

- App icon and some parts of the app’s interface has been updated.
- Fixed an issue with keyboard shortcuts not functioning correctly.
- Importing images should now be (almost) instantaneous.
- Imported images now uses the format of the image imported, so PNG/JPEG settings will be discontinued.
- Fixed a bug where the app crashes if you attempted to refresh diary data while the data is being refreshed.
- Fixes some small bugs when swiping between entries in the Entry view.
- Fixed some other minor internal issues.

## Version 2.4.24

- Fixes an issue with Chinese, Japanese characters etc not being able to be typed normally within the app. Sorry for any inconvenience caused.
- Adds haptic feedback for the bounce back when you attempt to swipe left or right to another entry in the Entry view, but there are no more entries to view in that direction.
- Theme text color in the top bar & status bar text color should now match. Some themes were messed up previously.

## Version 2.4.23

This release adds some features and fixes a few bugs.

- Font formatting now supported. You can now use Bold, Italics, Underline, Strikethrough and Hyperlinks in your entries. Some of these formatting features may have limitations in iOS 11 and older, e.g. the inability to use Bold and Italics at the same time in these older OSes.
- Exporting features are now out of experimental phase. Easily export your entire journal as a PDF file, or with its raw data packaged into a zip file.
- 3D Touch functionality is now supported. Peek and pop in the Timeline, and force press the app icon to quickly create a new entry within the app.
- Added the ability to see local storage utilised by your Diary data. Note that if you’ve selected to store data on iCloud, this only shows the total data occupied by all your diary contents that are downloaded locally
- Fixes an issue with the Apple Watch app where the app will get stuck in the Syncing stage.
- Temporarily removed the ability to sync all data to the watch and currently limited to only 30 entries plus anything created on the watch.
- Fixes some animation glitches within the Entry editing view, so you’ll now feel more satisfied when editing the entries.
- Improved the algorithm behind the Dynamic Text Size feature in the Timeline, which should slightly improve scrolling performance.
- Slightly improved how search results are presented.
- Fixes issues regarding low storage space and added warnings when you’ve low storage space.

## Version 2.4.22

This new release is an attempt to fix the crashes in which 0.1% of users are experiencing all the time for no reason, and a reinstall of the app will fixes the issue for these users. Do inform me if this still hasn’t fixed the issue but going into Safe mode and contacting me.

## Version 2.4.20 ~ 2.4.21

Included a few amazing functionalities in this update. Notably:

- Apple Watch Support! The complete version of Personal Diary including your entire Timeline and every single aspect of an entry can be created and/or modified directly on your watch (okay, maybe not complete because you can’t add or view images yet, but support will be coming soon!). Comes with automatic mood & weather selection as well (which can be overridden directly on your watch), and your settings will be mirrored from the Personal Diary app on your iPhone.

Apple Watch app usage requires “Allow data access on your Apple Watch app” to be enabled on the iPhone app.

- Printing & Export To PDF Support! You can now export an individual entry or all of your Personal Diary data for printing or just for archiving your data.

And other random updates like:

- The new iPad Pros & iOS 12.1 are now supported as well!
- The App Store Screenshots are updated to make them more interesting. ;)
- Notifications now allow you to directly select “Create New Entry” (by 3D touching the notification) and instantly jump into a new entry within the app and start writing.

And some bug fixes:
- Fixed random animation glitches when deleting an entry.
- Removed animations for users on iOS 9 due to an animation glitch that only occurs persistently on iOS 9.
- Fixed bugs regarding the app not detecting a new iCloud sign in properly and therefore would not display iCloud content until an app refresh is performed.

## Version 2.4.19
New features added, while most bugs should be squashed. Hopefully they don’t reproduce.

- Killed a bug where the Timeline just decides not to chronologically sort your entries and jumble up your entries if you’ve modified the dates so that it isn’t referring to ‘now’, until you summon it to reload by pulling down to refresh.
- Squashed a bug causing the app to be stubborn and nag you to write in your diary even if you have already written earlier.
- Annihilated a bug that made the app be lazy and not want to automatically select the latest weather as it can see from the sky, but rather just based on its memory, guesses the weather based on info a few hours to days ago.
- Removed a bug where hiding entry preview literally hides the preview of everything, i.e. it also hides whether or not an entry is downloaded.
- Added the ability to toggle whether to use randomness when notifications are sent.
- Adds more information to clarify when to expect a reply from me after sending an email.
- Adds a Tipping Jar for supporting the development of the app, since some of you are willing to do so. Thank you for supporting Personal Diary :)
- Slightly updated splash screen which now also indicates the version number of the app, and shows detailed loading progress of the app.
- Reordered some of the settings from within the app.
- Added random Easter eggs but I won’t tell you what are they. ;)

## Version 2.4.17 - 2.4.18
- The app is now fully compatible with iOS 12 & the 2018 iPhone models.
- Added Experimental Siri Integration and Siri Shortcuts support.
- Fixes a bug where pressing the ‘+’ button to add an entry while searching causes a crash.
- Fixes an issue where scrolling very quickly causes lots of lag. Performance should now be improved. (Note that entries that are downloading may still hamper app and scrolling performance)
- Fixes a lag that occurs while swiping from the left edge in the editing view to go back to Timeline. It’s so smooth it’ll be so satisfying to swipe to go back to Timeline and watch your entries slide back in.
- Fixed an animation glitch where the image viewer panel in the editing view will initially display two headers titled “Images” as the panel loads.
- Fixes some issues with VoiceOver hints, and added support for AI functionality with VoiceOver.
- Fixes a bug when turning off “Allow Password Reset When Locked” will disallow password resets everywhere.
- Fixes some issues with disabling cloud storage (migrating your data from the cloud to local storage).
- Fixes an issue where notifications linger in the Notification Centre longer than it should be there.
- Fixes an issue where the Time Indicator in the Timeline just goes *poof*, and disappears.
- The fancy animations within the app now obey the “Reduce Motion” setting in iOS.
- The app now uses less power when “Low Power Mode” is enabled in iOS by disabling unnecessary animations, slowing down entry sync and reload, etc.
- More details about FAQs are added directly at the footer of the relevant menu.
- Added Safe Mode which can be enabled to bypass the usual routine of the app if it ever gets stuck in a crash loop.
- Adds randomness to when the notification is triggered by ±30 minutes so that you won’t be bored of it triggering exactly at the time you specified.

## Version 2.4.15 - 2.4.16
- Adds iCloud disabling/sign out notification. The app now notifies you that your data stored on iCloud is inaccessible and how to fix the problem, as some users were confused as to why they cannot find data in the app after disabling iCloud.
- Increases maximum text size setting of the app for easier readability if needed.
- Some small updates to the AI Engine.
- Adds the ability to disable the ability to reset forgotten passwords when locked.
- Fixes an issue where the number 6 button on the password keypad has been replaced with “…” for some users.
- Eliminates all possible manners where the password keypad could possibly be corrupted in future versions.
- Fixes a security issue with the password reset tool.
- Improved verification process of the password reset tool.
- Fixes bugs with some settings not correctly applied.

## Version 2.4.11 - 2.4.12

- Fixes a bug where excessive lag might occur everywhere within the app, either suddenly or immediately after a crash.
- Fixes a bug where pressing the “+” button to add an entry will take forever to load.
- Fixes a bug where performing a migration from iCloud to Local Storage could cause data loss if data is not completely downloaded.
- Includes new animations within the Timeline section.
- Adds support for swiping left or right to quickly flip between entries in the entry view.
- Day of the week (Sunday, Monday, etc.) is now also displayed in the Timeline if selected in Settings > Date Format.
- Adds the ability to clear app cache.
- Fixes a flaw that allows a user to tamper with downloading entries, causing the partially downloaded entries to be corrupted or to lose mood/weather data.
- Fixes an issue where an old version of an entry incorrectly auto-saves, possibly overriding a newer version.
- Fixes animation issues when entries from different years are visible on launch.
- Fixes animation issues when launching the app for users that don’t use a password.
- Relaxes the requirements for a password reset.
- Adds support for additional external keyboard shortcuts.

## Version 2.4.7 - 2.4.10

These updates adds:
- Daily Diary Notifications

These updates fixes:
- a bug causing the app to crash for some users when entering into the Timeline section.
- an issue where turning on Face ID will cause the app to crash when relaunched
- an issue where passcodes are not properly saved.
- a bug causing some users to fail to login to the app after enabling diary notifications.

## Version 2.4.6
New Features (originally teased in the main release version 2.4):
- Auto Mood Selection
  - Selects the mood automatically based on what you wrote. The mood selection AI will improve overtime as more updates come along.
- Auto Weather Selection
  - Selects the weather automatically based on your current location (using GPS, or else via IP address tracking).
- Daily Feedback
  - Shows you a personal response (by an AI) after writing an entry. Requires auto mood selection as the AI is mainly influenced by the mood.

Feature Improvements:
- Reasons for a download error will now show up.
- Less aggressive rejection by the passcode recovery tool.
- VoiceOver hints improved.

Performance Improvements: (noticeable if you have lots of entries)
- Faster App Launch Times
- Faster Timeline loading times after first launch of the app.
- Eliminated the lag when entering the Timeline section.
- Reduced lag when multiple entries are downloading.

Bug fixes:
- Error messages will now not constantly pop up over what you are doing now which caused the inability to use the app in previous versions.

Additions:
- Passcode protection will now persist even after deletion of the app. Note that other than the recovery tool, there will be no other way to enter the app except with your passcode starting from this version of the app.
- Since you all tend to report issues I can’t find, I’ve included the ability to send internal diagnostic information to me in order to diagnose the problem better.

## Version 2.4.1 ~ 2.4.5

This minor update:
- fixes an issue which prevents you to scroll to another area while keyboard is displayed.
- fixes an issue which causes the text cursor to jump to the end when editing an entry and not to start at where you have tapped.
- fixes user interface which does not reference Touch ID & Face ID properly.
- improved user interface when in the locked state.
- slightly improved the responsiveness of the app.
- v2.4.2 fixes an issue caused by v2.4.1 to not allow users to turn on or turn off Touch ID/Face ID.
- v2.4.3 fixes an issue caused by v2.4.2 where the “2” is replaced with “z…e” in the password field, which causes multiple users not being able to enter the app.

## Version 2.4

This update contains:
- faster performance,
- bug fixes,
- slight UI changes,
- improvements to entries created in the same day,
- new messages pop up,
- under the hood improvements,
- compatibility with new iPhone models such as the iPhone X.

## Version 2.3

- New Dark Mode!
(Dark Mode auto-enables in extreme low-light)
- Better interface redesign!
- Now with 25 different moods!
- Now with 10 different weather options!
- Added no mood & weather option.
- Improved Smart Search.
- #hashtags, “quotes” now supported!
- New Recovery Mode.
- Password Recovery.
- Data Loss Diagnostics tool.
- “Distress” email to developer.
- Adjustments to entry preview to show more data.
- Added the ability to turn off iCloud.
- Additional themes included.
- Improved VoiceOver compatibility.
- Minor bug fixes.

Some features requires iOS 9 and later to function properly.

## Version 2.2

What’s New In This Version:

iCloud Sync:
- View & edit your entries from all your devices!
- No difference in app performance
- Pull to refresh entries in iCloud
- Entries stored in the cloud=Data Safe

Smart Search:
- Easily search keywords, dates, mood & more!

Numeric Passcode:
- 0/4/6/x-digit passcode can now be set.
- Press ‘Done’ to enter password and access entries; instead of auto complete after typing 4 digits. This is for higher security.

Images Auto-Popup:
- Auto-pops-up images if there’re attached.

Minor bug fixes
- [FIXED] Settings Not Saving Properly
- [FIXED] Occasional crashes

Keyboard shortcuts now supported
VoiceOver improvements & fixes

## Version 2.1

- Icon redesigned
- Fixed a bug where entries would disappear.
- Password is renamed as passcode.
- You can now search entries.
- Added the ability to change font size.
- Added the ability to change date format displayed.
- App performance improvements.
- App launches faster than ever.
- Added some weather icons.
- Date now reflects to your current region format.

## Version 2.0

- More moods to choose from
- You can now import photos into your entries
- Ability to select a theme
- New full screen editing mode (Optional)
- Improved auto-saving
- Various bug fixes
- Slight design modifications

## Version 1.0

- First Release
