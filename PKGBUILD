# Maintainer: Xilin Wu <sophon@radxa.com>
# Upstream: Qualcomm video control (smart venc ctrl algo) prebuilt for armv8-2a

pkgname=qcom-smart-venc-ctrl-algo
pkgver=1.0
pkgrel=1
pkgdesc="Qualcomm prebuilt binaries for the Smart Video Encoder Control Algorithm, used to dynamically optimize video encoding parameters and performance."
arch=('aarch64')
url="https://qartifactory-edge.qualcomm.com"
license=('LicenseRef-Qualcomm-Proprietary')
depends=('qcom-fastcv-binaries')
options=('!strip')

source=("https://qartifactory-edge.qualcomm.com/artifactory/qsc_releases/software/chip/component/iot-core-algs.lnx.0.0/260112.1/prebuilt_yocto/qcom-video-ctrl_${pkgver}_armv8-2a.tar.gz")
sha256sums=('9e6b8b6e0b013b6126fe6ab0776591347f0f66fd7153f4afa8e100b9d64af308')

package() {
  cd "$srcdir"

  cp -a usr "$pkgdir/"
  cp -a etc "$pkgdir/"

  install -Dm644 usr/share/doc/qcom-video-ctrl/LICENSE \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
