UNetbootin Source Revision 613
Copyright Geza Kovacs
Homepage at http://unetbootin.sourceforge.net
Licensed under the GNU GPL v2 and above, components from other projects are licensed under their respective licenses
Build generated on Mon Jul 20 01:43:12 PDT 2015

Download using git:
git clone https://github.com/gkovacs/unetbootin.git
cd unetbootin
git checkout cbf30e41bbd2ad57f31feb29c559d6a2046f0d6c

Download using bzr:
bzr branch http://bazaar.launchpad.net/~vcs-imports/unetbootin/trunk -r613

Build instructions at http://sourceforge.net/apps/trac/unetbootin/wiki/compile

sed -i '/^RESOURCES/d' unetbootin.pro
lupdate-qt4 unetbootin.pro
lrelease-qt4 unetbootin.pro
qmake-qt4 "DEFINES += NOSTATIC" "RESOURCES -= unetbootin.qrc"
make
