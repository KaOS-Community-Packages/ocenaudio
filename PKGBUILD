pkgname=ocenaudio
pkgver=3.0.5
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
sha256sums_x86_64=('9453de656f87fdd1cd23f3036df60b499bff9e3f954f6b54005e8bbc6f50d246')
source_x86_64=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"
  ln -sf "/opt/$_pkgname/bin/${_pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}
