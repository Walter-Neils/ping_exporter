# Maintainer: Walter Irvin Neils <walter@walterneils.com>
pkgname=prometheus-ping-exporter-bin
pkgver=1.0.0
pkgrel=1
pkgdesc="Prometheus exporter for ping metrics (Manually built binary)"
arch=('x86_64')
license=('MIT') # Update based on the actual repo license
depends=()
backup=('etc/prometheus-ping-exporter.conf') # If you add a config later

# We assume the binary and service file are in the same folder as this PKGBUILD
source=("ping_exporter"
        "prometheus-ping-exporter.service")

# Skip checksums since these are your local files
sha256sums=('SKIP'
            'SKIP')

package() {
    # 1. Install the binary
    install -Dm755 "${srcdir}/ping_exporter" "${pkgdir}/usr/bin/prometheus-ping-exporter"

    # 2. Install the systemd service
    install -Dm644 "${srcdir}/prometheus-ping-exporter.service" "${pkgdir}/usr/lib/systemd/system/prometheus-ping-exporter.service"
}
