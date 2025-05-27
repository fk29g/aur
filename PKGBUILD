# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=motus
pkgname=$_projectname-bin
pkgver=0.3.1
pkgrel=1
pkgdesc="A dead simple password generator"
arch=("x86_64")
url="https://github.com/oleiade/motus"
license=("AGPL-3.0-only")
provides=($_projectname)
conflicts=($_projectname)
source=("$pkgname-$pkgver.tar.gz::$url/releases/download/v$pkgver/${_projectname}_${pkgver}_linux_amd64.tar.gz")
sha256sums=('d01a40d440cf7f938af28f6e4fe87190e04cf4cf656b5405d22d26b814b800ea')

package() {
    install -Dm 0755 motus "$pkgdir/usr/bin/motus"
    install -Dm 0644 LICENSE "$pkgdir/usr/share/licenses/$_projectname/LICENSE"
    install -Dm 0644 README.md "$pkgdir/usr/share/doc/$_projectname/README.md"
}
