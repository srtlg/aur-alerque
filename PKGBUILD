# Contributor: unlucu <unlucu at gmail dot com>

pkgname=aspell-tr
pkgver=0.50
pkgrel=1
pkgdesc="Turkish dictionary for aspell"
arch=('i686' 'x86_64')
url="http://turkce.sourceforge.net/"
license=('GPL')
depends=('aspell')
source=('ftp://ftp.gnu.org/gnu/aspell/dict/tr/aspell-tr-0.50-0.tar.bz2')
md5sums=('432ecdc4e5233da0a4c1a52ed9103fa2')

build() {
  cd $startdir/src/aspell-tr-${pkgver}-0
  ./configure
  make || return 1
  make DESTDIR=$startdir/pkg install
}
