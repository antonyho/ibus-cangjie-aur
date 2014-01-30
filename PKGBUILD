# Maintainer: Antony Ho <ntonyworkshop@gmail.com>
pkgname=ibus-cangjie
pkgver=2.0
pkgrel=1
pkgdesc="This is an IBus engine for users of the Cangjie and Quick input methods."
arch=('x86_64' 'i686')
url="http://cangjians.github.io/projects/ibus-cangjie/"
license=('GPL3')
depends=('ibus>=1.4' 'pycangjie>=1.0' 'python>=3.2' 'python-gobject')
conflicts=()
makedepends=('intltool')
replaces=('ibus-cangjie-git')
sha256sums=('55118065749ebe633b012509096896e69126382d75fc56dafc2e57eea0e1a8d6')
source=("http://cangjians.github.io/downloads/ibus-cangjie/$pkgname-$pkgver.tar.xz")

check () {
  cd "$srcdir/$pkgname-$pkgver"
  make check
}

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
