# Maintainer: smiley <smiley@smiley.aleeas.com>
_pkgbase=Certipy-5.0.4
pkgname=python-certipy-ad
pkgver=certipy-ad_5_0_4
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
source=("https://github.com/ly4k/Certipy/archive/refs/tags/5.0.4.tar.gz")
sha256sums=('7b1c0dc5a9b285bf5cd4b412c1515329f91122f47d16d711018dd44998409347')

pkgver=5.0.4

build() {
    cd "${srcdir}/${_pkgbase}"
    python -m build --wheel --no-isolation
}

package() {
    cd "${srcdir}/${_pkgbase}"
    python -m installer --destdir="${pkgdir}" dist/*.whl
}
