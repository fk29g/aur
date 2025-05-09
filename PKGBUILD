# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=exdupe
pkgname=exdupe-bin
pkgver=2.1.0
pkgrel=1
arch=("x86_64")
pkgdesc="Fast file archiver that supports data deduplication and differential backups"
url="https://github.com/rrrlasse/$_projectname"
license=("unknown")
source=("$pkgname-$pkgver.tar.gz::$url/releases/download/v${pkgver}/${_projectname}_${pkgver}_linux_amd64.tar.gz")
b2sums=('e582808c1ac91af738f3ae1b583504414342ffbd57cd399f5bcf16b3490650dcfd738e8235f08cc9f1621107be824c1a2c7b8b2b238a507168898aecba6da617')

package() {
    install -Dm 0755 exdupe "$pkgdir/usr/bin/exdupe"
}
