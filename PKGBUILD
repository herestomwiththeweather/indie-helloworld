_developer=http://indieboxproject.org/
_maintainer=$_developer
pkgname=indie-helloworld
pkgver=0.1
pkgrel=1
pkgdesc="Hello World"
arch=('any')
url="http://indieboxproject.org/"
license=('GPL')
groups=()
depends=()
backup=()
source=()
options=('!strip')
md5sums=('76ef522124a23e3d65fe65de00ae487a')
_parameterize=$(cat <<END
    s!##pkgname##!$pkgname!g;
    s!##pkgdesc##!$pkgdesc!g;
    s!##developer##!$_developer!g;
    s!##maintainer##!$_maintainer!g;
    s!##pkgver##!$pkgver!g;
    s!##pkgrel##!$pkgrel!g;
    s!##license##!$license!g;
END
)
package() {
# Manifest
    mkdir -p $pkgdir/var/lib/indie-box/manifests
    perl -pe "$_parameterize" $startdir/indie-box-manifest.json > $pkgdir/var/lib/indie-box/manifests/indie-helloworld.json
    chmod 0644 $pkgdir/var/lib/indie-box/manifests/indie-helloworld.json

# Code
    mkdir -p $pkgdir/usr/share/indie-helloworld
    install -m755 $startdir/index.php $pkgdir/usr/share/indie-helloworld/
}
