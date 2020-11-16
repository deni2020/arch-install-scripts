# Maintainer: Dave Reisner <dreisner@archlinux.org>

pkgname=arch-install-scripts
pkgver='23_3_????????'
pkgrel=1
pkgdesc="Scripts to aid in installing Arch Linux"
arch=('any')
url="https://github.com/deni2020/arch-install-scripts"
license=('GPL')
depends=('awk' 'bash' 'coreutils' 'pacman' 'util-linux')
makedepends=('asciidoc' 'git')

pkgver() {
  cd "$startdir"

  git describe | sed 's/^v//; s/-/_/g'
}

build() {
  make -C "$startdir"
}

check() {
  make -C "$startdir" check
}

package() {
  make -C "$startdir" PREFIX=/usr DESTDIR="$pkgdir" install
}
