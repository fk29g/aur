# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=meow
pkgname=$_projectname-nvim
pkgver=1.0.1
pkgrel=1
pkgdesc="cat alternative using Neovim for highlighting and configuration"
arch=("x86_64")
url="https://github.com/datsfilipe/$_projectname"
license=("MIT")
depends=("neovim")
makedepends=("rust")
source=("$_projectname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
b2sums=("5e8dac71b8f44c589f1b971dfbbec9cf50d62a55d8a26dc37cb2c1e3d9e02d007bc4b4f0d3dd0f04e9503e96566b8e71433866aa3632757a78ab7641d64dadc2")

build() {
    cd "$_projectname-$pkgver"
    cargo build --release
}

package() {
    cd "$_projectname-$pkgver"
    install -Dm 0755 target/release/meow "$pkgdir/usr/bin/meow"
    install -Dm 0644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
