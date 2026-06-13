# Software instalado tras instalar Ubuntu 26.04 Desktop

Inventario de software instalado manualmente para convertirlo más adelante en automatización reproducible.

Fecha de revisión: 2026-06-13

## Aplicaciones Snap

| Aplicación | Paquete | Versión detectada | Canal | Notas |
| --- | --- | --- | --- | --- |
| Bitwarden | `bitwarden` | `2026.4.0` | `latest/stable` | Gestor de contraseñas |
| Visual Studio Code | `code` | `1b50d58d` | `latest/stable` | Instalado con confinamiento `classic` |

## Paquetes APT / DEB

| Aplicación | Paquete | Versión detectada | Notas |
| --- | --- | --- | --- |
| Google Chrome | `google-chrome-stable` | `149.0.7827.114-1` | Instalado desde `.deb` o repositorio externo; actualmente solo aparece en `/var/lib/dpkg/status` |
| curl | `curl` | `8.18.0-1ubuntu2.1` | Herramienta CLI HTTP |
| Git | `git` | `1:2.53.0-1ubuntu1` | Control de versiones |
| GitHub CLI | `gh` | `2.46.0-4` | CLI de GitHub, disponible en repositorio Ubuntu `universe` |
| Ubuntu restricted addons | `ubuntu-restricted-addons` | `32` | Códecs/complementos multimedia restringidos |

## Instalaciones fuera de APT/Snap

| Herramienta | Ruta detectada | Versión detectada | Notas |
| --- | --- | --- | --- |
| opencode | `~/.opencode/bin/opencode` | `1.17.4` | Instalado con `curl -fsSL https://opencode.ai/install \| bash` |

## Notas

- Separar instalaciones por método: `apt`, `snap`, instalador externo y configuración de usuario.
- Para Chrome conviene automatizar la instalación del repositorio oficial o documentar la descarga del `.deb`.
