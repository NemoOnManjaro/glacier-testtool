# $Id$

pkgname=glacier-testtool
pkgver=0.3
pkgrel=1
pkgdesc="Nemo hardware tester"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-testtool"
license=('BSD-3-Clause' 'LGPL-2.1-only')
depends=('qt6-glacier-app' 'qt6-sensors-sensorfw' 'qt6-charts')
makedepends=('cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('14e83474d28815ddfec86fbc3a156ee0219550cfaa4f1fbdbd32e0f38c6d1fc1')

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
