# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=11
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="https://projects.archlinux.org/arch-install-scripts.git"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=("ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig})
md5sums=('5a993926740e3d6de0ab7d7679a7b3cd'
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
