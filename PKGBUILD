# Maintainer: Jack Maguire <jackmaguire1234@gmail.com>

_pkgname=fizz_buzz
pkgname=${_pkgname}-git
pkgrel=1
pkgver=1.0.2
pkgdesc='A Simple Fizzbuzz'
arch=('x86_64')
url="https://github.com/Epacnoss/fizz_buzz.git"
license=('MIT')
makedepends=('rust' 'git')
provides=('fizz_buzz')
conflicts=('fizz_buzz')
source=("git@github.com:Epacnoss/fizz_buzz.git")
md5sums=('SKIP')

pkgver() {
    cd "$srcdir/$_pkgname"
    printf "1.0.2"
}

build() {
    cd $_pkgname
    cargo build --locked --release
}

package() {
    cd $_pkgname
    install -Dm755 "target/release/$_pkgname" \
        -t "$pkgdir/usr/bin"
    install -Dm644 LICEN?E \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
