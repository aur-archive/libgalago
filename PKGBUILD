# $Id: PKGBUILD 78820 2012-10-25 06:47:28Z foutrelis $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: William Rea <sillywilly@gmail.com>

pkgname=libgalago
pkgver=0.5.2
pkgrel=4
pkgdesc="The Galago presence library"
arch=(i686 x86_64)
url="http://www.galago-project.org"
options=('!libtool')
license=("LGPL")
depends=('dbus-glib')
source=(http://www.galago-project.org/files/releases/source/libgalago/libgalago-$pkgver.tar.gz
	libgalago-mkinstalldirs.patch)
md5sums=('7ec92f2ecba1309ac4b71b4b4d8d0a0d'
         '3b38fecc5421ca338363b9ae1d218b7e')

build() {
  cd $srcdir/libgalago-$pkgver
  patch -p0 -i ../libgalago-mkinstalldirs.patch
  ./configure --prefix=/usr --disable-tests
  make
  make DESTDIR=$pkgdir install
  rm -rf $pkgdir/usr/share/autopackage
}
