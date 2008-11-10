UNetbootin Source Revision 299
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sat Nov  8 09:33:00 EST 2008
Download using bzr: bzr checkout http://bazaar.launchpad.net/~gezakovacs/unetbootin/devel-new -r299

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate unetbootin.pro
lrelease unetbootin.pro
qmake "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
