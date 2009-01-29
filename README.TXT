UNetbootin Source Revision 308
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sun Jan 25 18:35:08 EST 2009
Download using bzr: bzr checkout http://bazaar.launchpad.net/~gezakovacs/unetbootin/devel-new -r308

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
