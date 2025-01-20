# Maintainer: Bart Libert <bart plus aur at libert dot email>

pkgname=hours
pkgver=0.4.0
pkgrel=1
pkgdesc='A no-frills time tracking toolkit for command line nerds'
arch=('x86_64')
url='https://tools.dhruvs.space/hours/'
license=('MIT')
depends=('glibc')
makedepends=('go')
source=("$pkgname-$pkgver.tar.gz::https://github.com/dhth/hours/archive/refs/tags/v${pkgver}.tar.gz")
b2sums=('a2c917b4ad8f21a20348fc01b7124cddb9d451ec3ed75b16440419cfe8b0e65b38070fad2a189fa923e5308d6fc4c14a01c20907899226b0de7657957b02a986')

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
