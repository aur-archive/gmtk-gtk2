# Maintainer: OK100 <ok100.ok100.ok100@gmail.com>

pkgname=gmtk-gtk2
pkgver=1.0.8
pkgrel=1
pkgdesc='Common functions for gnome-mplayer and gecko-mediaplayer. GTK2 version.'
arch=('i686' 'x86_64')
url='http://gmtk.googlecode.com/'
license=('GPL')
depends=('glib2' 'gtk2' 'dconf')
makedepends=('intltool' 'pkg-config')
provides=(gmtk=${pkgver})
conflicts=('gmtk')
options=(!libtool)
source=("http://gmtk.googlecode.com/files/gmtk-${pkgver}.tar.gz")

build() {
  cd "${srcdir}/gmtk-${pkgver}"

  export CPPFLAGS="$CPPFLAGS $(pkg-config --cflags gtk+-2.0)"
  ./configure --prefix=/usr --sysconfdir=/etc --disable-gtk3
  make
}

package() {
  cd "${srcdir}/gmtk-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

md5sums=('ee8ab99f3ac2e0071c99a35e4847bba5')
