pkgname='pass'
pkgver=1.7.2
pkgrel=1
pkgdesc='Stores, retrieves, generates, and synchronizes passwords securely'
arch=('x86_64')
url='http://zx2c4.com/projects/password-store/'
license=('GPL2')
depends=('xclip' 'bash' 'gnupg' 'tree')
optdepends=('git: for Git support')
source=(http://git.zx2c4.com/password-store/snapshot/password-store-${pkgver}.tar.xz)
md5sums=('6e2fd1baae2354fe03fae85e403505be')

package() {
  cd "${srcdir}/password-store-$pkgver/"
  make DESTDIR="${pkgdir}" FORCE_ALL=1 install

  cd contrib/dmenu
  install -Dm0755 passmenu "${pkgdir}/usr/bin/passmenu"
} 
