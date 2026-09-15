# Maintainer: Xilin Wu <sophon@radxa.com>
# Upstream: Qualcomm video control (smart venc ctrl algo) prebuilt for armv8a

pkgname=qcom-smart-venc-ctrl-algo
pkgver=1.0.2
pkgrel=1
pkgdesc="Qualcomm prebuilt binaries for the Smart Video Encoder Control Algorithm, used to dynamically optimize video encoding parameters and performance."
arch=('aarch64')
url="https://qartifactory-edge.qualcomm.com"
license=('LicenseRef-Qualcomm-Proprietary')
depends=('glib2' 'qcom-fastcv-binaries')
options=('!strip')

source=("https://qartifactory-edge.qualcomm.com/artifactory/qsc_releases/software/chip/component/iot-core-algs.lnx.0.0/260814/prebuilt_yocto/qcom-video-ctrl_${pkgver}_armv8a.tar.gz")
sha256sums=('6d4eec53be35c145231b5e38fe38561753dda124eec14470adf77822f6dea8f3')

package() {
  cd "$srcdir"

  cp -a usr "$pkgdir/"
  cp -a etc "$pkgdir/"

  install -Dm644 usr/share/doc/qcom-video-ctrl/LICENSE.qcom-2 \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE.qcom-2.txt"
}
