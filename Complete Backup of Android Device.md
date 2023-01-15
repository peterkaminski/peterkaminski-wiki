# Complete Backup of Android Device

_Last edited: 2023-01-15_

## Overview

Goal: copy all files from an Android device to a Mac computer. This might used while decommissioning a phone before you resell or discard it.

I ended up using `adb`. Other methods include [Android File Transfer](https://www.android.com/filetransfer/) and [OpenMTP](https://openmtp.ganeshrvel.com/), but both of those failed to copy all the files.

The following was done with Android 13 (Pixel 6a) and macOS Monterey version 12.6.2 (MacBook Pro M1).

## Method

Install `adb` using [[Homebrew]]:

```shell
brew install --cask android-platform-tools
```

`adb` can be installed in other ways, this was the easiest for me.

On the smartphone, enable USB debugging by going to About in settings, and touching the build number until Developer mode is enabled.

On Mac:

```shell
adb shell
tar -chzf /data/local/tmp/sdcard_backup.tar.gz sdcard
exit
adb pull /data/local/tmp/sdcard_backup.tgz .
tar zxvf sdcard_backup.tgz
```

Notes:

- `/data/local/tmp/` is a writable directory (my phone was not rooted)
- Obviously, this would require enough storage to create the tgz.
- `tar` was used instead of a direct `adb pull /sdcard .` because the raw pull command stopped as soon as it hit a file that didn't have read permissions for the user. `tar` skips those with an error message instead of stopping.

## References

- [Writable location on Android](https://stackoverflow.com/a/24824482)
- [How to get full backup of sdcard?](https://forum.xda-developers.com/t/how-to-get-full-backup-of-sdcard.4339419/#post-85694191)
- [Homebrew - android-platform-tools](https://formulae.brew.sh/cask/android-platform-tools)
- [ADB File Transfer: The best way to manage your files](https://www.pixelspot.net/2017/07/03/adb-file-transfer-best-way-manage-files/)
