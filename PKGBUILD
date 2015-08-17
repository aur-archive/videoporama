# Maintainer: boenki <boenki at gmx dot de>
# Contributor: Julien MISCHKOWITZ <wain@archlinux.fr>
# Contributor: Dany Martineau <dany.luc.martineau at gmail.com>

pkgname=videoporama
pkgver=0.8.2
pkgrel=4
pkgdesc="Make image slideshow, export to video file"
arch=('any')
url="http://www.videoporama.tuxfamily.org"
license=('GPL2')
depends=('python2-imaging' 'mplayer' 'sox' 'python2-pyqt' 'pyexiv2' 'libdv' 'ffmpeg')
source=(http://download.tuxfamily.org/$pkgname/src/Videoporama_${pkgver}-1.tar.gz
        $pkgname.desktop)
md5sums=('abb3fd28be723fedafe82a67dbcdeb2b'
         '899eb1a29f51f0f6ca7e5e5e2bd82bd6')

package() {
  cd Videoporama_${pkgver}
  python2 setup.py install --root=$pkgdir
  install -Dm644 ../$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  sed -i "s|python|python2|g" $pkgdir/usr/bin/$pkgname
}