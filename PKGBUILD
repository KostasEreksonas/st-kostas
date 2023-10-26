# Maintainer: Kostas Ereksonas <k.ereksonas@gmail.com>
pkgname='st'
pkgver=1
pkgrel=1
pkgdesc="a simple terminal implementation for X"
arch=('x86_64')
url="https://git.suckless.org/st"
license=('MIT')
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=('package')
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname-$pkgver.tar.gz"
        "$pkgname-$pkgver.patch")
noextract=()
md5sums=()
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
}

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
