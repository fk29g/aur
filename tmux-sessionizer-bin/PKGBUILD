# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=tmux-sessionizer
pkgname=$_projectname-bin
pkgver=0.4.5
pkgrel=3
pkgdesc="A tool for opening git repositories as tmux sessions"
arch=("x86_64")
url="https://github.com/jrmoulton/tmux-sessionizer"
license=("MIT")
depends=("tmux")
provides=("$_projectname")
conflicts=("$_projectname")
source=("$pkgname-$pkgver.tar.gz::$url/releases/download/v$pkgver/$_projectname-x86_64-unknown-linux-gnu.tar.xz")
b2sums=("5624559415f495965fa6600794bffcbb6c78753fe314b3aa93e12cd5cc365cee79488c44ea9bc1ec0df01fb12d24d68cf24fcd7bfcf4cb65fbf623753c3337b7")

package() {
    cd "tmux-sessionizer-x86_64-unknown-linux-gnu"
    install -Dm 0755 tms $pkgdir/usr/bin/tms
    install -Dm 0644 LICENSE $pkgdir/usr/share/licenses/${_projectname}/LICENSE
}
