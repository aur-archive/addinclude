# Maintainer: Alexander R�dseth <rodseth@gmail.com>
pkgname=addinclude
pkgver=0.9
pkgrel=3
pkgdesc="A utility to easily add includes to C header- and sourcefiles"
arch=('x86_64' 'i686')
url="http://addinclude.roboticoverlords.org/"
license=('GPL')
makedepends=('go')
source=("http://$pkgname.roboticoverlords.org/$pkgname-$pkgver.tbz2")
md5sums=('18bf5f4627606c8da5843a6d89b318ab')
options=(!strip)

build() {
  cd "$srcdir/$pkgname-$pkgver"

  msg2 "Compiling..."
  make || GOROOT=/usr/lib/go make
  install -Dm755 "$pkgname" \
    "$pkgdir/usr/bin/$pkgname"

  msg2 "Packaging..."
  install -Dm644 "$pkgname.1.gz" \
    "$pkgdir/usr/share/man/man1/$pkgname.1.gz"
  install -Dm644 COPYING \
    "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
# vim:set ts=2 sw=2 et:
