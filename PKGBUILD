# Maintainer: Carl Mueller  archlinux at carlm e4ward com

pkgname=kdeplasma-applets-gmail-notifier
pkgver=0.2.2
pkgrel=2
pkgdesc="Gmail notifier"
arch=(i686 x86_64)
url="http://www.kde-look.org/content/show.php/gmail+notifier?content=153658"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=(http://kde-look.org/CONTENT/content-files/153658-gmailnotifier-keluoinhac-0.2.2.tar.gz)
md5sums=('b4ee0ddd0c8e47f9c305fcf36631164b')
build() {
  cd $srcdir/gmailnotifier-keluoinhac-$pkgver/
  mkdir build
  cd build
  cmake -DQT_QMAKE_EXECUTABLE=qmake-qt4 -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..
  make
  make DESTDIR=$pkgdir install
}
