pkgname=ocenaudio
pkgver=3.1.9
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
source=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
md5sums=('5b34d4f30cb9d3ecb1a56a43ce9bee73')

package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"

  ln -sf "/opt/$pkgname/bin/${pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}
