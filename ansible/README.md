# ansible

Configuración Ansible para aplicar el estado deseado sobre la propia máquina Ubuntu ya instalada.

## Contenido

- [`configure-apt-repositories.yml`](configure-apt-repositories.yml): configura los keyrings y repositorios APT oficiales de Google Chrome y Brave.
- [`install-apt-packages.yml`](install-apt-packages.yml): actualiza los paquetes APT instalados e instala herramientas base, OpenSSH, `pyenv` con sus dependencias de compilación, Docker con Buildx y Compose, Solaar para el Logitech MX Master 3S, Google Chrome y Brave.
- [`install-snap-packages.yml`](install-snap-packages.yml): instala Bitwarden, Termius (`termius-app`), OpenCode (`opencode`) con su componente de escritorio y Visual Studio Code (`code`). OpenCode y Visual Studio Code usan confinamiento `classic`.
- [`install-antigravity-ide.yml`](install-antigravity-ide.yml): instala o actualiza Google Antigravity IDE para Linux x64 desde su archivo oficial; crea el comando `antigravity-ide` y su lanzador de escritorio. No usa el snap `antigravity`, que corresponde a Antigravity 2.0 y no al IDE.
- [`configure-development-tools.yml`](configure-development-tools.yml): instala `tfenv` en el directorio personal, crea su enlace en `~/.local/bin` e inicializa `pyenv` en Bash.
- [`configure-docker.yml`](configure-docker.yml): habilita Docker y añade el usuario actual al grupo `docker` para usarlo sin `sudo`.
- [`configure-gnome-clock.yml`](configure-gnome-clock.yml): muestra día, fecha y segundos en el reloj de GNOME con formato de 24 horas.
- [`configure-ghostty.yml`](configure-ghostty.yml): configura Ghostty para copiar al seleccionar y pegar texto con el clic derecho, sin sobrescribir otros ajustes del usuario.
- [`configure-ssh.yml`](configure-ssh.yml): instala las claves públicas de [`../rsc/authorized_keys/`](../rsc/authorized_keys/) para el usuario local y permite SSH solo mediante esas claves.
- [`requirements.yml`](requirements.yml): colecciones Ansible necesarias para ejecutar el playbook.
