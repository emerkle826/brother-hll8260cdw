# Maintainer: Mio Iwakura <mio dot iwakura at gmail dot com>
pkgname="brother-hll8260cdw"
pkgver=1.4.0
pkgrel=1
_lprpkgver=1.3.0
pkgdesc="Brother HL-L8260CDW CUPS driver"
arch=('i686' 'x86_64')
url="http://brother.com"
license=('GPL')
depends=('cups' 'ghostscript')
depends_x86_64=('lib32-glibc')
source=("http://download.brother.com/welcome/dlf103210/hll8260cdwlpr-${_lprpkgver}-0.i386.rpm"
        "http://download.brother.com/welcome/dlf103219/hll8260cdwcupswrapper-${pkgver}-0.i386.rpm")
sha256sums=('af6192f22f9b8bd0b6cbc11619fa6052c7dd3697af97eb9697249b7b506c5318'
            'd69a65182fe3077d67a6e64b8ef424410d99a68560d62251e7ebc91cfa01c7c8')
package() {
    cp -a "$srcdir/usr" "$pkgdir"
    cp -a "$srcdir/opt" "$pkgdir"
    mkdir -p "$pkgdir/usr/lib/cups/filter"
    cd "$pkgdir/usr/lib/cups/filter"
    ln -s /opt/brother/Printers/hll8260cdw/cupswrapper/brother_lpdwrapper_hll8260cdw .
}
