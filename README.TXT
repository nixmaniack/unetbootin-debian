UNetbootin Source Revision 585
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on 2013年  7月  3日 水曜日 03:23:26 EDT

Download using git:
git clone git://unetbootin.git.sourceforge.net/gitroot/unetbootin
cd unetbootin
git checkout 7f39ef3f700d6f2fe8e904dcdfe8d9c7f6f83d9b

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r585

Build instructions at http://sourceforge.net/apps/trac/unetbootin/wiki/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
