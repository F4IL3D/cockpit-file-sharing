pkgname=cockpit-file-sharing
pkgver=2.4.5
pkgrel=1
pkgdesc="A Cockpit plugin to easily manage samba and NFS file sharing"
arch=('any')
url="https://github.com/45Drives/cockpit-file-sharing"
license=('GPL3')
depends=('cockpit' 'samba' 'python' 'nfs-utils')
source=("https://github.com/45Drives/cockpit-file-sharing/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('df059152fc3d103cb93ef7870a42c76d31b0fd5a2f884465b3fd47f74b2cf03c')

package() {
  install -dm755 "$pkgdir"/usr/share/cockpit/file-sharing

  for file in $(find "$srcdir/$pkgname-$pkgver/file-sharing/" -type f ); do
    install -Dm644 "$file" "$pkgdir"/usr/share/cockpit/file-sharing/;
  done
}
