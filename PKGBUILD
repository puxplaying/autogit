# Maintainer: puxplaying

pkgname=autogit
pkgver=0.13
pkgrel=1
pkgdesc="Auto build/maintain or install/update git PKGBUILDS"
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
	#install -Dm644 "update.desktop" "$pkgdir/usr/share/applications/update.desktop"
	#install -Dm644 "update.png" "$pkgdir/usr/share/pixmaps/update.png"
	install -Dm755 "$srcdir/$pkgname-$pkgver/autogit" "$pkgdir/usr/bin/autogit"
	cp -r $srcdir/$pkgname-$pkgver/reponames $pkgdir/usr/share/autogit/reponames/ 
	cp -r $srcdir/$pkgname-$pkgver/autogit.conf $pkgdir/usr/share/autogit/
}
