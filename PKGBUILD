# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Maintainer: Evan Teitelman <teitelmanevan at gmail.com>
pkgname='ruby-arachni-rpc'
_gemname=${pkgname#ruby-}
pkgver=0.1.3
pkgrel=1
pkgdesc="Arachni's EventMachine based RPC client and server."
arch=('any')
url="http://www.arachni-scanner.com/"
license=('GPL')
depends=('ruby')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('ddbf48d31410da7c7905f6d9202c41db')

package() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
