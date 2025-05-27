# Maintainer: fk29g <fk29g.uphill912@slmails.com>
# Contributor: Bart Libert <bart plus aur at libert dot email>
pkgname=hours
pkgver=0.5.0
pkgrel=1
pkgdesc='A no-frills time tracking toolkit for command line nerds'
arch=('x86_64')
url='https://tools.dhruvs.space/hours/'
license=('MIT')
makedepends=('go')
provides=("hours")
conflicts=("hours")
source=("$pkgname-$pkgver.tar.gz::https://github.com/dhth/hours/archive/refs/tags/v${pkgver}.tar.gz")
b2sums=('8bc7fb78f12e0aa94465534b354e6a331c12d9a871035d3ff14b08e247be259f21cf026f855384afb3c939d17309184c2145d16cf45ee905553c5c29c848840b')

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
    install -Dm 755 build/$pkgname "$pkgdir"/usr/bin/$pkgname
    install -Dm 644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
    install -Dm 644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
}
