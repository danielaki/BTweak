# Maintainer:

pkgname=btweak-git
pkgver=1.0.ac279a9
pkgrel=1
pkgdesc="BTweak - Um script simples de ajuste de kernel para sistemas Linux e Android, comprovado por evidências.
arch=('any')
url="https://github.com/danielaki/BTweak.git"
license=('GPL3')
depends=()
makedepends=('git')
source=("$pkgname"::'git+https://github.com/danielaki/btweak')
md5sums=('SKIP')
provides=(btweak)

pkgver() {
  cd "$pkgname"
  echo "1.0.`git rev-parse --short HEAD`"
}

package() {
  cd "$srcdir/${pkgname}/"
  chmod +x ktweak
  mkdir -p "$pkgdir/usr/bin/"
  mkdir -p "$pkgdir/etc/systemd/system/"
  install -Dm744 ktweak "$pkgdir/usr/bin/ktweak"
  install -Dm644 ktweak.service "$pkgdir/etc/systemd/system/ktweak.service"
}
