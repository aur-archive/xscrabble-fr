# Maintainer: jsteel <mail at jsteel dot org>
# Contributor: Anton Bazhenov <anton.bazhenov at gmail>
# Contributor: danym <dany.luc.martineau at gmail dot com>

pkgname=xscrabble-fr
pkgver=1.0
pkgrel=3
pkgdesc="French language files for XScrabble"
arch=('any')
url="http://www.happypenguin.org/show?XScrabble"
license=('custom:unknown')
depends=('xscrabble')
source=(ftp://ftp.ac-grenoble.fr/ge/educational_games/xscrabble_fr.tar.bz2)
md5sums=('1656a136583db35169a785a68a8a8420')

build() {
  cd "$srcdir"/${pkgname/-/_}

  sed -i "s_/usr/share/games/scrabble_/usr/share/xscrabble_" app-defaults/XScrabble_fr
}

package() {
  cd "$srcdir"/${pkgname/-/_}

  install -dm755 "$pkgdir"/usr/share/xscrabble/fr
  install -m644 lib/* "$pkgdir"/usr/share/xscrabble/fr/
  install -Dm644 app-defaults/XScrabble_fr "$pkgdir"/usr/share/X11/app-defaults/XScrabble_fr
}
