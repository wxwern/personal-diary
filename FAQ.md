# Frequently Asked Questions (FAQ)

This document lists Frequently Asked Questions about Personal Diary.

Note that the details here are only applicable for the latest versions of Personal Diary, so do ensure you've updated to the latest version of the app.

---

## Usage

### How do I set, change or remove my passcode/password?

- Go to Personal Diary and click on the Settings icon. Locate "Biometrics and Passcode" and select "Set/Change App Passcode..." and tap on that.

  If you intend to remove a passcode, simply press 'Set None' at the top right when you're prompted with 'Enter a New Passcode'.

### How do I sync my diary data between all my Apple devices?

- Simply make sure all your devices are signed in to the same Apple ID and have iCloud Drive turned on, and you're good to go!

  You can check your Apple ID info by going to the Settings app or System Preferences and locating your name, then tap on it.

  You can also verify that iCloud Drive is actively used for Personal Diary by going into Personal Diary \> Settings \> "Storage Location and Usage" and making sure you're using iCloud Drive.

  If you're having problems, check the issues section below.

### How do I change the mood, date and weather for a selected entry?

- Tap on the mood, date and weather text near the top of the screen while viewing an entry.

### How do I disable auto mood detection and auto weather selection?

- You may find the relevant settings at Personal Diary \> Settings \> Automation and AI. The options only prevent the automatic selection of mood and weather, but does not remove them.

  If you are instead looking for disabling the mood and weather options, see the below question.

### How do I disable or hide the mood and weather options entirely?

- Go to Personal Diary \> Settings \> New Entry Defaults \> and turn off "Mood and Weather".

  This will configure all new diary entries to have _no_ mood and weather information. You can still override this on a per-entry basis, and old entries will not be modified by this change.

## Issues

### I am experiencing a weird glitch within the app, or the app isn't responding or lagging. What should I do?

- Try the following troubleshooting steps ([iOS, iPadOS](https://support.apple.com/en-us/HT201398), [watchOS](https://support.apple.com/en-us/HT204510), [macOS](https://support.apple.com/en-us/HT201276)). In many cases, this should resolve the issue.

  You should also check if there is any available updates on the App Store, and if so update the app to the latest release.

  Finally, do report the issue via Personal Diary \> Settings \> App Support, or Recovery Mode (if you are prompted), so as it can be resolved.

### I forgot my passcode/password. Is there a way to reset it?

- If you forgot your passcode, you may go to Recovery Mode (under app settings, or at the passcode page when locked) and try a reset.

  When performing a passcode reset, the app will run some checks to verify your identity based on historical activity and/or biometric and system authentication, and if it fails to do so, it will not allow you to proceed.

  _Note that the passcode reset tool does not guarantee a successful passcode reset, so do remember your passcode well or your data may be permanently inaccessible._

### I've successfully performed a passcode reset but I am still prompted with a passcode. What do I do or type?

- You should be notified that your passcode has been reset to the default, which is either `0000` or `1234` depending on the version you're using. Try those codes and they should take you right in.

  You may change that afterwards via the "Set or Change App Passcode..." option in Personal Diary settings.

### My data is not syncing between my Apple devices even though my settings are correct. How do I resolve that?

- Please try restarting your device.
  - On iOS, [click here to check how to restart depending on your device](https://support.apple.com/kb/HT201559).
  - On iPadOS, [click here to check how to restart depending on your device](https://support.apple.com/kb/HT210631).
  - On watchOS, [you need to press and hold the side button, then press or slide the power off button](https://support.apple.com/en-us/HT204510).
  - On macOS, [click the Apple logo located at the top left of the Menu Bar, and then click Restart](https://support.apple.com/guide/mac-help/shut-down-or-restart-your-mac-mchlp2522/mac).

  Next, make sure you're connected to the Internet (ideally a Wi-Fi connection), and ensure you have turned off Low Power Mode and Low Data Mode.

  Ensure that you have enough iCloud storage and local device storage on all your devices.

  Finally, open the app on all your devices. To force an update, you can perform a pull down to refresh in the Timeline, or press the refresh button on a Mac.

### My diary data has disappeared completely and/or I see "iCloud Access Denied". What should I do to restore my data?

- As described by the error, this is usually because your data is in iCloud but the app cannot access it. Your data shouldn't be missing.

  First, try restarting your device. Sometimes, it's a glitch with the system and it denies the app access to your account.
  - On iOS, [click here to check how to restart depending on your device](https://support.apple.com/kb/HT201559).
  - On iPadOS, [click here to check how to restart depending on your device](https://support.apple.com/kb/HT210631).
  - On macOS, [click the Apple logo located at the top left of the Menu Bar, and then click Restart](https://support.apple.com/guide/mac-help/shut-down-or-restart-your-mac-mchlp2522/mac).

  Next, make sure the following switches are turned on:
  - Settings app/System Preferences \> \[Your Name\] \> iCloud \> iCloud Drive
  - Settings app/System Preferences \> \[Your Name\] \> iCloud \> Personal Diary (under Apps Using iCloud)
  - Personal Diary app \> Settings \> iCloud Drive.

  If you're connected to an Internet connection (ideally on Wi-Fi, and have Low Data Mode and Low Power Mode off), your data should automatically download from iCloud Drive in a moment.

### My diary data, specifically date information, appears to be corrupted. Can this be resolved?

- This tends to be an issue when restoring from an iOS/iPadOS/iCloud backup, migrating to a different device or upgrading iOS/iPadOS, as the OS tampers with the date information the app uses.

  If you have been using Personal Diary version 2.5 or later frequently and have been updating to the latest releases, simply waiting for a moment for your diary data to download will automatically resolve the issue. You can force this to occur by performing a "pull down to refresh". This is because the date information displayed may not be the actual data stored by the app.

### My issue isn't listed!

- Check and search the [Issues](https://github.com/wxwern/personal-diary/issues?q=is%3Aissue+sort%3Aupdated-desc) page to see if anyone else has had the same issue, and if it has been resolved.
- Otherwise, report a new issue there or via the App Support section in Personal Diary Settings.

## Contact

Still can't figure something out? Contact us via Personal Diary \> Settings \> App Support.
