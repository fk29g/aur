# Maintainer: Bart Libert <bart plus aur at libert dot email>

pkgname=hours
pkgver=0.4.1
pkgrel=1
pkgdesc='A no-frills time tracking toolkit for command line nerds'
arch=('x86_64')
url='https://tools.dhruvs.space/hours/'
license=('MIT')
depends=('glibc')
makedepends=('go')
source=("$pkgname-$pkgver.tar.gz::https://github.com/dhth/hours/archive/refs/tags/v${pkgver}.tar.gz")
b2sums=('aaf8370e48260a4b9ef6a9208f0b988dea49da92bac27473a21b5c0b68cfb487ef9bc55c5d472c7d85b294001e3f0c5b671dc828074bd9c34e07ae2bf245f979')

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
