pkgname=parsley-git
pkgver=d83692a
pkgrel=1
pkgdesc=""
arch=('any')
url="https://github.com/python-parsley/parsley"
license=('MIT')
depends=('python2')
makedepends=('git' 'python2-setuptools')
source=("$pkgname"::git://github.com/python-parsley/parsley.git)
md5sums=('SKIP')

pkgver() {
  cd "$pkgname"
  local ver=$(git describe --always)
  printf "%s\n" "${ver//-/.}"
}

package() {
  cd "$pkgname"
  python2 setup.py install --root=$pkgdir
}

# vim:set ts=2 sw=2 et:
