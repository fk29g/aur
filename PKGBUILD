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
b2sums=('b39df369573cac821859d6c3cdfd09b4ea23aebc3f9da7eca78fbbb665d5e9dfb0b96ca2c9d2fa7d626d192b6a5d40e571ad8511bd056a35959e26c9056bd8f4')

package() {
    install -Dm 0755 reddittui "${pkgdir}/usr/bin/reddittui"
    install -Dm 0644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
    install -Dm 0644 README.md "${pkgdir}/usr/share/doc/${_projectname}/README.md"
}
