# ops

Procedimientos operativos para usar este repositorio.

## Ejecutar playbooks de Ansible en localhost

Instalar dependencias de Ansible:

```bash
ansible-galaxy collection install -r ansible/requirements.yml
```

Ejecutar los playbooks en este orden:

```bash
ansible-playbook -i localhost, -c local ansible/install-apt-packages.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/configure-ghostty.yml
```

```bash
ansible-playbook -i localhost, -c local ansible/install-snap-packages.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/install-google-chrome.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/install-antigravity-ide.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

Se indica `/usr/bin/sudo.ws` porque Ansible 2.20 no reconoce correctamente el prompt de contraseña de `sudo-rs`, usado por defecto en este sistema. Esta opción usa el sudo clásico solo durante la ejecución del playbook, sin cambiar la configuración global.

`install-antigravity-ide.yml` descarga la versión declarada del archivo oficial de Google para Linux x64. Para actualizarla, cambiar juntos `antigravity_ide_version` y `antigravity_ide_build` por los valores publicados en [la página oficial de descarga](https://antigravity.google/download#antigravity-ide). No sustituirlo por el snap `antigravity`: instala Antigravity 2.0, no Google Antigravity IDE.

`install-snap-packages.yml` instala también el componente opcional `opencode+desktop`, necesario para abrir OpenCode Desktop desde App Center.

`configure-ghostty.yml` añade solo el bloque gestionado por Ansible a `~/.config/ghostty/config`: copia al seleccionar y pega texto con el clic derecho. `wl-clipboard`, instalado por el playbook APT, permite a OpenCode leer imágenes del portapapeles en Wayland mediante `Ctrl+V`.
