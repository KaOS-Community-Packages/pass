pkgname='pass'
pkgver=1.6.5
pkgrel=1
pkgdesc='Stores, retrieves, generates, and synchronizes passwords securely'
arch=('x86_64')
url='http://zx2c4.com/projects/password-store/'
license=('GPL2')
depends=('xclip' 'bash' 'gnupg' 'pwgen' 'tree')
optdepends=('git: for Git support')
source=(http://git.zx2c4.com/password-store/snapshot/password-store-${pkgver}.tar.xz)
md5sums=('2c4468360c678184051e76f03c2f6b04')

package() {
  cd "${srcdir}/password-store-$pkgver/"
  make DESTDIR="${pkgdir}" FORCE_ALL=1 install

  cd contrib/dmenu
  install -Dm0755 passmenu "${pkgdir}/usr/bin/passmenu"
} 
