# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=8
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=(https://github.com/downloads/falconindy/$pkgname/$pkgname-$pkgver.tar.gz{,.sig})
md5sums=('fa163bfc641b6c32c711a6d9e4519802'
         '74136d5e49f2a00e1e1a843fc88a35cb')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
