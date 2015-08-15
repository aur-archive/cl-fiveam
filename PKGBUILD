# Maintainer: DavidK <david_king at softhome dot net>

pkgname=cl-fiveam
pkgver=1.2
pkgrel=1
pkgdesc="Simple regression testing framework for Common Lisp"
arch=('any')
url="http://common-lisp.net/project/fiveam"
license=('custom')
depends=('common-lisp' 'cl-alexandria')
install=cl-fiveam.install
_clname=fiveam
source=("${url}/files/${_clname}-${pkgver}.tar.gz")
md5sums=('1d20bfa19c7615caf4054dce7a117865')

package() {
    cd "${srcdir}"/${_clname}-${pkgver}
    install -d "${pkgdir}"/usr/share/common-lisp/source/${_clname}
    install -d "${pkgdir}"/usr/share/common-lisp/source/${_clname}/src
    install -d "${pkgdir}"/usr/share/common-lisp/source/${_clname}/t
    install -d "${pkgdir}"/usr/share/common-lisp/systems
    install -d "${pkgdir}"/usr/share/licenses/${pkgname}

    install -m 644 -t "${pkgdir}"/usr/share/common-lisp/source/${_clname}/src src/*.lisp
    install -m 644 -t "${pkgdir}"/usr/share/common-lisp/source/${_clname}/t t/*.lisp
    install -m 644 -t "${pkgdir}"/usr/share/common-lisp/source/${_clname} *.asd
    install -m 644 -t "${pkgdir}"/usr/share/common-lisp/source/${_clname} version.lisp-expr
    install -m 644 -T COPYING "${pkgdir}"/usr/share/licenses/${pkgname}/LICENSE

    cd "${pkgdir}"/usr/share/common-lisp/systems
    ln -s ../source/${_clname}/${_clname}.asd .
}

# vim:set ts=2 sw=4 et nospell:
