# Maintainer: Tony Crisci <tony@dubstepdish.com>
pkgname=i3ipc-glib
pkgver=0.5.0
pkgrel=1
epoch=
pkgdesc="A C interface library to i3wm"
arch=('i686' 'x86_64')
url="https://github.com/acrisci/i3ipc-glib"
license=('GPL3')
groups=()
depends=('libxcb' 'json-glib')
makedepends=()
checkdepends=()
optdepends=('i3ipc-lua: Lua language bindings'
            'i3ipc-python: Python language bindings'
            'i3ipc-gjs: JavaScript language bindings')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/acrisci/i3ipc-glib/releases/download/v${pkgver}/i3ipc-${pkgver}.tar.gz")
noextract=()
md5sums=("778691469d9e28d26856e99bc029dcb1")

build() {
    cd "$srcdir/i3ipc-$pkgver"
    ./configure --prefix=/usr
    make
}

package() {
    cd "$srcdir/i3ipc-$pkgver"
	make DESTDIR="$pkgdir/" install
}
