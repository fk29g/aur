# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=clidle
pkgname=$_projectname-bin
pkgver=0.1.0
pkgrel=1
pkgdesc="Play Wordle from your terminal"
arch=("x86_64")
url="https://github.com/ajeetdsouza/clidle"
license=("MIT")
makedepends=("go")
provides=("clidle")
conflicts=("clidle")
source=("$pkgname-$pkgver.tar.gz::$url/releases/download/v$pkgver/clidle_Linux_x86_64.tar.gz")
b2sums=("SKIP")

package() {
    install -Dm 0755 clidle "$pkgdir/usr/bin/clidle"
    install -Dm 0644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
