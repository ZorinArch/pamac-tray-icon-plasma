# Maintainer: Artyom Grinyov (LordTermor)
# Maintainer: Zorin Arch (ZorinArch)

pkgname=pamac-tray-icon-plasma
pkgver=0.1.2
pkgrel=2
pkgdesc="Pamac tray icon for plasma users"
arch=('x86_64')
license=('GPL3')
depends=('pamac-aur>=10.0.2' 'qt5-base>=5.15.0' 'knotifications')
makedepends=('git' 'cmake')
conflicts=('pamac-tray-appindicator')
replaces=('pamac-tray-appindicator')
options=(!emptydirs)
source=("git+https://gitlab.com/LordTermor/$pkgname#commit=4c1d846750741b60239d4f5865d5bab987604611")
sha256sums=('SKIP')

prepare() {
  mkdir -p build
}

build() {
  cd build
  cmake \
    -DCMAKE_BUILD_TYPE="None" \
    -DCMAKE_INSTALL_PREFIX="/usr" \
    ../$pkgname
  make
}

package() {
  cd build
  make DESTDIR="${pkgdir}" install
}
 
