# Maintainer: Georg Wagner (@puxplaying) <puxplaying@gmail.com>

pkgname=autogit
pkgver=1.7.4
pkgrel=1
pkgdesc="Auto build, update, install PKGBUILDS from Github, Gitlab and AUR"
arch=('any')
url="https://github.com/puxplaying/autogit"
license=('GPL3')
depends=('pacman' 'sudo' 'bash' 'curl' 'fzf')
makedepends=('git')
optdepends=('manjaro-tools-pkg: Needed for Manjaro clean chroot package building'
            'manjaro-chrootbuild: Needed for Manjaro clean chroot package building')
backup=(etc/autogit/autogit.conf)
source=("$pkgname-$pkgver.tar.gz::$url/archive/$pkgver.tar.gz")
sha256sums=('f7a748a47b7c8fe58ec536c484a57dedbc30ef9cdc1834301b7aec81afb30883')

package () {
  cd "$pkgname-$pkgver"
  install -Dm755 "$pkgname" -t "$pkgdir/usr/bin/"
  install -Dm644 "$pkgname.conf" -t "$pkgdir/etc/$pkgname/"
  cp -r reponames "$pkgdir/etc/$pkgname/"
}
