# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=5
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=(https://github.com/downloads/falconindy/$pkgname/$pkgname-$pkgver.tar.gz{,.sig})
md5sums=('7b11caeb9958a36a323bfe2b109c1566'
         '569ec9f8a499068de49e6641bb85c82e')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
