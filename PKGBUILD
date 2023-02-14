# $Id$

pkgname=glacier-testtool
pkgver=0.2.2
pkgrel=1
pkgdesc="Nemo hardware tester"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-testtool"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'qt5-sensors-sensorfw' 'qt5-charts')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('010fb1a80e0ac1dbeae6b76ee9c316441408927427e78bb23eefa08c81b7ec29')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
