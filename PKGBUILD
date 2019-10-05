# Maintainer: Jguer <joaogg3@gmail.com>
pkgname=yay
pkgver=9.3.3
pkgrel=1
pkgdesc="Yet another yogurt. Pacman wrapper and AUR helper written in go."
arch=('i686' 'x86_64' 'armv7h' 'armv6h' 'aarch64')
url="https://github.com/Jguer/yay"
license=('GPL')
depends=(
  'pacman>=5.1.0'
  'pacman<=5.1.3'
  'sudo'
  'git'
)
makedepends=(
  'go'
)
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/Jguer/yay/archive/v${pkgver}.tar.gz")
sha1sums=('78def56ee761c17f929d83a8a111610f92ac5d34')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  EXTRA_GOFLAGS="-gcflags all=-trimpath=${PWD} -asmflags all=-trimpath=${PWD}" \
    LDFLAGS="-linkmode external -extldflags \"${LDFLAGS}\"" \
    make VERSION=$pkgver DESTDIR="$pkgdir" build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make VERSION=$pkgver DESTDIR="$pkgdir" PREFIX=/usr install
}
