# infra-amd_ubuntu_desktop-yaml

Repositorio IaC para la instalación de Ubuntu Desktop en mi AMD Ryzen 7900X.

## Instalación reproducible

- [`autoinstall.example.yaml`](autoinstall.example.yaml): plantilla para instalar Ubuntu Desktop de forma repetible con `autoinstall`/Subiquity.
- Antes de usarla, sustituir `identity.username`, `identity.hostname` y `identity.password` por valores reales. La contraseña debe ser un hash SHA-512 generado, por ejemplo, con `openssl passwd -6`.

## Documentación

- [Software instalado manualmente](SOFTWARE.md)
- [Configuración manual realizada](CONFIGURACION.md)
