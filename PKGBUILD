pkgname=ocenaudio
pkgver=3.0.8
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
source=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
md5sums=('0e06c316bbc849e03e577b1fad7932c3')

package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"

  ln -sf "/opt/$pkgname/bin/${pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}


