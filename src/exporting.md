# Εξαγωγή

<!-- toc -->

Η εξαγωγή σας επιτρέπει να αποθηκεύσετε μέρος της συλλογής σας ως αρχείο κειμένου ή
πακεταρισμένη τράπουλα Anki. Για την εξαγωγή πατήστε Εξαγωγή στο μενού Αρχείο.

## Αρχεία κειμένου

Αν επιλέξετε "Σημειώσεις σε απλό κείμενο", το Anki θα γράψει το περιεχόμενο
των σημειώσεων σε ένα αρχείο κειμένου. Κάθε πεδίο διαχωρίζεται από ένα tab.
Αν επεξεργαστείτε το αρχείο που προκύπτει και δεν τροποποιήσετε το πρώτο πεδίο,
μπορείτε αργότερα να εισάγετε αυτό το αρχείο ξανά στο Anki, και το Anki θα ενημερώσει
τις σημειώσεις σας βάσει των αλλαγών, δεδομένου ότι η εισαγωγή γίνεται στον ίδιο τύπο σημείωσης.

Αν επιθυμείτε να επεξεργαστείτε και το πρώτο πεδίο, θα πρέπει να αλλάξετε
την μορφή του τύπου σημείωσης έτσι ώστε το πρώτο πεδίο να είναι ένας ID αριθμός
αντί για απλό κείμενο. (Μπορείτε να εγκαταστήσετε για μεγαλύτερη ευκολία το πρόσθετο [Add note id](https://ankiweb.net/shared/info/1672832404).)

Για τη διατήρηση της μορφοποίησης κατά την εισαγωγή του κειμένου,
το κείμενο εξάγεται με ενσωματωμένη όλη την μορφοποίηση HTML.

## Πακεταρισμένες τράπουλες

Μια 'πακεταρισμένη τράπουλα' αποτελείται από κάρτες, σημειώσεις, τύπους σημειώσεων και ήχους ή εικόνες
ενωμένα μεταξύ τους σε ένα αρχείο με κατάληξη .apkg ή .colpkg. Μπορείτε να χρησιμοποιήσετε
πακεταρισμένες τράπουλες για να μεταφέρετε κάρτες μεταξύ ατόμων ή για τη δημιουργία αντιγράφων ασφαλείας
τμημάτων της συλλογής σας.

Υπάρχουν δύο διαφορετικά είδη πακεταρισμένων τραπουλών.

### Συλλογή (.colpkg)

When you export all decks with scheduling included, this is called a
'collection package'. Anki will copy your entire collection into a file
ending in .colpkg, and place it on your desktop. A collection package is
used to back up your collection, or copy it to another device.

Collection packages created with previous versions of Anki were called
collection.apkg.

When this file is later imported, Anki will delete all the current cards
in the collection, and replace the collection with the items in the
file. This is useful for copying your collection back and forth between
devices.

Existing media in your collection is not deleted when you import a
collection package. To delete unused media, use Tools&gt;Check Media.

Αν επιλέξετε την μορφή πακέτου συλλογης Anki 2.1.50+, οι εισαγωγές και εξαγωγές
θα είναι ταχύτερες και τα αρχεία πολυμέσων συμπιεσμένα, αλλά το αρχείο .colpkg
δεν θα είναι αναγνώσιμο από παλαιότερες εκδόσεις Anki.

### Τράπουλα (.apkg)

Τα πακέτα τράπουλας περιέχουν μια μόνο τράπουλα (and any child decks it may have).
Έχουν ένα όνομα αρχείου που τελειώνει σε .apkg, but a filename other than
collection.apkg. When you import a deck package, Anki will add the
contents into your collection, rather than overwriting your collection.

If some notes in the deck package have previously been imported, Anki
will keep the version with the most recent modification time. So if you
download an updated deck, the edits that have been made in the updated
version will be made in your collection as well, but if you re-import an
unchanged deck after making edits in your collection, the changes in
your collection will be kept.

Αν επιλέξετε να μην συμπεριλάβετε πληροφορίες προγραμματισμού, το Anki θα λάβει ως
δεδομένο ότι μοιράζεστε την τράπουλα με άλλα άτομα και θα αφαιρέσει  remove marked
and leech tags so that they will have a clean copy of it.
