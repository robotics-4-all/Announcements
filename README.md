![logo](https://github.com/robotics-4-all/Announcements/blob/master/Capture.PNG?raw=true)
# Διαθέσιμες διπλωματικές ISSEL περιόδου Νοεμβρίου 2020

Παρακάτω μπορείτε να βρείτε τα νέα θέματα διπλωματικών της Ομάδας Ευφυών Συστημάτων και Τεχνολογίας Λογισμικού. Οι φοιτητές που ενδιαφέρονται για διπλωματική εργασία παρακαλούνται να συμπληρώσουν [τη φόρμα έκφρασης ενδιαφέροντος](https://issel.ee.auth.gr/diathesimes-diplwmatikes/%cf%86%cf%8c%cf%81%ce%bc%ce%b1-%ce%ad%ce%ba%cf%86%cf%81%ce%b1%cf%83%ce%b7%cf%82-%ce%b5%ce%bd%ce%b4%ce%b9%ce%b1%cf%86%ce%ad%cf%81%ce%bf%ce%bd%cf%84%ce%bf%cf%82/) έως και ημερομηνία που θα ανακοινωθεί στην επόμενο χρόνο. Επίσης, μπορείτε να βρείτε σχετικές ερωτήσεις σχετικά με τη διαδικασία επιλογής και τις απαιτήσεις στον παρακάτω σύνδεσμο: [Link](https://issel.ee.auth.gr/sixnes-erwtiseis/).

Την εβδομάδα (to be defined) θα διοργανωθεί διαδικτυακή παρουσίαση των θεμάτων (θα ακολουθήσει σχετική ανακοίνωση). Κατά τη διάρκεια της παρουσίασης θα συζητηθούν λεπτομέρειες πάνω στα θέματα, καθώς και οι διαδικασίες εκπόνησης των διπλωματικών. Παρακαλώ ενημερώστε όποιους άλλους μπορεί να ενδιαφέρονται.

Περιεχόμενα:
- [R4A-Autumn20-0: Εντοπισμός θέσης κινούμενου οχήματος σε εσωτερικό χώρο με χρήση πολλαπλών καμερών](#r4a-autumn20-0)
- [R4A-Autumn20-1: Εφαρμογή croud-sourcing τεχνικών για αυτόνομα αυτοκίνητα προς δημιουργία και παροχή web-based GIS layers](#r4a-autumn20-1)
- [R4A-Autumn20-2: Εύρεση θέσης πάρκινγκ με χρήση κινητού τηλεφώνου (ή αλλιώς Κατηγοριοποίηση τύπου κίνησης ανθρώπου με χρήση δεδομένων GPS και επιταχυνσιομέτρου από κινητό τηλέφωνο)](#r4a-autumn20-2)
- [R4A-Autumn20-3: Σχεδίαση και ανάπτυξη μηχανισμού εισαγωγής εκπαιδευτικών στόχων σε εφαρμογές εκπαιδευτικής ρομποτικής και επικύρωσης επίτευξής τους κατά την εκτέλεση αυτών](#r4a-autumn20-3)


---
## R4A-Autumn20-0
**Εντοπισμός θέσης κινούμενου οχήματος σε εσωτερικό χώρο με χρήση πολλαπλών καμερών**

Ο εντοπισμός θέσης ενός ρομποτικού οχήματος (global localization) είναι ένας από τους βασικότερους αλγορίθμους που πρέπει να διαθέτει ένα αυτόνομο ρομπότ. Αν και το συγκεκριμένο πρόβλημα διαθέτει μία πληθώρα λύσεων, η απόδειξη ότι οι συγκεκριμένοι αλγόριθμοι διαθέτουν την κατάλληλη ακρίβεια στον πραγματικό κόσμο είναι αρκετά δύσκολη, αφού πρέπει να είναι γνωστή η ακριβής πραγματική θέση του ρομπότ στον χώρο. Εφόσον η πλειοψηφία των αλγορίθμων localization λειτουργεί με αισθητήρες lidar, το validation συνήθως γίνεται με χρήση καμερών, οι οποίες βρίσκονται σε προκαθορισμένα σημεία στον χώρο και προσπαθούν να εντοπίσουν το όχημα σε διαβαθμισμένο έδαφος. Η εναλλακτική είναι ο εντοπισμός συγκεκριμένου μοτίβου το οποίο βρίσκεται πάνω στο ρομπότ, η εύρεση του γεωμετρικού μετασχηματισμού σε σχέση με κάθε κάμερα και τελικά η συνένωση όλης της πληροφορίας σε μία κυρίαρχη θέση. Στη παρούσα διπλωματική καλείστε να δημιουργήσετε ένα τέτοιο λογισμικό, το οποίο θα λειτουργεί με μεταβλητό αριθμό καμερών, για τις οποίες δεν θα απαιτείται εκ των προτέρων γνώση των σχετικών τους θέσεων, όπως και με κάποιο οπτικό μοτίβο του οποίου ο εντοπισμός και προσανατολισμός θα είναι εύκολος. Ο εντοπισμός θέσης θα γίνεται σε δύο βήματα. Στο πρώτο, θα γίνεται εντοπισμός των σχετικών θέσεων των καμερών με χρήση του οπτικού pattern, ενώ στο δεύτερο βήμα θα χρησιμοποιούνται οι θέσεις των καμερών, ώστε να εντοπίζεται η θέση του ρομποτικού οχήματος, στο οποίο θα υπάρχει το ίδιο ή διαφορετικό pattern.

**Γνώσεις που θα αποκτηθούν:** Python ή C++, λήψη δεδομένων από πολλαπλές κάμερες με χαμηλό latency, επεξεργασία εικόνας, μαθηματικοί μετασχηματισμοί

**Εκτιμώμενος χρόνος περάτωσης:** 9 μήνες

**Συνεργαζόμενοι ερευνητές:** Δρ. Τσαρδούλιας Εμμανουήλ, Υπ.Δρ. Καρανικιώτης Θωμάς

---

## R4A-Autumn20-1
**Εφαρμογή croud-sourcing τεχνικών για αυτόνομα αυτοκίνητα προς δημιουργία και παροχή web-based GIS layers**

Δύο από τις πιο υποσχόμενες τεχνικές στον τομέα της οδήγησης είναι 1) τα αυτόνομα οχήματα, έχοντας ώς σκοπό (μεταξύ άλλων) α) η μείωση των ατυχημάτων και β) η αύξηση της προσβασιμότητας μίας πόλης από άτομα με κινητικές δυσκολίες, και 2) εφαρμογές croud-sourcing οι οποίες λαμβάνουν δεδομένα από κινούμενα οχήματα (είτε άμεσα από αισθητήρες τους, είτε έμμεσα από τα κινητά των επιβατών) και παρέχουν χρήσιμη πληροφορία στους τελικούς χρήστες. Μία από τις γνωστότερες εφαρμογές croud-sourcing για οδήγηση είναι η ένδειξη της κίνησης στην εφαρμογή GoogleMaps, αφού αυτή προκύπτει από τα ενεργά GPS κάθε οδηγού, και τελικά χρησιμοποιείται ώστε να προτείνονται συντομότερες χρονικά (αλλά όχι απαραίτητα σε μήκος) διαδρομές. Σκοπός της παρούσας διπλωματικής έργασίας είναι η χρήση πολλαπλών προσομοιωμένων οχημάτων τα οποία θα κινούνται σε μία εικονική πόλη, από τα οποία θα γίνεται συλλογή δεδομένων ταχύτητας, lidar ή καμερών σε δομές IoT/BigData, έχοντας ως τελικό σκοπό την επεξεργασία τους σε near-real-time ώστε να προκύπτουν χρήσιμες πληροφορίες σχετικά με την οδήγηση. Κάθε είδος πληροφορίας θα παρέχεται ως διαφορετικό layer σε κάποιο open-source σύστημα GIS (πχ https://www.openstreetmap.org/). Πιθανές εφαρμογές είναι η ένδειξη της κίνησης σε δρόμους, εντοπισμός εμποδίων στον δρόμο, εντοπισμός τρακαρισμάτων, εντοπισμός ελευθέρων θέσεων parking κτλ.)

**Γνώσεις που θα αποκτηθούν:** Python, λήψη δεδομένων από ετερογενείς αισθητήρες, διαχείριση IoT frameworks/BigData infrastructures, Machine learning, GIS frameworks

**Εκτιμώμενος χρόνος περάτωσης:** 9 μήνες

**Συνεργαζόμενοι ερευνητές:** Δρ. Τσαρδούλιας Εμμανουήλ, Υπ.Δρ. 

---

## R4A-Autumn20-2
**Εύρεση θέσης πάρκινγκ με χρήση κινητού τηλεφώνου (ή αλλιώς Κατηγοριοποίηση τύπου κίνησης ανθρώπου με χρήση δεδομένων GPS και επιταχυνσιομέτρου από κινητό τηλέφωνο)**

Είναι γεγονός ότι τα σύγχρονα κινητά τηλέφωνα είναι μία πηγή πλούσιας πληροφορίας αφού διαθέτουν πληθώρα ετερογενών αισθητήρων. Συγκεκριμένα, μέσω της χρήσης των αισθητήρων GPS και επιταχυνσιομέτρου είναι δυνατός ο υπολογισμός μοτίβων κίνησης του εκάστοτε ανθρώπου, πάντα σε πλαίσιο ανωνυμοποίησης των δεδομένων. Η συγκεκριμένη διπλωματική στοχεύει στην χρήση αυτών των δεδομένων με στόχο τον εντοπισμό του πότε ο κάτοχος του κινητού παρκάρει ή ξεπαρκάρει, έχοντας ως απώτερο σκοπό την συλλογή παρόμοιων δεδομένων από πολλά άτομα (crowdsourcing) και την παρουσίαση των αποτελεσμάτων σε ένα mobile app. Τα βήματα της διπλωματικής εργασίας περιλαμβάνουν:
- Την δημιουργία native mobile application το οποίο θα λαμβάνει δεδομένα GPS και επιταχυνσιομέτρου
- Την αποστολή δεδομένων (personalized but anonymous) σε IoT/BigData υποδομή
- Την υλοποίηση ML αλγορίθμων μέσω των οποίων θα γίνεται το classification της κίνησης (π.χ. περπάτημα, οδήγηση κτλ.), από την οποία θα προκύψουν τα χρήσιμα events (παρκάρισμα / ξεπαρκάρισμα)
- Την δημιουργία συστήματος/layer GIS (Geographic Information System), στο οποίο θα παρουσιάζονται σε πραγματικό χρόνο heatmaps με την συχνότητα των events.
Το τελικό αποτέλεσμα που θα εμφανίζεται στον χρήση είναι η ένδειξη ότι μία περιοχή ή δρόμος παρουσιάζει υψηλή κινητικότητα παρκαρίσματος/ξεπαρκαρίσματος, ούτως ώστε η προσπάθεια εύρεσης κάποιας ελεύθερης θέσης να είναι περισσότερο στοχευμένη.


**Γνώσεις που θα αποκτηθούν:** Mobile app development (Android), λήψη δεδομένων αισθητήρων από κινητό, αλγόριθμοι ML, χρήση εργαλείων GIS

**Εκτιμώμενος χρόνος περάτωσης:** 9 μήνες

**Συνεργαζόμενοι ερευνητές:** Δρ. Τσαρδούλιας Εμμανουήλ, Υπ.Δρ. Καρανικιώτης Θωμάς

---

## R4A-Autumn20-3
**Σχεδίαση και ανάπτυξη μηχανισμού εισαγωγής εκπαιδευτικών στόχων σε εφαρμογές εκπαιδευτικής ρομποτικής και επικύρωσης επίτευξής τους κατά την εκτέλεση αυτών.**

Αναμφίβολα ο τομέας της εκπαιδευτικής ρομποτικής έχει πλέον εδραιωθεί στο σύγχρονο σχολείο, όπου χρησιμοποιούνται μια πληθώρα πλατφορμών εκπαιδευτικής ρομποτικής. Οι περισσότερες από αυτές στοχεύουν στο να εισάγουν τους μαθητές στις βασικές έννοιες τις ρομποτικής μέσω της δυνατότητας δημιουργίας εφαρμογών που χρησιμοποιούν ποικίλα αισθητήρια (sensors), διάφορους ενεργοποιητές (effectors) καθώς και έξυπνους αλγορίθμους. Ωστόσο, απουσιάζει η δυνατότητα (εκ μέρους του διδάσκοντος) ορισμού των στόχων μιας άσκησης και επιπλέον της δυνατότητας επαλήθευσης κατά την εκτέλεσή της πως ο μαθητής πέτυχε να ολοκληρώσει επιτυχώς την εκάστοτε άσκηση. Η παρούσα διπλωματική, στοχεύει συνεπώς να παράσχει την προαναφερθείσα δυνατότητα μοντελοποίησης εκπαιδευτικών στόχων, τους οποίους ο διδάσκων κατά τη σχεδίαση ασκήσεων θα μπορεί με εύκολο τρόπο μέσω γραφικής διεπαφής (GUI) να εισάγει. Κατόπιν, μέσω του λογισμικού που παράγεται από το μηχανισμό της διπλωματικής, το ρομπότ και το περιβάλλον αυτού, “παρακολουθούνται” στενά ούτως ώστε να αξιολογείται σε πραγματικό χρόνο αν κάποια χρονική στιγμή έχει ικανοποιηθεί κάποιος επιπλέον στόχος που έχει τεθεί και εν τέλει κατά τον τερματισμό της εφαρμογής να μπορεί να αξιολογηθεί η επίδοση του μαθητή. Ο παραπάνω μηχανισμός θα εφαρμοστεί στην ήδη υπάρχουσα πλατφόρμα εκπαιδευτικής ρομποτικής του εργαστηρίου TekTrain.

**Προαπαιτούμενα:** Αντικειμενοστραφής Προγραμματισμός, προτιμητέα η γνώση Python (όχι απαιτούμενη).

**Γνώσεις που θα αποκτηθούν:** Μοντελοποίηση, Αυτόματη Μηχανική Λογισμικού, Αρχιτεκτονική ρομποτικού προσομοιωτή

**Εκτιμώμενος χρόνος περάτωσης:** 9-12 μήνες

**Συνεργαζόμενοι ερευνητές:** Δρ. Ζολώτας Χριστόφορος, Δρ. Τσαρδούλιας Εμμανουήλ


