# Syncing

Bubbletrail supports syncing via a cloud storage account. The sync method is
platform independent and works with all editions of Bubbletrail (macOS, iOS,
Android, etc.).

To get started with syncing, visit <https://admin.bubbletrail.net/> and sign
up with your email address. You'll get the credentials to enter in
Bubbletrail. We won't spam you or sell your email address -- we only use it
as a unique identifier, and to have a point of contact in case of problems.

## Privacy

Bubbletrail syncs data by storing dives, sites, etc as objects in cloud
storage. These objects are encrypted into a "vault" using the user-specified
"vault key". The storage provider thus gets very limited access to the
synced data. Specifically, they cannot see any information about dives,
sites etc themselves, including any names, identifiers or statistics stored
with them.

However, dives are stored as individual storage objects, and the object key
may include the date of the dive. The storage provider can thus see *how
many dives are in the log*, in many cases *the date when they occurred*, and
they can infer that you've been diving when new dives are added to the
vault.

### Vault keys

The vault key you enter in the syncing preferences fulfils dual purposes:

- It is the seed for the encryption key for your data.
- It forms a partition inside the sync bucket.

The latter point means that you can have multiple separate sets of devices
using the _same bucket, access key, and secret key_, but _different vault
keys_. The devices with the same vault key will sync with each other; the
ones with different vault keys will simply not see each other at all. This
means a storage bucket can be shared for syncing separate Bubbletrail
databases, for example by family members.
