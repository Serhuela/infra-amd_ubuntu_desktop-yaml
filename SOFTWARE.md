# Software instalado y aprobado tras instalar Ubuntu 26.04 Desktop

Inventario de software instalado manualmente y de instalaciones aprobadas para convertirlo en automatización reproducible.

Fecha de revisión: 2026-07-31

## Aplicaciones Snap

| Aplicación | Paquete | Versión detectada o declarada | Canal | Notas |
| --- | --- | --- | --- | --- |
| Bitwarden | `bitwarden` | `2026.4.0` | `latest/stable` | Gestor de contraseñas |
| OpenCode | `opencode` | `1.18.8` | `latest/stable` | Agente de código con componente de escritorio; usa confinamiento `classic` |
| Termius | `termius-app` | `9.42.2` | `latest/stable` | Cliente SSH |
| Visual Studio Code | `code` | `1b6a1881` | `latest/stable` | Instalado con confinamiento `classic` |

## Paquetes de repositorios APT de Ubuntu

| Aplicación | Paquete | Versión detectada o declarada | Notas |
| --- | --- | --- | --- |
| Ansible | `ansible` | `13.1.0+dfsg-1ubuntu1` | Automatización de este repositorio |
| curl | `curl` | `8.18.0-1ubuntu2.3` | Herramienta CLI HTTP |
| Docker Engine | `docker.io` | `29.1.3-0ubuntu4.1` | Motor de contenedores |
| Docker Buildx | `docker-buildx` | `0.30.1-0ubuntu1` | Constructor avanzado de imágenes |
| Docker Compose | `docker-compose-v2` | `2.40.3+ds1-0ubuntu1` | Orquestación de contenedores |
| Git | `git` | `1:2.53.0-1ubuntu1` | Control de versiones; instalado antes de GitHub CLI |
| GitHub CLI | `gh` | `2.46.0-4` | CLI de GitHub, disponible en repositorio Ubuntu `universe` |
| Ghostty | `ghostty` | `1.3.0~us1-0ubuntu1` | Terminal que permite copiar y pegar texto a mi estilo y dentro de opencode |
| OpenSSH Server | `openssh-server` | `1:10.2p1-2ubuntu3.5` | Acceso SSH mediante claves públicas autorizadas |
| pyenv | `pyenv` | `2.6.8-1` | Gestor de versiones de Python |
| Solaar | `solaar` | `1.1.19-1` | Configuración del ratón Logitech MX Master 3S |
| Ubuntu restricted addons | `ubuntu-restricted-addons` | `32` | Códecs/complementos multimedia restringidos |
| wl-clipboard | `wl-clipboard` | `2.2.1-2build1` | Portapapeles Wayland para OpenCode |

## Paquetes de repositorios APT externos

| Aplicación | Paquete | Versión detectada o declarada | Origen |
| --- | --- | --- | --- |
| Brave | `brave-browser` | Sin fijar | Repositorio oficial de Brave |
| Google Chrome | `google-chrome-stable` | `151.0.7922.71-1` | Repositorio oficial de Google |

## Instalaciones desde archivos oficiales

| Aplicación | Comando | Versión detectada o declarada | Origen |
| --- | --- | --- | --- |
| Google Antigravity IDE | `antigravity-ide` | `1.107.0` | Archivo oficial de Google para Linux x64 |
| tfenv | `tfenv` | Última revisión de `master` | Repositorio oficial `tfutils/tfenv` en `~/.tfenv` |

## Notas

- Separar instalaciones por origen: Snap, repositorios APT de Ubuntu, repositorios APT externos y archivos oficiales.
