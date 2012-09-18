# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=7
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=(https://github.com/downloads/falconindy/$pkgname/$pkgname-$pkgver.tar.gz{,.sig})
md5sums=('54a3bc7b3b7dc7d5403c859493c6181d'
         '8e4e0ac25493c7c92dcabc449dccd80a')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
