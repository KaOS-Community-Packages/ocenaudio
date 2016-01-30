pkgname=ocenaudio
pkgver=3.0.6
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
sha256sums_x86_64=('cb58a734c9ba8d193ef8e0c44ecee08abe5d978b52da6efd9a1b533801eb565b')
source_x86_64=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"
  ln -sf "/opt/$_pkgname/bin/${_pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}
