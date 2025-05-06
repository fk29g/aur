# Maintainer: fk29g <fk29g.uphill912@slmails.com>
pkgname=firefox-extension-refined-github-bin
pkgver=25.4.8
pkgrel=1
pkgdesc="Simplifies the GitHub interface and adds many useful features"
arch=("any")
url="https://addons.mozilla.org/addon/refined-github-/"
license=("MIT")
groups=("firefox-addons")
depends=("firefox>=126.0")
install="$pkgname.install"
source=("$pkgname-$pkgver.xpi::https://addons.mozilla.org/firefox/downloads/file/4470107/refined_github-$pkgver.xpi"
        "add-id.patch")
noextract=("$pkgname-$pkgver.xpi")
sha256sums=("4e07f83622497c5ea1e2fb39f94d910233cdf467a562df4b37dc39adea6fba47"
            "748b64c23a8e78904fd1b6dc26f7f74d8e8ac9a2a2ee070f4343f01cc82c2c41")

prepare() {
    mkdir "$pkgname-$pkgver"
    bsdtar -xf "$pkgname-$pkgver.xpi" -C "$pkgname-$pkgver"
    cd "$pkgname-$pkgver"
    patch -p1 < "$srcdir/add-id.patch"
    zip -r "$pkgname-$pkgver.xpi" ./*
}

package() {
    cd $pkgname-$pkgver
    install -Dm 0644 "$pkgname-$pkgver.xpi" "$pkgdir/usr/lib/firefox/browser/extensions/addon@refined-github.xpi"
}
