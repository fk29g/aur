# Maintainer: fk29g <fk29g.uphill912@slmails.com>
_projectname=podman-tui
pkgname=$_projectname-bin
pkgver=1.6.0
pkgrel=1
pkgdesc="Podman Terminal UI"
arch=("x86_64")
url="https://github.com/containers/podman-tui"
license=("Apache-2.0")
provides=("$_projectname")
conflicts=("$_projectname")
source=("$_projectname-$pkgver.zip::$url/releases/download/v$pkgver/${_projectname}-release-linux_amd64.zip"
        "$_projectname-LICENSE::https://raw.githubusercontent.com/containers/podman-tui/refs/tags/v$pkgver/LICENSE"
        "$_projectname-README::https://raw.githubusercontent.com/containers/podman-tui/refs/tags/v$pkgver/docs/README.md"
        "$_projectname-install::https://raw.githubusercontent.com/containers/podman-tui/refs/tags/v$pkgver/docs/install.md")
b2sums=('3c17059d0475c3613f69a62fb32205748b23cd920fb5fdefdf4a3bb63b2f4a28ddbe800cff2bb1b779feae4148b6269a9f029fca03745efa04a36e1648e7ae67'
        '43452dd4216bba835bff542c02fcd0a80b77fef97a6f1042adcbbbcf312bb856b0707c35b2f1af356e0b4262e501a159f06bf1f947f182d0023cdd4aefbd8a85'
        'cef3fb0a613eadcabead86a00c809426f16400fda46ba19dde5d1d295606ea5b38a1fe834ded2e166c55bf2bcf170da4c2b707170a089d2176fcbda5230442b2'
        'b1d270a0ff93296c05925d6a0a0777336d8e6547733b5fa81256113e9cfaee76b3ab7c6cb3ca74a03e5cd30e155ceb6cc95486efb48f2e07218c290f5ea4b2a0')

package() {
    install -Dm 644 "$_projectname-LICENSE" "$pkgdir/usr/share/licenses/$_projectname/LICENSE.md"
    install -Dm 644 "$_projectname-README" "$pkgdir/usr/share/doc/$_projectname/README.md"
    install -Dm 644 "$_projectname-install" "$pkgdir/usr/share/doc/$_projectname/install.md"
    cd "$_projectname-release-linux_amd64/$_projectname-$pkgver"
    install -Dm 755 "$_projectname" "$pkgdir/usr/bin/$_projectname"
}
