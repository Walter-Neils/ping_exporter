# Maintainer: Walter Irvin Neils <walter@walterneils.com>
pkgname=prometheus-ping-exporter-bin
pkgver=1.0.0
pkgrel=1
pkgdesc="Prometheus exporter for ping metrics (Manually built binary)"
arch=('x86_64')
license=('MIT') # Update based on the actual repo license
depends=()
backup=('etc/prometheus-ping-exporter.yaml')

source=("ping_exporter"
        "prometheus-ping-exporter.service" "prometheus-ping-exporter.yaml")

sha256sums=('SKIP'
            'SKIP'
    	    'SKIP')

package() {
    install -Dm755 "${srcdir}/ping_exporter" "${pkgdir}/usr/bin/prometheus-ping-exporter"
    install -Dm644 "${srcdir}/prometheus-ping-exporter.yaml" "${pkgdir}/etc/prometheus-ping-exporter.yaml"
    install -Dm644 "${srcdir}/prometheus-ping-exporter.service" "${pkgdir}/usr/lib/systemd/system/prometheus-ping-exporter.service"
}
