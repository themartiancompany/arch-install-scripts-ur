# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=6
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=(https://github.com/downloads/falconindy/$pkgname/$pkgname-$pkgver.tar.gz{,.sig})
md5sums=('26876d375d82b557465c5f00c3025267'
         'cc17e92c8539e518b17ea6c55749a969')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
