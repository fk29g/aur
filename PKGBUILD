# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=hours
pkgname=$_projectname-bin
pkgver=0.5.0
pkgrel=1
pkgdesc="A no-frills time tracking toolkit for command line nerds"
arch=("x86_64")
url="https://github.com/dhth/hours"
license=("MIT")
provides=("hours")
conflicts=("hours")
source=("$pkgname-$pkgver.tar.gz::$url/releases/download/v$pkgver/${_projectname}_${pkgver}_linux_amd64.tar.gz")
b2sums=('7e6fb8579982d08ff9513f233250bdd3271ff364b14c7e56eea76c4eb3a696c4957b9fba43b4ca77759485ea509523f4932656f12be3c50f514f78638832bf2c')

package() {
    install -Dm 755 $_projectname "$pkgdir/usr/bin/$_projectname"
    install -Dm 644 LICENSE "$pkgdir/usr/share/licenses/$_projectname/LICENSE"
    install -Dm 644 README.md "$pkgdir/usr/share/doc/$_projectname/README.md"
}
