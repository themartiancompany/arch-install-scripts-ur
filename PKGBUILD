# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=9
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=(https://github.com/downloads/falconindy/$pkgname/$pkgname-$pkgver.tar.gz{,.sig})
md5sums=('672a7bf8f20cf5c86a3a3ff4f132c5f6'
         'd58a94848ba18cdfebbb262fe70c819d')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
