UNetbootin Source Revision 442
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sat May  1 14:45:17 EDT 2010

Download using git:
git clone git://unetbootin.git.sourceforge.net/gitroot/unetbootin
cd unetbootin
git checkout e39a2ef696ecdb9d18007caa9758e9f96af8f4f8

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r442

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
