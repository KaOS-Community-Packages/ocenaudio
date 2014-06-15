pkgname=ocenaudio
pkgver=2.0.5
pkgrel=1
pkgdesc="A cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('as-is')
depends=('qt')
source=("http://www.ocenaudio.com.br/downloads/${pkgname}64.deb")
md5sums=('f28966d9db0a5afa5ebd24d744805013')
 
 
build() {
  bsdtar -xf ${pkgname}64.deb data.tar.gz
  bsdtar -xf data.tar.gz
  rm data.tar.gz
  cd $srcdir/opt/$pkgname/lib
  rm libQt*
}
 
package() {
  cd $srcdir
  install -d -m 755 $pkgdir/opt/$pkgname/{lib,bin}
  install -d -m 755 $pkgdir/usr/share
  install -d -m 755 $pkgdir/usr/bin
  install -m 755 opt/$pkgname/bin/$pkgname $pkgdir/opt/$pkgname/bin/
  cp -d opt/$pkgname/lib/* $pkgdir/opt/$pkgname/lib/.
  cp -dR usr/share/applications $pkgdir/usr/share/.
  cp -dR usr/share/icons $pkgdir/usr/share/.
 
  ln -sf /opt/ocenaudio/bin/ocenaudio $pkgdir/usr/bin/ocenaudio
}