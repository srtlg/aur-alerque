# Maintainer:  Caleb Maclennan <caleb@alerque.com>

pkgname=otf-antykwa-torunska
pkgver=2.08
pkgrel=2
pkgdesc='Open Type Antiqua of Torun, a two-element typeface designed by Zygfryd Gardzielewski'
arch=('any')
url='http://jmn.pl/en/antykwa-torunska/'
license=('custom')
source=("http://jmn.pl/pliki/AntykwaTorunska-otf-${pkgver/./_}.zip")
sha256sums=('9f225ce269b5757b31019435077ea84606ba56b7d36a0b94f51dacd370b5868d')

package() {
    cd antt-otf
    install -Dm644 -t "$pkgdir/usr/share/fonts/OTF/" *.otf
}
