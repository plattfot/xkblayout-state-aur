# Maintainer: Fredrik Salomonsson <plattfot@gmail.com>
pkgname=xkblayout-state-git
pkgver=v1b.r6.gc5e17d2
pkgrel=1
epoch=
pkgdesc="A small command-line program to get/set the current XKB keyboard layout."
arch=('x86_64')
url="https://github.com/nonpop/xkblayout-state"
license=('GPL2')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname-$pkgver::git+https://github.com/nonpop/xkblayout-state.git")
noextract=()
md5sums=('SKIP') #generate with 'makepkg -g'

pkgver() {
  cd "$pkgname-$pkgver"
  git describe --long | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

build() {
	cd "$pkgname-$pkgver"
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	mkdir -p $pkgdir/usr/bin
	cp xkblayout-state $pkgdir/usr/bin/
}
