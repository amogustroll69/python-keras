_pkgbase='keras'
pkgbase="python-${_pkgbase}"
pkgname=("${pkgbase}")
pkgdesc='A deep learning API written in Python, running on top of the machine learning platform TensorFlow'
url='https://keras.io/'
license=('Apache')
pkgver=2.15.0
pkgrel=1
arch=('any')
source=("https://files.pythonhosted.org/packages/fc/a7/0d4490de967a67f68a538cc9cdb259bff971c4b5787f7765dc7c8f118f71/keras-2.15.0-py3-none-any.whl"
	"${_pkgbase}-${pkgver}-LICENSE::https://github.com/keras-team/keras/raw/master/LICENSE")
makedepends=('python-build' 'python-installer' 'python-wheel')
depends=('absl-py' 'python' 'python-h5py' 'python-keras-preprocessing' 'python-numpy' 'python-pandas' 'python-pillow'
         'python-pydot' 'python-scipy' 'python-six' 'python-tensorflow' 'python-yaml' 'tensorboard')
sha256sums=("2dcc6d2e30cf9c951064b63c1f4c404b966c59caf09e01f3549138ec8ee0dd1f" "43070e2d4e532684de521b885f385d0841030efa2b1a20bafb76133a5e1379c1")

package () {
  python -m installer --destdir="$pkgdir" *.whl
  install -Dm 644 "${_pkgbase}-${pkgver}-LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
