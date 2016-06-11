# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=16
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="https://projects.archlinux.org/arch-install-scripts.git"
license=('GPL')
depends=('bash' 'coreutils' 'pacman' 'util-linux')
source=("https://sources.archlinux.org/other/$pkgname/$pkgname-$pkgver.tar.gz"{,.sig})
validpgpkeys=('487EACC08557AD082088DABA1EB2638FF56C0C53')  # Dave Reisner
md5sums=('c154998acb5f7cef802b53e129f6dec8'
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
