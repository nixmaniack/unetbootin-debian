UNetbootin Source Revision 301
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Tue Nov 11 16:40:44 EST 2008
Download using bzr: bzr checkout http://bazaar.launchpad.net/~gezakovacs/unetbootin/devel-new -r301

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
