pkgname=ocenaudio
pkgver=3.0.6
pkgrel=1
pkgdesc="Cross-platform, easy to use, fast and functional audio editor"
arch=('x86_64')
url="http://www.ocenaudio.com.br/"
license=('custom')
depends=('desktop-file-utils' 'gtk-update-icon-cache' 'jack' 'pulseaudio'
         'qt5-base' 'shared-mime-info')
source=("http://www.ocenaudio.com.br/downloads/ocenaudio_debian64.deb")
md5sums=('4a706f1c57c7916b2ba1d540657e8270')

package() {
  tar -xJf ${srcdir}/data.tar.xz -C "${pkgdir}"
  install -dm755 "${pkgdir}/usr/bin"
  
  ln -sf "/opt/$_pkgname/bin/${_pkgname}" "${pkgdir}/usr/bin"
  rm -rf "${pkgdir}/var"
}
