# Contributor: Simon Lackerbauer <calypso@nopm.net>
pkgname=sylph-searcher
pkgver=1.2.0
pkgrel=1
pkgdesc="Sylph-Searcher provides fast full-text search for Sylpheed"
arch=('i686' 'x86_64')
url="http://sylpheed.sraoss.jp/en/"
license=('BSD')
depends=('glib2' 'gtk2' 'postgresql' 'postgresql-tsearch2' 'libsylph' 'mecab' 'mecab-ipadic')
# mecab + mecap-ipadic you can get here http://sourceforge.net/project/showfiles.php?group_id=177856
source=(http://sylpheed.sraoss.jp/sylpheed/misc/$pkgname-$pkgver.tar.gz)
md5sums=('6a65c7bf2b6aa16f7c4fe7b0c3b1d6c5')
sha1sums=('2dd92e0e180f1f107ea4a1a9c6623e291be2b2c0')

build() {
	cd $startdir/src/$pkgname-$pkgver
	./configure --prefix=/usr
	make || return 1
	make prefix=$startdir/pkg/usr install
}
