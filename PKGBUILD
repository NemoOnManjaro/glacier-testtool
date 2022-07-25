# $Id$

pkgname=glacier-testtool
pkgver=0.2.1
pkgrel=1
pkgdesc="Nemo hardware tester"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-testtool"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt5-glacier-app' 'qt5-sensors-sensorfw' 'qt5-charts')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('34103698509cc7cdbb1f712be2938464044ecefb9016456c12475542b83ff064')

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
