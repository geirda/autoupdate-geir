# Maintainer: Geir Damstuen
pkgname="autoupdate-geir"
pkgver=0.1
pkgrel=1
pkgdesc="Checks for updates and stores the number in a file"
url="https://github.com/geirda/autoupdate-geir.git"
arch=('i686' 'x86_64')
license=('GPL')
depends=('pacman-contrib' 'checkupdates-aur')
provides=(autoupdate-geir)
conflicts=(autoupdate)
source=("git+$url")
md5sums=('SKIP')

prepare() {
	cd "$srcdir/$pkgname"
}

build() {
	cd "$srcdir/$pkgname"
}

package() {
	cd "$srcdir/$pkgname"
	install -Dm640 "${srcdir}/${pkgname}/autoupdate.service" "$pkgdir/etc/systemd/system/autoupdate.service"
	install -Dm640 "${srcdir}/${pkgname}/autoupdate.timer" "$pkgdir/etc/systemd/system/autoupdate.timer"
	install -Dm644 "${srcdir}/${pkgname}/refreshupdates.hook" "$pkgdir/etc/pacman.d/hooks/refreshupdates.hook"
	install -Dm755 "${srcdir}/${pkgname}/logupdates.sh" "$pkgdir/usr/bin/logupdates.sh"
}
