# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=14
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="https://projects.archlinux.org/arch-install-scripts.git"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=("ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig})
md5sums=('fcab5a3e463413b06790969cfe09851c'
         'SKIP')

build() {
  make -C "$pkgname-$pkgver"
}

check() {
  make -C "$pkgname-$pkgver" check
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
