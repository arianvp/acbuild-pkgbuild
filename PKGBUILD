pkgdesc="App Container Image Build Command"
pkgname=acbuild
pkgver=0.4.0
pkgrel=2
arch=('i686' 'x86_64')
url="https://github.com/containers/build"
source=("https://github.com/containers/build/releases/download/v${pkgver}/${pkgname}-v${pkgver}.tar.gz"{,.asc})
validgpgkeys=('4AF8D94884580913')
md5sums=('157a2b2b17b0cf59442331fb20622bd5', '678d3533813d1a8cdc90538f0d1f11cd')
makedepends=('go')
options=('!strip')
optdepends=(
    'gnupg: required to sign container images'
)
license=('Apache')


package() {
  cd "${srcdir}/${pkgname}-v${pkgver}"
  install -D -m755 $pkgname "$pkgdir/usr/bin/$pkgname"
}
md5sums=('157a2b2b17b0cf59442331fb20622bd5'
         'SKIP')
