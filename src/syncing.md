# Συγχρονισμός με το AnkiWeb

<!-- toc -->

Το AnkiWeb είναι μία υπηρεσία που σας επιτρέπει να διατηρήσετε τη συλλογή σας
συγχρονισμένη μεταξύ πολλαπλών συσκευών και να διαβάσετε online. Παρακαλούμε εγγραφείτε για έναν
[δωρεάν λογαριασμό](https://ankiweb.net/) πρωτού ακολουθήσετε τα παρακάτω βήματα.

## Εισαγωγικά Video

Για μια γρήγορη εισαγωγή στον συγχρονισμό, παρακαλούμε δείτε τα
[syncing intro videos](https://www.youtube.com/watch?v=YkiM4DPzSVc&list=PLGgmaKOIHykFoomqkBJAyGiDQ2kyiuTao&yt:cc=on).

## Setup

Για να αρχίσετε τον συγχρονισμό της συλλογής σας μεταξύ συσκευών, click the sync button
(the top right one on the [main screen](studying.md#decks), or press 'y' on your keyboard.
You’ll be prompted for your AnkiWeb ID and password, which you created
in the signup process.

Όταν συγχρονίζετε τη συλλογή σας για πρώτη φορά, το Anki θα σας ρωτήσει
αν θέλετε να κάνετε λήψη ή ανέβασμα. Αν έχετε κάρτες στον υπολογιστή σας
και ο AnkiWeb λογαριασμός σας είναι κενός, επιλέξτε "ανέβασμα" για την αποστολή
των δεδομένων σας στο AnkiWeb. Αν έχετε κάρτες στο AnkiWeb από μια άλλη συσκευή
και καμία κάρτα στον υπολογιστή σας, επιλέξτε "λήψη" για την αντικατάσταση της άδειας
τοπικής συλλογής με κάρτες του AnkiWeb. Αν έχετε διαφορετικές κάρτες και στις δύο συσκευές, [more work is required](#merging-conflicts) για να αποφύγετε να χάσετε δεδομένα.

Once the initial one way sync is completed, Anki will be able to merge
changes from multiple locations with a few exceptions.

Αν διαφορετικά άτομα χρησιμοποιούν το Anki στον υπολογιστή σας και έχετε δημιουργήσει
ένα προφίλ για κάθε χρήστη, ο καθένας θα πρέπει να έχει τον δικό του λογαριασμό AnkiWeb
για τον συγχρονισμός του. Αν δοκιμάσετε να συγχρονίσετε πολλαπλά προφίλ με έναν AnkiWeb λογαριασμό
θα χάσετε δεδομένα.

## Αυτόματος συγχρονισμός

Once syncing is enabled, Anki will automatically sync each time your
collection is closed or opened. If you would prefer to synchronize
manually, you can disable automatic syncing in Anki’s [preferences.](preferences.md#syncing)

## Χρώμα κουμπιού

Το κουμπί συγχρονισμού αλλάζει σε μπλε όταν απαιτείται ένας κανονικός συγχρονισμός, ενώ σε κόκκινο
όταν απαιτείται ένας ολόκληρος συγχρονισμός.

## Πολυμέσα

Σχετικά video: <https://www.youtube.com/watch?v=phP9GGG-PxY>

Το Anki συγχρονίζει ήχους και εικόνες που χρησιμοποιούν οι σημειώσεις σας. It will
notice when media has been added or removed from your [media folder](files.md#file-locations), but
will not notice if you have edited some existing files without adding or
removing any. To get your edits noticed, you need to add or remove a
file as well.

One-way syncs (where you're prompted to upload or download) have no influence over how media
syncs - media changes are always merged.

To prevent accidental data loss, deletions will only sync to other devices if they are made after
media is fully in sync. If you delete files before your device is fully in sync, and the deleted
files are already on AnkiWeb, they will be downloaded the next time you sync.

If you’re running Anki off a [USB flash drive](files.md#running-from-a-flash-drive), you should use an NTFS
file system, as Anki may not be able to detect media changes on a FAT32
filesystem.

## Conflicts

Σχετικά video: <https://www.youtube.com/watch?v=UEAcpfMQnjo>

Κάτω υπό φυσιολογικές συνθήκες, οι επαναλήψεις και οι τροποποιήσεις των καρτών μπορούν να συγχωνευτούν, so if
you review or edit on two different devices before syncing, Anki will
preserve your changes from both locations. If the same card has been
reviewed in two different locations, both reviews will be marked in the
revision history, and the card will be kept in the state it was when it
was most recently answered.

Υπάρχουν μερικές αλλαγές τις οποίες το Anki δεν μπορεί να συγχωνεύσει. These mainly
relate to the format of notes: things like adding a new field, or
removing a card template. When you perform an operation that can’t be
merged, Anki will warn you, and give you the option of aborting the
operation. If you choose to continue, you’ll be asked to choose whether
to keep the local copy or the copy on AnkiWeb when your collection is
next synchronized.

If certain problems are detected while syncing, it will also force a one
way sync. If you find this consistently happens, please post on our
support site.

When a one way sync is required, you need to choose whether you wish to
keep the collection on your local device, or the collection on AnkiWeb.
If changes have been made on both ends, only changes on one end can be
preserved.

If you choose Upload, the content on your local device will be sent to
AnkiWeb. You then need to sync your other devices, and choose "Download"
to have them grab a copy of that content.

If you choose Download, it will replace any local changes you’ve made
with the data that is on AnkiWeb.

Once all devices are in sync, future syncs will return to the normal
behaviour of merging changes from both ends.

If you wish to force a full upload or download (for example, because you
accidentally deleted a deck on one side and want to restore the deck
rather than having its deletion synchronized), you can check the "On
next sync, force changes in one direction" box in
Tools&gt;Preferences&gt;Network, then sync as usual. (You’ll be given
the option to choose which side you want to use.)

Forcing a one way sync only affects card syncing - media is synced as
normal. If you have files that you want to remove from AnkiWeb, please
ensure your client is fully in sync first. After syncing is up to date,
any files you remove (e.g via the Check Media function) will be removed
from AnkiWeb on the following sync.

## Merging Conflicts

Because the [first sync](#setup) can only sync changes in one
direction, if you have added different content to different devices or
profiles before setting syncing up, content on one device will be lost
if you overwrite it with the content from the other device. With some
work, it is possible to manually merge data into a single collection.

Start by taking a backup on each device/profile, in case something goes
wrong. With the computer version you can use File&gt;Export to export
"all decks" with scheduling information and media files included, and
save the file somewhere safe. In AnkiMobile, the Add/Export button on
the decks list screen will let you export all decks with media.

Next, if one of your devices is a mobile device, synchronize it first.
If there’s a conflict, choose "upload" to overwrite any existing data on
AnkiWeb with the data from your mobile device. If both devices/profiles
are on your computer, synchronize the device/profile with the most
number of decks first.

Now return to the other device/profile. If automatic syncing is enabled,
a message may pop up asking if you want to upload or download. Click the
cancel button - we don’t want to sync yet.

Once you’re looking at the deck list, click the cog icon next to the
first deck, and choose "export". Export the content with scheduling
information and media included, and save the .apkg file somewhere. Now
you’ll need to repeat this for each top-level deck.

Once all top-level decks have been exported, click the sync button at
the top right, and choose "download", which will overwrite the local
content with the content you synced from your other device.

You can now use File&gt;Import to import the .apkg files you exported
earlier, which will merge the exported content with the existing
content, so everything will be in one place.

## Firewalls

Anki needs to be able to make outbound HTTPS connections to sync. It must be
able to connect to ankiweb.net, sync.ankiweb.net, sync2.ankiweb.net, and so on.
These domains may change over time, and the IP addresses they point to may also
change, so we recommend you allow wildcard access to \*.ankiweb.net to reduce
the chance of the firewall rules needing to be updated in the future.

If you have a firewall on your machine, you should add an exception for
Anki. If you are on a work or school network, please contact your
network administrator for assistance - it is not something we can help
you with.

## Proxies

If you need a proxy to access the internet, Anki should automatically
pick up your system proxy settings if you’re on Windows or macOS, and
will honour the HTTP_PROXY environment variable if you’re on another
platform.

Anki will only be able to pick up your system settings if a proxy is
manually configured, and does not require a password. If your system
uses automatic proxy setup, or uses a proxy that requires a username and
password, you will need to manually tell Anki the proxy configuration.

To tell Anki your proxy settings, define a HTTPS_PROXY environmental
variable that points to the proxy server. It will look like:

    http://user:pass@proxy.company.com:8080

If your username or password contains an @ (e.g `user@workdomain.com`),
you need to change it to %40, like so:

    http://user%40workdomain.com:pass@proxy.company.com:8080

Anki 2.0 expects to find HTTP_PROXY instead of HTTPS_PROXY.

To set environmental variables on Windows, please see
<https://www.google.com/search?q=windows+set+environmental+variable>

If you’re on a Mac, please see
<http://stackoverflow.com/questions/135688/setting-environment-variables-in-os-x>

Heavily locked down networks that intercept secure connections and
present their own certificate instead may cause Anki to throw up SSL
errors. In such environments, you may be able to work around the errors
with <https://ankiweb.net/shared/info/878367706>

An alternative solution is to install a local proxy server, and point
that proxy server at your normal proxy server. You can then tell Anki to
use the local proxy, which will redirect requests to the proxy you
normally use.
