#!/usr/bin/makepkg -p
# Maintainer:  Matthew Bauer <mjbauer95@gmail.com>
pkgname=uzbl-extension-manager
pkgver=20100119
pkgrel=1
pkgdesc=""
arch=(i686 x86_64)
url=""
license=('GPL')
depends=()
optdepends=()
makedepends=('gcc')
provides=('dundancy')

_gitroot="git://github.com/paradoq/uzbl-extension-manager.git"
_gitname="$pkgname-$pkgver"

build() {
	cd "${srcdir}"

	msg "Connecting to github.com GIT server...."

	if [ -d "${srcdir}/$_gitname" ] ; then
		cd "$_gitname" && git pull origin || return 1
		msg "The local files are updated."
	else
		git clone "$_gitroot" "$_gitname"
		cd "$_gitname"
	fi

	msg "GIT checkout done"
	msg "Starting install..."
}
