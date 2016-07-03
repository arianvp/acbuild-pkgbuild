pkgdesc="App Container Image Build Command"
pkgname=acbuild
pkgver=0.3.1
pkgrel=2
arch=('i686' 'x86_64')
url="https://github.com/appc/acbuild"
source=("https://github.com/appc/${pkgname}/releases/download/v${pkgver}/${pkgname}-v${pkgver}.tar.gz"{,.asc})
validgpgkeys=('4AF8D94884580913')
md5sums=('SKIP')
makedepends=('git' 'go')
options=('!strip')
optdepends=(
    'gnupg: required to sign container images'
)
license=('Apache')

build() {
  cd "${srcdir}/${pkgname}-v${pkgver}"
  ./build
}

package() {
  cd "${srcdir}/${pkgname}-v${pkgver}"
  install -D -m755 bin/$pkgname "$pkgdir/usr/bin/$pkgname"
}
