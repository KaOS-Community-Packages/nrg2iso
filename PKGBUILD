
pkgname=nrg2iso
pkgver=0.4
pkgrel=1
pkgdesc="Utility for converting CD or DVD image generated by Nero Burning Rom to ISO format"
arch=('x86_64')
url="http://gregory.kokanosky.free.fr/v4/linux/nrg2iso.en.html"
license=('GPL')
depends=('glibc')
source=(http://gregory.kokanosky.free.fr/v4/linux/${pkgname}-${pkgver}.tar.gz)
md5sums=('996c38c8f1465e9c51ccad4f31ec2eee')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}

	sed -i -e 's|gcc|gcc ${CFLAGS}|g' Makefile
	make
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}

	install -D nrg2iso ${pkgdir}/usr/bin/nrg2iso
}

