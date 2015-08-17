# Maintainer:  Shaw <puxx@mail.ustc.edu.cn>
# Contributor: Shadow Ma ( i at shadow.ma )

pkgname=qdoubanfm-git
pkgver=20140611
pkgrel=1
pkgdesc="A DoubanFM Client based on Qt5"
arch=('i686' 'x86_64')
url="https://github.com/zonyitoo/doubanfm-qt"
license=('MIT')
depends=('qt5-multimedia'
         'gstreamer0.10-base-plugins'
         'gstreamer0.10-good-plugins'
         'gstreamer0.10-ugly-plugins')
makedepends=('git')
source=("git+https://github.com/zonyitoo/doubanfm-qt.git")
md5sums=('SKIP')

build() {
	cd "${srcdir}/doubanfm-qt/"
	qmake-qt5 doubanfm-qt.pro
	make
}

package() {
	cd "${srcdir}/doubanfm-qt/"
	install -Dm755 doubanfm-qt "${pkgdir}/usr/bin/doubanfm-qt"
	install -Dm644 QDoubanFM.desktop "${pkgdir}/usr/share/applications/QDoubanFM.desktop"
	install -Dm644 QDoubanFM.png "${pkgdir}/usr/share/pixmaps/QDoubanFM.png"
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/qdoubanfm-git/LICENSE"
}
