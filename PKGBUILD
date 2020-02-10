# Maintainer: Caleb Maclennan <caleb@alerque.com>

_rockname=testmore
_project=lua-TestMore
pkgbase=lua-$_rockname
pkgname=("lua-$_rockname" "lua52-$_rockname" "lua51-$_rockname")
pkgver=0.3.5
_rockrel=1
pkgrel=1
arch=('any')
url="https://framagit.org/fperrad/$_project"
license=('MIT')
checkdepends=('lua')
source=("$pkgbase-$pkgver.tar.bz2::https://framagit.org/fperrad/$_project/-/archive/$pkgver/$_project-$pkgver.tar.bz2")
sha256sums=('a2daca2648e904def3e5467612d09e4f8956b1bc474d5f0994533e2aed3c5b8b')

check() {
  cd "$_project-$pkgver"
  make check
}

_package_helper() {
  cd "$_project-$pkgver"
  make LUAVER=$1 PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 COPYRIGHT "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_lua-testmore() {
  depends+=('lua')
  _package_helper 5.3
}

package_lua52-testmore() {
  depends+=('lua52')
  _package_helper 5.2
}

package_lua51-testmore() {
  depends+=('lua51')
  _package_helper 5.1
}
