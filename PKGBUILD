# Maintainer: Georg Wagner (@puxplaying) <puxplaying@gmail.com>

pkgname=autogit
pkgver=0.41
pkgrel=1
pkgdesc="Auto build, update, install PKGBUILDS from Github, Gitlab and AUR"
arch=(any)
url="https://github.com/puxplaying/autogit"
license=('GPL3')
depends=('pacman' 'sudo' 'bash' 'curl')
makedepends=('git')
optdepends=('manjaro-tools-pkg: Needed for Manjaro clean chroot package building')
source=("$url/archive/$pkgver.tar.gz")
md5sums=('SKIP')

package () {
	cd "$srcdir/$pkgname-$pkgver"
	install -Dm755 "$srcdir/$pkgname-$pkgver/autogit" "$pkgdir/usr/bin/autogit"
	mkdir -p $pkgdir/usr/share/autogit/reponames
	cp -r reponames/ $pkgdir/usr/share/autogit/
	cp -r autogit.conf $pkgdir/usr/share/autogit/
}
