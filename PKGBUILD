# Maintainer: artist for Sonic-DE

pkgname=sonic-workspace-wallpapers
pkgver=6.6.4
_dirver=$(echo $pkgver | cut -d. -f1-3)
pkgrel=1
pkgdesc='Additional wallpapers for the Sonic Workspace'
arch=(any)
url='https://github.com/Sonic-DE/sonic-workspace-wallpapers'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(sonicde)
conflicts=(plasma-workspace-wallpapers)
provides=(plasma-workspace-wallpapers)
replaces=(plasma-workspace-wallpapers)
source=("$pkgname-$pkgver.tar.gz::${url}/archive/refs/tags/$pkgver.tar.gz")

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}

sha256sums=('bb6d6a0a3fa7c8045dbc112087d3fc77e3fd6a1cf65a359ad80250a32cdc7cec')

