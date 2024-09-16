# Maintainer: Tmpstpdwn <tmpstpdwn@tuta.io>
pkgname=ttf2png
pkgver=1.0.r3.05c640c
pkgrel=1
pkgdesc="TTF to PNG Converter"
arch=('x86_64')
url="https://github.com/tmpstpdwn/ttf2png.git"
license=('GPL3')
depends=('binutils' 'imagemagick')
makedepends=('git')
provides=('ttf2png')
source=("git+$url")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  printf "${pkgver}.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  mkdir -p "${pkgdir}"/usr/bin
  cd "$srcdir/$pkgname"
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
  install -Dm755 src/* "${pkgdir}"/usr/bin/
}
