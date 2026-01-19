# Getting started

## Installation

For **macOS**, download the `bubbletrail-macos-(version).zip` file from the
[latest GitHub release][gh]. Unpack it if that didn't happen automatically
  after download, and drag the resulting `Bubbletrail.app` to your
`/Applications` directory.

For **iOS**, download the app from the [App Store][as].

## Import of existing logs

Bubbletrail cam import dive logs in several common formats. Imports are
easiest to do in the desktop version of Bubbletrail as it allows selecting
files from the computer filesystem, but are also possible in the mobile
version if you get the file to your mobile device via a link or email.

In desktop Bubbletrail, select `Settings` in the navigation bar and then
`Import log file`. Choose a log file in one of the supported formats (see
below). The dives in the log will be added to those already in Bubbletrail,
with some logic for deduplication.

### From MacDive

Bubbletrail understands MacDive's own/native XML format. In MacDive, select
your dives and then choose `Export` and `Selected as XML` in the menu.

### From Subsurface

Bubbletrail understands Subsurface's own/native XML format. In Subsurface,
choose `File` and `Export` in the menu. In the dialog, select `Subsurface
XML` as the export format and `All dives` or a selection of dives as you
prefer.

### From other programs

Bubbletrail also supports UDDF log files which can be exported from many
programs. Alternatively, Subsurface is very capable and supports many import
formats. You can use Subsurface as a middle-man for many formats not
supported directly by Bubbletrail.

## Import from dive computer

Bubbletrail supports dive computers that communicate over Bluetooth LE. This
is many or most modern dive computers, but not all of them. To download
dives, select `Connect` in Bubbletrail. Make sure your dive computer is on
and in Bluetooth pairing mode, then press `Scan` in Bubbletrail. It should
show up in the list, after which you can tap `Connect` and then `Download`.
The first time you sync with a new computer may take longer, as Bubbletrail
doesn't get know which dives are already downloaded. Bubbletrail will avoid
downloading dives that are older than those already in your archive.

!!! info

    Bubbletrail supports synchronising the clock of many dive computers and
    will do so automatically when downloading dives.

## Syncing between devices

You can sync your dive log between several different devices, mobile and
desktop. Bubbletrail supports syncing via any standard cloud storage
provider (AWS S3 protocol), and we also provide a free cloud storage
instance for anyone to use.

!!! info

    Your data is encrypted with a password of your choice when syncing
    so the storage provider cannot access any details of
    your dives. See [Syncing](syncing.md) for details.

To get a sync account, enter your email address on the [Bubbletrail sync
subscription page][sync]. You'll get an email with the necessary credentials
which you then enter into Bubbletrail on the sync settings pages.
Bubbletrail will sync automatically at startup and after you've added or
changed dives, or you can trigger a manual sync when required. The first
time you sync may take a while if you have a lot of dives.

[gh]: https://github.com/bubbletrail/bubbletrail/releases/latest
[as]: https://apps.apple.com/app/id6756735362
[sync]: https://admin.bubbletrail.net/
