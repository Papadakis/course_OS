Αθανάσιος Παπαδάκης	993	papadaki@uth.gr
Απόστολος Τσαούσης	1714	aptsaous@uth.gr

Για την μεταγλώττιση της εφαρμογής find_roots_lib, αρχικά εκτελούμε την εντολή
gcc -c roots.c -o roots
Στην συνέχεια για την δημιουργία της στατικής βιβλιοθήκης χρησιμοποιούμε την εντολή
ar rcs libroots.a roots
Διασυνδέουμε την βιβλιοθήκη με την find_roots_lib με την παρακάτω εντολή
gcc -static find_roots_lib.c -L. -lroots -o find_roots_lib
Τέλος τρέχουμε την εφαρμογή με την εντολή
./find_roots_lib

Για την μεταγλώττιση του module, αρχικά εκτελούμε στον φάκελο που βρίσκεται το project1-iosched.c την εντολή make.
Μόλις δημιουργηθεί το αρχείο project1-iosched.ko, δίνουμε την εντολή insmod project1-iosched.ko και μετά την εντολή dmesg | tail
για να επιβεβαιώσουμε ότι έγινε ορθά η εισαγωγή.
Τέλος για την αφαίρεση του module χρησιμοποιούμε την εντολή rmmod project1-iosched.ko

