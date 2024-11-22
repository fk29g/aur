# Maintainer: Bart Libert <bart plus aur at libert dot email>

pkgname=hours
pkgver=0.3.0
pkgrel=1
pkgdesc='A no-frills time tracking toolkit for command line nerds'
arch=('x86_64')
url='https://tools.dhruvs.space/hours/'
license=('MIT')
depends=('glibc')
makedepends=('go')
source=("$pkgname-$pkgver.tar.gz::https://github.com/dhth/hours/archive/refs/tags/v${pkgver}.tar.gz")
b2sums=('e1c86be43b6181869c5b81dd1d04033b836ff3ca561e77ed7bf0605d3189b40ddd1225e13285cbfab5a13bf03005db78a4d4d7594c6677b9c1d21f8056c5847f')

prepare(){
  cd "$pkgname-$pkgver"
  mkdir -p build/
}

build() {
  cd "$pkgname-$pkgver"
  export CGO_CPPFLAGS="${CPPFLAGS}"
  export CGO_CFLAGS="${CFLAGS}"
  export CGO_CXXFLAGS="${CXXFLAGS}"
  export CGO_LDFLAGS="${LDFLAGS}"
  export GOFLAGS="-buildmode=pie -trimpath -ldflags=-linkmode=external -mod=readonly -modcacherw"
  go build -o build
}

package() {
  cd "$pkgname-$pkgver"
  install -Dm755 build/$pkgname "$pkgdir"/usr/bin/$pkgname
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
