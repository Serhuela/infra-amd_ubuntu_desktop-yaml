# ops

Procedimientos operativos para usar este repositorio.

## Ejecutar playbooks de Ansible en localhost

Instalar Ansible:

```bash
sudo apt install ansible
```

Instalar dependencias de Ansible:

```bash
ansible-galaxy collection install -r ansible/requirements.yml
```

Instalar la configuración base:

```bash
ansible-playbook -i localhost, -c local ansible/playbook.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

Instalar Visual Studio Code por separado:

```bash
ansible-playbook -i localhost, -c local ansible/vscode.yml -K -e ansible_become_exe=/usr/bin/sudo.ws
```

Se indica `/usr/bin/sudo.ws` porque Ansible 2.20 no reconoce correctamente el prompt de contraseña de `sudo-rs`, usado por defecto en este sistema. Esta opción usa el sudo clásico solo durante la ejecución del playbook, sin cambiar la configuración global.
