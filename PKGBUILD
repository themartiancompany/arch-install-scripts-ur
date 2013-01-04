# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=10
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="http://github.com/falconindy/arch-install-scripts"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=("ftp://ftp.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig})
md5sums=('ce34cc7ebbc03c3aa45a8d9dc0bc5c5f'
         '8f88eea7e62dffde09ecd4bb89d44e56')

build() {
  make -C "$pkgname-$pkgver"
}

package() {
  make -C "$pkgname-$pkgver" PREFIX=/usr DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
