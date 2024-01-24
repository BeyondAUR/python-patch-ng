# Maintainer: Tomislav Ivek <tomislav dot ivek at gmail dot com>

pkgname=python-patch-ng
pkgver=1.17.4
pkgrel=4
pkgdesc='Library to parse and apply unified diffs forked from python-patch.'
arch=('any')
url="https://github.com/conan-io/python-patch/"
license=('MIT')
depends=('python')
makedepends=('python-setuptools')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/conan-io/python-patch-ng/archive/refs/tags/${pkgver}.tar.gz")
b2sums=("78067e3c3d296a21f8fd4155fe770245ba4457cb9e37003f5e7667c30827878a8c06d62c77bb1fdaf61b96a813612a7c39800d7040b13a9d18f0baeccbd86ba1")

build() {
  cd "$srcdir/${pkgname}-${pkgver}"
  python setup.py build
}

package() {
  cd "$srcdir/${pkgname}-${pkgver}"
  python setup.py install --optimize=1 --root "$pkgdir"
  install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
