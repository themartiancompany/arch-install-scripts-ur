# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=1
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/$pkgname"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=("$pkgname-$pkgver.tar.gz::https://www.github.com/falconindy/$pkgname/tarball/v$pkgver")
md5sums=('85efe23284fb3997399c8487cb5dc3c5')

build() {
  dirname=$(tar tf "$pkgname-$pkgver.tar.gz" | sed 1q)
  make -C "$dirname"
}

package() {
  dirname=$(tar tf "$pkgname-$pkgver.tar.gz" | sed 1q)
  make -j1 -C "$dirname" PREFIX=/usr DESTDIR="$pkgdir" all install
}

# vim:set ts=2 sw=2 et:
