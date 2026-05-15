# Maintainer: artist for Sonic-DE

pkgname=sonic-workspace-wallpapers
pkgver=6.6.5
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

sha256sums=('0440c2f0719f10db3cbd7a163ad3830e8586f6e4158c128780e7b9814d0bf46e')

