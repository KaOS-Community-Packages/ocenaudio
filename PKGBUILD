pkgname=ocenaudio
pkgver=3.0.4
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
sha256sums_x86_64=('e23dd32ab5dc77e51387d2202ee760489b4a82f3ace2bc7e622b3e128168638b')
source_x86_64=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"
  ln -sf "/opt/$_pkgname/bin/${_pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}
