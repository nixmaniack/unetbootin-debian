UNetbootin Source Revision 429
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sun Apr  4 04:22:28 EDT 2010

Download using git:
git clone git://unetbootin.git.sourceforge.net/gitroot/unetbootin
cd unetbootin
git checkout e5963601e9591184b8e18fa3d9d8ea23c09cbd8d

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r429

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
