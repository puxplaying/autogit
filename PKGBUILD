# Maintainer: Georg Wagner (@puxplaying) <puxplaying@gmail.com>

pkgname=autogit
pkgver=1.6.0
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
sha256sums=('9a98945ea1c9970621df539ea4578dfa7c8cac90c7c29418e5ffce7067ea574a')

package () {
  cd "$pkgname-$pkgver"
  install -Dm755 "$pkgname" -t "$pkgdir/usr/bin/"
  install -Dm644 "$pkgname.conf" -t "$pkgdir/usr/share/$pkgname/"
  cp -r reponames "$pkgdir/usr/share/$pkgname/"
}
