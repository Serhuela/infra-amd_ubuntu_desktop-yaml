# ansible

Configuración Ansible para aplicar el estado deseado sobre la propia máquina Ubuntu ya instalada.

## Contenido

- [`install-apt-packages.yml`](install-apt-packages.yml): instala `ansible`, `curl`, `git`, `gh` y `ubuntu-restricted-addons` desde los repositorios APT de Ubuntu en `localhost`.
- [`install-snap-packages.yml`](install-snap-packages.yml): instala Bitwarden, Termius (`termius-app`) y Visual Studio Code (`code`); este último usa confinamiento `classic`.
- [`install-google-chrome.yml`](install-google-chrome.yml): configura el keyring y repositorio APT de Google Chrome e instala `google-chrome-stable`.
- [`install-opencode.yml`](install-opencode.yml): instala OpenCode de forma idempotente; requiere ejecutar antes `install-apt-packages.yml` para disponer de `curl`.
- [`requirements.yml`](requirements.yml): colecciones Ansible necesarias para ejecutar el playbook.
