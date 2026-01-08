# Syncing

Bubbletrail supports syncing via a cloud storage account. The sync method is
platform independent and works with all editions of Bubbletrail (macOS, iOS,
Android, etc.).

## Privacy

Bubbletrail sync data by storing dives, sites, etc as objects in cloud
storage. These objects are encrypted into a "vault" using the user-specified
"vault key". The storage provider thus gets limited access to the synced
data. Specifically, they cannot see any information about dives, sites etc
themselves, including any names, identifiers or statistics stored with them.

However, dives are stored as individual storage objects, and the object key
may include the date of the dive. (The specific key used depends on whether
the dive was created in Bubbletrail or imported from any of several
supported import formats.) The storage provider can thus see *how many dives
are in the log*, in some cases *the date when they occurred*, and they can
infer that you've been diving when new dives are added to the vault.
