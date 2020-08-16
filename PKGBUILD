# Maintainer:Thomas Leon Highbaugh <thighbaugh@zoho.com>
pkgname=st-tlh-git
pkgver=0.8.5.r8.e63a45c
pkgrel=1
pkgdesc="A patched, themed build of st (the Suckless simple terminal) from tlh based on Derek Taylor's ST."
arch=(x86_64 i686)
url="https://github.com/Thomashighbaugh/st-tlh.git"
license=('MIT')
groups=('System')
depends=(ttf-hack ttf-joypixels)
makedepends=(git)
checkdepends=()
optdepends=()
provides=(st)
conflicts=(st)
replaces=()
backup=()
options=()
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
  cd "${_pkgname}"
  printf "0.8.5.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd st-tlh
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  cd st-tlh  
  mkdir -p ${pkgdir}/opt/${pkgname}
  cp -rf * ${pkgdir}/opt/${pkgname}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
}

