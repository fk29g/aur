# Maintainer: fk29g <fk29g.uphill912@slmails.com>
pkgname=reddit-tui
pkgver=0.3.8
pkgrel=2
pkgdesc="Terminal UI for Reddit"
arch=("x86_64")
url="https://github.com/tonymajestro/reddit-tui"
license=("MIT")
makedepends=("go>=1.16")
conflicts=("reddit-tui")
provides=("reddit-tui")
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('781241b998cd87e912efd3af4233b1d8e618ab6ab87eb78b062cd1b699b99cb5')

build() {
    cd "$pkgname-$pkgver"
    go build -o reddittui main.go
}

package() {
    cd "$pkgname-$pkgver"
    install -Dm 0755 reddittui "${pkgdir}/usr/bin/reddittui"
    install -Dm 0644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
