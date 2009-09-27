UNetbootin Source Revision 372
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Sun Sep 20 17:02:06 EDT 2009

Download using git:
git clone git://unetbootin.git.sourceforge.net/gitroot/unetbootin
cd unetbootin
git checkout 66a03d84902ddde5a128c6e38cd3d7c36dcdf8ef

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r372

Build instructions at http://unetbootin.wiki.sourceforge.net/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
