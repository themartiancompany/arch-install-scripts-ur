# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>
# Maintainer: David Runge <dvzrv@archlinux.org>
# Maintainer: Morten Linderud <foxboron@archlinux.org>
# Contributor: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver=28
pkgrel=2
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="https://gitlab.archlinux.org/archlinux/arch-install-scripts"
license=('GPL2')
depends=(
  'awk'
  'bash'
  'coreutils'
  'grep'
  'pacman'
  'util-linux'
)
_os="$( \
  uname \
    -o)"
if [[ "${_os}" == "GNU/Linux" ]]; then
  depends+=(
    awk
  )
fi
if [[ "${_os}" == "Android" ]]; then
  depends+=(
    gawk
  )
fi

makedepends=(
  'asciidoc'
  'git'
)
source=(
  "git+$url.git#tag=v${pkgver}?signed"
)
validpgpkeys=(
  'BD27B07A5EF45C2ADAF70E0484818A6819AF4A9B'  # Eli Schwartz
  'C100346676634E80C940FB9E9C02FF419FECBE16'  # MortenLinderud
)
sha256sums=(
  'SKIP'
)

pkgver() {
  cd \
    "$pkgname"
  git \
    describe | \
    sed \
      's/^v//'
}

build() {
  make \
    -C \
      "$pkgname"
}

check() {
  make \
    -C \
      "$pkgname" \
    check
}

package() {
  make \
    -C \
      "$pkgname" \
    PREFIX=/usr \
    DESTDIR="$pkgdir" \
    install
}

