# Maintainer: puxplaying

pkgname=autogit
pkgver=0.4
pkgrel=1
_pkgdir=$HOME/autogit
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
	if [ -e "$_pkgdir" ]
		then
			echo "local config found"
		else
			mkdir -p $_pkgdir
		cp -r $srcdir/$pkgname-$pkgver/reponames $_pkgdir/reponames/ 
		cp -r $srcdir/$pkgname-$pkgver/autogit.config $_pkgdir/
	fi
}
