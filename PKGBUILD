# Maintainer: Fera Maxwell <kiziltasenes44@gmail.com>
pkgname=deskgen
pkgver=1.0
pkgrel=1
pkgdesc="Universal .desktop file generator (Python3 + PyQt6)"
arch=('any')
url="https://github.com/Fera-Maxwell/deskgen"
license=('GPL')
depends=('python' 'python-pyqt6')
source=("https://raw.githubusercontent.com/Fera-Maxwell/deskgen/main/deskgen")
sha256sums=('SKIP')

package() {
    # Install the executable in /usr/bin
    install -Dm755 "$srcdir/deskgen" "$pkgdir/usr/bin/deskgen"

    # Install a .desktop file for menu integration
    mkdir -p "$pkgdir/usr/share/applications"
    cat > "$pkgdir/usr/share/applications/deskgen.desktop" << EOF
[Desktop Entry]
Name=Desk-gen
Comment=Universal .desktop file generator
Exec=/usr/bin/deskgen
Type=Application
Terminal=false
Categories=Utility;
EOF
}
