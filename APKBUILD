# Maintainer: lazaruslgoneone <lazaruslongone@gmail.com>

# vim: set noet:
# vim: set ft=sh:

pkgname=soxy
pkgver=0.3.0
pkgrel=0
pkgdesc="a tool to help daemonize ssh as a socks proxy"
pkgusers="soxy"
url="https://github.com/lazaruslongone/soxy/"
arch="noarch"
license="custom"
depends="openssh bash"
makedepends="bash"
install=
source="https://github.com/lazaruslongone/${pkgname}/archive/${pkgver}.zip
				soxy.initd
				soxy.profiled
				config.sample"

_builddir="$srcdir/$pkgname-$pkgver"

package() {
	echo "building ${pkgname}-${pkgver}-r${pkgrel}"
	cd "${_builddir}"
	install -vDm755 ../soxy.initd "${pkgdir}"/etc/init.d/soxy
	install -vDm755 ../soxy.profiled "${pkgdir}"/etc/profile.d/soxy
	install -vd  "${pkgdir}"/etc/soxy
	install -vDm755 ../config.sample "${pkgdir}"/etc/soxy/config
	install -vd "${pkgdir}"/usr/bin
	install -vDm755 soxy "${pkgdir}"/usr/bin/soxy
}

md5sums="c65904b66c707a00a737e3d597171a4b  0.3.0.zip
3065f675781f9e33befe9384eaf2b6c0  soxy.initd
20dc6717e265df351f158e68ae3218c3  soxy.profiled
0ff264d8c4835a922a77283421445ecc  config.sample"
sha256sums="97eedc1fb638c4a4711cd219e1def767d144b8474f48c9a7170d10cbe75632d3  0.3.0.zip
6ec3c2087ac0cd8c4381142459531f8c44e1c90e3cc51c5b18a11e0f6a69ffce  soxy.initd
bf4d96bce60224e9b80708d1d598ece57c62d5fc44dd880ba0c6014acd5d287a  soxy.profiled
40a9f5c555172a628f092df52c0d54d560e2b37cf48b019b7cdc8723ddfe133d  config.sample"
sha512sums="0cf5858acce9114b6a77bee3d0f8890134977a900cd7d83df6da9e5db8183454c815fd9dd9afbaaa4aa98dfe7b608f3a79c0231cd28c8e481f99d6f190d2ac00  0.3.0.zip
9f120860dbde9c5a43ab811c1f6366efbb3faea464f8f1ef85d7d058aa9d97cea700a6678c4c4c47d36aae7853a1e2a184da4f9f9349bba8ac04df3359df486a  soxy.initd
59835fd5dda3dd4e0307c656b054c53602bd6472b8212fa288f509c47e67409743135e951734451c27c266d1e2a01bb676c9c3f8a0f8d74dce34316b3432c0ec  soxy.profiled
d511aa6af05e9f66a2950d58c9a52b01d2714ff6aef7df438da7dd5c7a3bef17aa580131ceb3e457082f0f920db5adf0e46c96175374cf1033fd614def0d36fa  config.sample"
