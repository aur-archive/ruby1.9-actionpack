# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Babken Vardanyan <483ken@gmail.com>

_gemname=actionpack
pkgname=ruby1.9-$_gemname
pkgver=3.2.19
pkgrel=1
pkgdesc='Web-flow and rendering framework putting the VC in MVC (part of Rails).'
arch=(any)
url='http://www.rubyonrails.org'
license=(MIT)
depends=(ruby1.9 ruby1.9-activesupport ruby1.9-activemodel ruby1.9-rack-cache ruby1.9-builder ruby1.9-rack ruby1.9-rack-test ruby1.9-journey ruby1.9-sprockets ruby1.9-erubis)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('44285b467d5c89d6fcc7ccb0d75e18371373a097')

package() {
  local _gemdir="$(ruby-1.9 -e'puts Gem.default_dir')"
  gem-1.9 install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
}
