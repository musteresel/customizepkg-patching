# Author: Daniel Oertwig <Daniel.Oertwig+customizepkgpatching at gmail dot com>
pkgname=customizepkg-patching
pkgrel=1
pkgdesc="A tool to automate modification of PKGBUILDs using patch" 
url="https://github.com/DanielOertwig/customizepkg-patching" 
license="GPL" 
arch=('any')
depends=('bash' 'diffutils' 'patch')
optdepends=('vim: For using vimdiff')
provides=(customizepkg)
conflicts=(customizepkg)
source=('git://github.com/DanielOertwig/customizepkg-patching#branch=release') 
md5sums=('SKIP')

pkgver()
{
	cd customizepkg-patching
	echo $(git rev-list --count master).$(git rev-parse --short master)
}
package()
{
	cd customizepkg-patching
	install -d "$pkgdir/usr/bin"
	install -t "$pkgdir/usr/bin/cusomizepkg" customizepkg
	install -d "$pkgdir/etc/customizepkg.d"
}
