pkgbase='python-hanziconv'
pkgname=('python-hanziconv')
_module='hanziconv'
pkgver='0.3.2'
pkgrel=1
pkgdesc="Hanzi Converter for Traditional and Simplified Chinese"
url="https://github.com/berniey/hanziconv"
depends=('python')
makedepends=('python-setuptools')
license=('APACHE')
arch=('any')
source=("https://files.pythonhosted.org/packages/source/${_module::1}/$_module/$_module-$pkgver.tar.gz")
sha256sums=('208866da6ae305bca19eb98702b65c93bb3a803b496e4287ca740d68892fc4c4')

build() {
    cd "${srcdir}/${_module}-${pkgver}"
    python setup.py build
}

package() {
    depends+=()
    cd "${srcdir}/${_module}-${pkgver}"
    python setup.py install --root="${pkgdir}" --optimize=1 --skip-build
}
