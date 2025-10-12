# Maintainer: Satyam Jha <satyam_jha at zohomail dot in>
# Maintainer: Harsh Narayan Jha <harshnj at proton dot me>
pkgname=ulaa-browser-bin
_pkgname=Ulaa-Browser
pkgver=2.36.2
pkgrel=1
pkgdesc="An ad-free privacy first browser with minimal design bundled with sophisticated technology to make browsing experience smoother, safer, and secure."
arch=(x86_64)
url="https://ulaa.com"
license=()
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=(ulaa-browser-stable)
conflicts=(ulaa-browser ulaa-bin)
replaces=()
backup=()
options=(!debug)
install=
changelog=CHANGELOG
source_x86_64=(${_pkgname}-v${pkgver}-${pkgrel}.deb::https://downloads.zohocdn.com/ulaa-browser/release/linux/stable/${_pkgname}-v${pkgver}-amd64.deb)
noextract=()
sha256sums_x86_64=('9fcfb050e492aceffff1c2257d61f94d4275bc2c651ae396e4a879e2187ab972')
validpgpkeys=()

prepare() {
  ar x "${srcdir}/${_pkgname}-v${pkgver}-${pkgrel}.deb"
  tar -xvf data.tar.xz
}

package() {
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_16.png "${pkgdir}/usr/share/icons/hicolor/16x16/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_24.png "${pkgdir}/usr/share/icons/hicolor/24x24/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_32.png "${pkgdir}/usr/share/icons/hicolor/32x32/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_48.png "${pkgdir}/usr/share/icons/hicolor/48x48/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_64.png "${pkgdir}/usr/share/icons/hicolor/64x64/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_128.png "${pkgdir}/usr/share/icons/hicolor/128x128/apps/ulaa-browser.png"
    install -Dm755 ./opt/zoho.com/ulaa/product_logo_256.png "${pkgdir}/usr/share/icons/hicolor/256x256/apps/ulaa-browser.png"

    cp -ra ./opt ./usr ./etc "${pkgdir}"
}
