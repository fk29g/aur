# Maintainer: fk29g <fk29g.uphill912@slmails.com>
pkgname=reddit-tui
pkgver=0.3.6
pkgrel=1
pkgdesc="Terminal UI for Reddit"
arch=("x86_64")
url="https://github.com/tonymajestro/reddit-tui"
license=("MIT")
makedepends=("go>=1.16")
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=("7c386a54a8e73369013fe20a2bd71010548b328ad5fc59ed49c51db42478f654")

build() {
    cd "$pkgname-$pkgver"
    go build -o reddittui main.go
}

package() {
    cd "$pkgname-$pkgver"
    install -Dm 0755 reddittui "${pkgdir}/usr/bin/reddittui"
    install -Dm 0644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
