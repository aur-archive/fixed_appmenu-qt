pkgname=fixed_appmenu-qt
pkgbranch=trunk
pkgver=0.1.2
pkgrel=1
pkgdesc="Application menu module for Qt"
arch=('i686' 'x86_64')
url="https://launchpad.net/appmenu-qt"
license=('GPL')
depends=('libdbusmenu-qt>=0.7.0' 'fixed_qt-appmenu')
makedepends=('cmake' 'automoc4')
source=(http://launchpad.net/appmenu-qt/trunk/0.1.2/+download/appmenu-qt-0.1.2.tar.bz2)
sha1sums=('07939d653a036b6676c624a94d53ca327bc3415f')

build() {
   cd "${srcdir}/appmenu-qt-0.1.2"
   cmake . -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`
   make
}

package() {
   cd "${srcdir}/appmenu-qt-0.1.2"
   make DESTDIR="${pkgdir}" install
}
