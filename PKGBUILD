pkgname=st
pkgver=20150529
pkgrel=1
pkgdesc='A simple virtual terminal emulator for X.'

arch=('i686' 'x86_64')
license=('MIT')
depends=('libxft')
makedepends=('ncurses' 'libxext' 'git')
url="http://st.suckless.org"
source=(git://github.com/enten/$pkgname)
sha256sums=('SKIP')

build() {
	cd $srcdir/$pkgname
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
	cd $srcdir/$pkgname
	make PREFIX=/usr DESTDIR=$pkgdir TERMINFO=$pkgdir/usr/share/terminfo install
}
