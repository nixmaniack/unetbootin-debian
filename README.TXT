UNetbootin Source Revision 356
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sun Jun 14 15:06:00 PDT 2009
Download using bzr: bzr checkout http://bazaar.launchpad.net/~gezakovacs/unetbootin/devel-new -r356

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
