# Maintainer: Alexander Wenzel <elkangaroo@gmail.com>
pkgname=glue
pkgver=0.3
pkgrel=1
pkgdesc='A simple command line tool to generate CSS sprites'
arch=('any')
url='https://github.com/jorgebastida/glue/'
license=('BSD')
depends=('python2' 'python2-pillow')
makedepends=('python2-distribute')
optdepends=('optipng: optimize the output PNG files')
options=(!emptydirs)
source=("https://pypi.python.org/packages/source/g/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('56ea951568a5af3c6a4d0d3a0727cddf')
#source=("https://github.com/jorgebastida/$pkgname/archive/$pkgver.zip")
#md5sums=('ce0037ea125824d3b21e56ec69a9dc4e')

package() {
  cd "$srcdir/$pkgname-$pkgver"

	install -D -m644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"

	python2 setup.py install --root="$pkgdir/" --optimize=1
}
