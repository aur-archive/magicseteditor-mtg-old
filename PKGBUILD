
pkgname=magicseteditor-mtg-old
pkgver=20140628
pkgrel=2
pkgdesc="Magic Set Editor templates for Magic: The Gathering Pre-Modern design"
arch=(any)
url="http://msetemps.sourceforge.net/phpBB3/viewtopic.php?t=144"
license=('freeware')
depends=('magicseteditor-mtg-base')
conflicts=("")
source=("http://downloads.sourceforge.net/msetemps/Magic - Alpha Beta Unlimited.mse-installer"
        "http://downloads.sourceforge.net/msetemps/Magic - Old Styles.mse-installer")
md5sums=('5c304c390be062e8cdb94330df901334'
         '507c7fdaf99cad8b9678dcdfe5e2f6fb')

package() {
  install -d $pkgdir/usr/share/magicseteditor/data

  cd $srcdir
  find magic-{mana-old,mana-small-abu,pt-symbols-portal,veryold}.* -name '*.png' -type f -exec mogrify {} \;
  cp -r magic-{mana-old,mana-small-abu,pt-symbols-portal,veryold}.* $pkgdir/usr/share/magicseteditor/data
  find magic-old* -name '*.png' -type f -exec mogrify {} \;
  cp -r magic-old* $pkgdir/usr/share/magicseteditor/data
  chmod -R 755 $pkgdir/usr/share/magicseteditor/data/*
}
