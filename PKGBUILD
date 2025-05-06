# Maintainer: fk29g <fk29g.uphill912@slmails.com>
# Maintainer: giorgiopapini
pkgname=netdump
pkgver=1.0.0
pkgrel=2
pkgdesc="Network packet analyzer supporting real-time and offline analysis with ASCII visualization"
arch=("x86_64")
url="https://github.com/giorgiopapini/netdump"
license=("GPL-3.0-only")
depends=("libpcap")
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/$pkgver.tar.gz"
        "fix-install-dirs.patch")
sha256sums=('a773e2f2d9aab2c7444886aa23b77371ce4d8ec269af6dc6edb5b071c4c3990d'
            '4ade65fde68dea6f894e75eb7e0a6aa4862776d640cc9643a0e078aa29714320')

prepare() {
    cd "$pkgname-$pkgver"
    patch -p1 < "$srcdir/fix-install-dirs.patch"
}

build() {
    cd "$pkgname-$pkgver"
    make
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir" install
    install -Dm 0644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
