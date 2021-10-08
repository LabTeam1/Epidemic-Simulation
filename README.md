# Πρόβλημα
Πώς θα εξελιχθεί μία επιδημία σε μία κοινότητα ανάλογα με τα χαρακτηριστικά της και τα μέτρα καταπολέμησής της;

# Project
Αξιοποιούμε την Τεχνητή Νοημοσύνη σε πρόγραμμα προσομοίωσης (α) της εξάπλωσης μίας επιδημίας σε μία κοινότητα ατόμων, αλλά και (β) της αποτύπωσης της επίδρασης των μέτρων καταπολέμησης της διασποράς.
Όλο το project μας έχει προγραμματιστεί σε Python. Η εικονική αυτή κοινότητα παρουσιάζεται γραφικά στην οθόνη με τη βοήθεια της ενσωματωμένης open source βιβλιοθήκης της python, tkinter<sup>(1)</sup>. Κάθε άτομο της κοινότητας απεικονίζεται/αντιπροσωπεύεται από έναν "ανακλαστικό πράκτορα" τεχνητής νοημοσύνης, reflex agent<sup>(2)</sup>. Οι πράκτορες αυτοί κινούνται αυτόνομα μέσα στην εικονική κοινότητα, συναντιούνται και συνωστίζονται σε σημεία συγκέντρωσης. Καθώς κινούνται, υπάρχει το ενδεχόμενο να κολλήσουν τον ιό από κάποιο άλλο μέλος της κοινότητας και τηρούν τα μέτρα που ενδεχομένως έχουν οριστεί από τον χειριστή της προσομοίωσης (πχ. τήρηση αποστάσεων ή επιβολή μάσκας).

# Γιατί Τεχνητή Νοημοσύνη;
Το κομμάτι της τεχνητής νοημοσύνης στο συγκεκριμένο project συνίσταται στον προγραμματισμό των μελών της εικονικής κοινότητας ως reflex agents. Έτσι, τα άτομα αυτά κινούνται με βάση τον στόχο/προορισμό τους αλλά δεν λαμβάνουν ρητές οδηγίες για το πώς θα φτάσουν εκεί και ούτε προχωρούν "τυφλά". Αντιθέτως, κάθε άτομο ξεχωριστά, πριν από κάθε του κίνηση ελέγχει τα δεδομένα του περιβάλλοντός του και ύστερα κοστολογεί κάθε μία από τις πιθανές επόμενες κινήσεις του βάσει αυτών, επιλέγοντας τελικά την καλύτερη δυνατή. Με αυτόν τον τρόπο καταφέρνουμε να δημιουργήσουμε μία προσομοίωση όπου όλα τα άτομα της κοινωνίας κινούνται αυτόνομα, βρίσκοντας τις συντομότερες διαδρομές προς τον προορισμό τους ή/και ελέγχοντας το περιβάλλον τους προκειμένου να αποφύγουν, κατά το δυνατόν, την επαφή με άλλα άτομα σε περίπτωση επιβολής του μέτρου "τήρηση αποστάσεων".

# Δεδομένα
Όσον αφορά τον ιό, τα δεδομένα του (πιθανότητα μετάδοσης με και χωρίς χρήση μάσκας, ποσοστά θνησιμότητας κ.ά.) διαβάζονται με ειδικό τρόπο από ένα συγκεκριμένο αρχείο txt<sup>(3)</sup>. Για το project μας αυτό, χρησιμοποιούμε τα δεδομένα του ιού covid-19, αλλά το πρόγραμμα επιτρέπει την προσομοίωση και ιών με διαφορετικά χαρακτηριστικά (δεδομένου ότι αυτά δίνονται μέσω του σχετικού τυποποιημένου αρχείου txt). Τα στατιστικά στοιχεία και τα δεδομένα του covid-19, καθώς και τα μέτρα καταπολέμησης που χρησιμοποιήσαμε, προέρχονται από έγκυρες πηγές, όπως τον Παγκόσμιο Οργανισμό Υγείας (WHO).

# Λειτουργία
Ο χρήστης πατά το κουμπί Play και βλέπει την εξάπλωση/αντιμετώπιση της πανδημίας στην οθόνη γραφικά με χρωματική κωδικοποίηση. Στο παράθυρο φαίνονται όλα τα σχετικά δεδομένα, όπως το πλήθος των υγιών, των αρρώστων, των ατόμων με ανοσία, καθώς και το πλήθος των θανάτων. Ο χρήστης μπορεί ανά πάσα στιγμή να χρησιμοποιήσει τα αντίστοιχα κουμπιά που υπάρχουν στο παράθυρο για να επιβάλει στην κοινότητα τη χρήση μάσκας, την τήρηση αποστάσεων, ή και την επιβολή lockdown. 

(1)  https://docs.python.org/3/library/tkinter.html \
(2)  βλ. εικόνα reflex_agent.png, στο αποθετήριο GitHub του έργου μας https://github.com/LabTeam1/Epidemic-Simulation/blob/main/reflex_agent.png \
(3)  βλ. αρχείο virus_info.txt, στο αποθετήριο GitHub του έργου μας https://github.com/LabTeam1/Epidemic-Simulation/blob/main/code/virus_info.txt 
