# Maintainer: fk29g <fk29g.uphill912@slmails.com>
pkgname=firefox-extension-skip-redirect
pkgver=2.3.6
pkgrel=1
pkgdesc="Skip intermediary pages that some pages use before redirecting to a final page"
arch=("any")
url="https://github.com/sblask-webextensions/webextension-skip-redirect"
license=("MIT")
grups=("firefox-addons")
depends=("firefox")
makedepends=("npm" "moreutils")
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/${pkgver}.tar.gz")
noextract=("$pkgname-$pkgver.tar.gz")
sha256sums=("1008c461ff2d6e5903db562d9508ce297f91016eaffc2279a6ee770cfd96a50d")

prepare() {
    mkdir -p "$pkgname-$pkgver"
    tar -xf "$pkgname-$pkgver.tar.gz" -C "$pkgname-$pkgver" --strip-components=1
    cd $pkgname-$pkgver
    npm install
}

build() {
    cd "$pkgname-$pkgver"
	npm run artifact-create:firefox
}

package() {
    cd "$pkgname-$pkgver"
    install -Dm 0644 skip_redirect-$pkgver.zip "$pkgdir/usr/lib/firefox/browser/extensions/skipredirect@sblask.xpi"
}
