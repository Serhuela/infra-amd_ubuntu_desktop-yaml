# Configuración aplicada a Ubuntu 26.04 Desktop

Configuración del equipo fuera del inventario de software y de los ajustes manuales, documentados en [CONFIGURACION_MANUAL.md](CONFIGURACION_MANUAL.md). Los playbooks de [`ansible/`](ansible/) son la fuente de verdad de los ajustes reproducibles.

Fecha de revisión: 2026-07-31

## Instalación base

- Idioma: `es_ES.UTF-8`; teclado español; zona horaria `Europe/Madrid`.
- Actualizaciones de seguridad, códecs y controladores durante la instalación.
- OpenSSH se instala posteriormente mediante Ansible.

## Configuración reproducible

- Repositorios APT oficiales de Google Chrome y Brave con sus claves de firma.
- Reloj de GNOME en formato de 24 horas, con día, fecha y segundos.
- Ghostty copia la selección al portapapeles estándar y pega con el clic derecho.
- `pyenv` se inicializa en Bash; `tfenv` se instala en `~/.tfenv` y se expone en `~/.local/bin`.
- Docker queda habilitado al inicio y el usuario local pertenece al grupo `docker`; es necesario cerrar e iniciar sesión para aplicar este último cambio.
- OpenSSH solo permite al usuario local autenticarse con las claves públicas versionadas en [`rsc/authorized_keys/`](rsc/authorized_keys/); deshabilita el acceso de `root`, la contraseña y la autenticación interactiva.
