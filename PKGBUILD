pkgname=gnome-breeze-git
pkgver=r69.3cb67a6-1
pkgrel=1
pkgdesc="A GTK theme created to match with the new Plasma 5 Breeze."
arch=('any')
url="https://github.com/dirruk1/gnome-breeze"
license=('LGPL')
optdepends=("gtk2: GTK+2 theme" "gtk3: GTK+3 theme")
makedepends=('git')
conflicts=('gtk-theme-breezy-gtk3' 'gtk-theme-breezy-gtk2' ' gtk-theme-breezy')
source=(gnome-breeze::"git+https://github.com/dirruk1/gnome-breeze.git")
sha512sums=('SKIP')

prepare() {
pkgver
}

pkgver() {
    cd "gnome-breeze"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "gnome-breeze"
    find Breeze* -type f -exec install -Dm644 '{}' "$pkgdir/usr/share/themes/{}" \;
}
