# Contributor: crmaxx <crmaxx@gmail.com>
pkgname=pptpclient-rdr
pkgver=1.7.2
pkgrel=1
pkgdesc="Client for the proprietary Microsoft Point-to-Point Tunneling Protocol, PPTP. ppp-rdr version"
url="http://pptpclient.sourceforge.net/"
license="GPL"
depends=(glibc ppp-rdr)
backup=(etc/ppp/{options.pptp})
source=(http://dl.sourceforge.net/sourceforge/pptpclient/pptp-$pkgver.tar.gz)
md5sums=('4c3d19286a37459a632c7128c92a9857')
arch=(i686 x86_64)
 
build() { 
  cd $startdir/src/pptp-$pkgver
  sed -i '/CFLAGS/d' Makefile
  make || return 1
  make DESTDIR=$startdir/pkg install
}
