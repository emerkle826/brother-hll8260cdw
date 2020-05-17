# Maintainer: Mio Iwakura <mio dot iwakura at gmail dot com>
pkgname="brother-hll8260cdw"
pkgver=1.5.0
pkgrel=1
_lprpkgver=1.5.0
pkgdesc="Brother HL-L8260CDW CUPS driver"
arch=('i686' 'x86_64')
url="http://brother.com"
license=('GPL')
depends=('cups' 'ghostscript')
depends_x86_64=('lib32-glibc')
source=("http://download.brother.com/welcome/dlf103210/hll8260cdwlpr-${_lprpkgver}-0.i386.rpm"
        "http://download.brother.com/welcome/dlf103219/hll8260cdwcupswrapper-${pkgver}-0.i386.rpm")
sha256sums=('3d0f4211329d005bae5d0cb0be112af8cbb5a1bd975db26ff8ed50aeeb8236fb'
            '35558b77e743dddf8929b6019cb4954718c96eec1b64963aa67a08075cf8cd9e')
package() {
    cp -a "$srcdir/opt" "$pkgdir"
    mkdir -p "$pkgdir/usr/lib/cups/filter"
    cd "$pkgdir/usr/lib/cups/filter"
    ln -s /opt/brother/Printers/hll8260cdw/cupswrapper/brother_lpdwrapper_hll8260cdw .
    mkdir -p "$pkgdir/usr/bin"
    cd "$pkgdir/usr/bin"
    ln -s /opt/brother/Printers/hll8260cdw/lpd/$CARCH/brprintconf_hll8260cdw .
    cd "$pkgdir/opt/brother/Printers/hll8260cdw/lpd"
    ln -s /opt/brother/Printers/hll8260cdw/lpd/$CARCH/brhll8260cdwfilter .
}
