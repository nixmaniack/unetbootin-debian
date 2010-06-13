UNetbootin Source Revision 471
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Thu Jun  3 14:59:18 PDT 2010

Download using git:
git clone git://unetbootin.git.sourceforge.net/gitroot/unetbootin
cd unetbootin
git checkout 04e3672278060522988f6df3d1f8ec17278dd4a6

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r471

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
