# ansible

Configuración Ansible para aplicar el estado deseado sobre la propia máquina Ubuntu ya instalada.

## Contenido

- [`install-apt-packages.yml`](install-apt-packages.yml): instala `ansible`, `curl`, `git`, `gh`, Ghostty, `ubuntu-restricted-addons` y `wl-clipboard` desde los repositorios APT de Ubuntu en `localhost`.
- [`install-snap-packages.yml`](install-snap-packages.yml): instala Bitwarden, Termius (`termius-app`), OpenCode (`opencode`) con su componente de escritorio y Visual Studio Code (`code`). OpenCode y Visual Studio Code usan confinamiento `classic`.
- [`install-google-chrome.yml`](install-google-chrome.yml): configura el keyring y repositorio APT de Google Chrome e instala `google-chrome-stable`.
- [`install-antigravity-ide.yml`](install-antigravity-ide.yml): instala o actualiza Google Antigravity IDE para Linux x64 desde su archivo oficial; crea el comando `antigravity-ide` y su lanzador de escritorio. No usa el snap `antigravity`, que corresponde a Antigravity 2.0 y no al IDE.
- [`configure-gnome-clock.yml`](configure-gnome-clock.yml): muestra día, fecha y segundos en el reloj de GNOME con formato de 24 horas.
- [`configure-ghostty.yml`](configure-ghostty.yml): configura Ghostty para copiar al seleccionar y pegar texto con el clic derecho, sin sobrescribir otros ajustes del usuario.
- [`requirements.yml`](requirements.yml): colecciones Ansible necesarias para ejecutar el playbook.
