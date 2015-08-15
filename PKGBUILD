# Maintainer: Clayton Holloway <clayton.holloway@gmail.com>

pkgname=droppuburl
pkgver=latest
pkgrel=5
pkgdesc="simple 'open-with' script to copy a dropbox public url to the clipboard. Works well with pcmanfm/thunar/etc"
arch=(any)
license=('GPL')
url="http://www.dropbox.com"
depends=('xclip' 'python2' 'dropbox')

source=(http://www.dropbox.com/download?dl=packages/dropbox.py droppuburl droppuburl.desktop)
md5sums=('b094beab191d84bc0117fa5c3dbeaa2c'
         'ccc776a6d93b02ccfb2064a4366a12e5'
         '1b16e481b6b7b066e024264a105d2493')

package() {
    cd "$srcdir" || return 1

    install -D -m755 "${srcdir}/droppuburl"           "${pkgdir}/usr/bin/droppuburl"
    install -D -m755 "${srcdir}/dropbox.py"           "${pkgdir}/usr/bin/dropbox.py"

    # Desktop launcher with icon
    install -D -m644 "${srcdir}/droppuburl.desktop" "${pkgdir}/usr/share/applications/droppuburl.desktop"

}

# vim:set ts=4 sw=4 et:
