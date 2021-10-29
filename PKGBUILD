# Maintainer: not_anonymous <nmlibertarian@gmail.com>
# Contributor: Emeric Grange <emeric.grange@gmail.com>
# Contributor: Matej Stuchlik <matej.stuchlik at gmail dot com>

pkgname=openrocket-yar
_pkgname=OpenRocket-YAR
pkgver=211027
pkgrel=1
pkgdesc="A free and fully featured rocket flight simulator - 6 degrees of freedom"
arch=('any')
url=https://github.com/yorkaerospace/openrocket
license=('GPL3')
depends=('java-environment=8' 'desktop-file-utils')
replaces=('openrocket')
conflicts=('openrocket')
source=("https://github.com/yorkaerospace/openrocket/releases/download/yar-21.10.27/$_pkgname-$pkgver.jar"
        openrocket.1
	de_debian.tar.gz)
noextract=($_pkgname-$pkgver.jar)

package() {
	cd $srcdir

	install -Dm644 $_pkgname-$pkgver.jar $pkgdir/usr/share/java/openrocket/openrocket.jar
	install -Dm755 openrocket.1 $pkgdir/usr/bin/openrocket

	install -Dm644 de_debian/openrocket.1 $pkgdir/usr/share/man/man1/openrocket.1
	find "$pkgdir/usr/share/man/man1" -name *.1 -exec gzip -9 {} +

	install -Dm644 de_debian/openrocket.desktop $pkgdir/usr/share/applications/openrocket.desktop
	install -Dm644 de_debian/openrocket.xpm $pkgdir/usr/share/pixmaps/openrocket.xpm
}
md5sums=('33330e1287bfeee321d4e6af39b221fe'
         '54eb3c1641feb1eac7d4e4d9e912434a'
         'f8edc554065e121767355936727fc88a')
sha256sums=('40c0526672d7f849d6c71710c8a8772fef4df2663cb922647c38aa3d76c6e3af'
            '74ab605cb11161784d4af96d018eb88adf7a2e4a8b1088a64b94b1e8ec5e18d1'
            '62c4e739f82fa53fdae8a41f12bfb2828b77df89c8f48b1a790192a8e773cb98')
