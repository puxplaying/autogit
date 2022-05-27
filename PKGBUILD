# Maintainer: Georg Wagner (@puxplaying) <puxplaying@gmail.com>

pkgname=autogit
pkgver=1.7.3
pkgrel=1
pkgdesc="Auto build, update, install PKGBUILDS from Github, Gitlab and AUR"
arch=('any')
url="https://github.com/puxplaying/autogit"
license=('GPL3')
depends=('pacman' 'sudo' 'bash' 'curl' 'fzf')
makedepends=('git')
optdepends=('manjaro-tools-pkg: Needed for Manjaro clean chroot package building'
            'manjaro-chrootbuild: Needed for Manjaro clean chroot package building')
source=("$pkgname-$pkgver.tar.gz::$url/archive/$pkgver.tar.gz")
sha256sums=('4d26d4535b132a733e2f785cd641fc28a605005219f437cc3b16241822afc623')

package () {
  backup=(etc/autogit/autogit.conf)
  cd "$pkgname-$pkgver"
  install -Dm755 "$pkgname" -t "$pkgdir/usr/bin/"
  install -Dm644 "$pkgname.conf" -t "$pkgdir/etc/$pkgname/"
  cp -r reponames "$pkgdir/etc/$pkgname/"
}
