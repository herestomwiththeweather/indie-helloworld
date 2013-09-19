# Maintainer: http://indieboxproject.org/

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

package() {
# Manifest
    mkdir -p $pkgdir/var/lib/indie-box/manifests
    install -m644 $startdir/indie-box-manifest.json $pkgdir/var/lib/indie-box/manifests/indie-helloworld.json

# Code
    mkdir -p $pkgdir/usr/share/indie-helloworld
    install -m755 $startdir/index.php        $pkgdir/usr/share/indie-helloworld/
}
