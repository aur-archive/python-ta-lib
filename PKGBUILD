# Maintainer: perlawk

pkgname=python-ta-lib
pkgver=0.4
pkgrel=1
pkgdesc='python wrapper of talib'
arch=('any')
url="https://github.com/mrjbq7/ta-lib"
license=('custom:public domain')
depends=('cython' 'ta-lib')
makedepends=(git)

prepare() {
  if [ ! -e "$srcdir"/ta-lib ] ; then
    git clone https://github.com/mrjbq7/ta-lib.git
  fi
}

build() {
  cd "$srcdir/ta-lib"
  python setup.py build 
}

package() {
  cd "$srcdir/ta-lib"
  python setup.py install --root="$pkgdir" --optimize=1
}

