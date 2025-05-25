# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=reddit-tui
pkgname=$_projectname-bin
pkgver=0.3.8
pkgrel=1
pkgdesc="Terminal UI for Reddit"
arch=("x86_64")
url="https://github.com/tonymajestro/reddit-tui"
license=("MIT")
provides=("reddit-tui")
conflicts=("reddit-tui")
source=("$_projectname-$pkgver.tar.gz::$url/releases/download/v$pkgver/${_projectname}_Linux_x86_64.tar.gz")
sha256sums=('SKIP')

package() {
    install -Dm 0755 reddittui "${pkgdir}/usr/bin/reddittui"
    install -Dm 0644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
    install -Dm 0644 README.md "${pkgdir}/usr/share/doc/${_projectname}/README.md"
}
