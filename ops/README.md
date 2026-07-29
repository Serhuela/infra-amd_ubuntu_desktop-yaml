# ops

Procedimientos operativos para usar este repositorio.

## Ejecutar playbooks de Ansible en localhost

Instalar dependencias de Ansible:

```bash
ansible-galaxy collection install -r ansible/requirements.yml
```

Ejecutar los playbooks en este orden. El de OpenCode depende de `curl`, instalado por el primero:

```bash
ansible-playbook -i localhost, -c local ansible/install-apt-packages.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/install-snap-packages.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/install-google-chrome.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

```bash
ansible-playbook -i localhost, -c local ansible/install-opencode.yml
```

Se indica `/usr/bin/sudo.ws` porque Ansible 2.20 no reconoce correctamente el prompt de contraseña de `sudo-rs`, usado por defecto en este sistema. Esta opción usa el sudo clásico solo durante la ejecución del playbook, sin cambiar la configuración global.
