# Maintainer: smiley <smiley@smiley.aleeas.com>
_pkgbase=Certipy-5.0.3
pkgname=python-certipy-ad
pkgver=certipy-ad_5_0_3
pkgrel=1
pkgdesc="Tool for Active Directory Certificate Services enumeration and abuse"
arch=('any')
conflicts=('certipy-ad')
url="https://github.com/ly4k/Certipy"
license=(MIT)
provides=('certipy-ad')
depends=(
    python
    python-asn1crypto
    python-cryptography
    impacket
    python-ldap3
    python-pyasn1
    python-dnspython
    python-pyopenssl
    python-requests
    python-pycryptodome
    python-beautifulsoup4
    python-httpx
    python-argcomplete
)
makedepends=(
    python-build
    python-installer
    python-wheel
)
source=("https://github.com/ly4k/Certipy/archive/refs/tags/5.0.3.tar.gz")
sha256sums=('beb5967d4fff4aeaac7e0e46c7cfd09ce1e816d407a6981fdde923b050cd5ab7')

pkgver=5.0.3

build() {
    cd "${srcdir}/${_pkgbase}"
    python -m build --wheel --no-isolation
}

package() {
    cd "${srcdir}/${_pkgbase}"
    python -m installer --destdir="${pkgdir}" dist/*.whl
}
