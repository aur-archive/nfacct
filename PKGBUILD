# Maintainer: Alessandro Sagratini <ale_sagra@hotmail.com>
pkgname=nfacct
pkgver=1.0.0
pkgrel=1
pkgdesc="Command line tool to create/retrieve/delete accounting objects."
arch=('i686' 'x86_64')
url="http://www.netfilter.org/projects/nfacct/index.html"
license=('GPL')
depends=('libnetfilter_acct')
options=(!libtool)
source=(http://www.netfilter.org/projects/$pkgname/files/$pkgname-$pkgver.tar.bz2)
md5sums=('5f5cc14c4dfb57f478f1b0348a31034b')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

check() {
  cd "$srcdir/$pkgname-$pkgver"
  make -k check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
