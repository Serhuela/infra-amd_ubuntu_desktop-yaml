# ops

Procedimientos operativos para usar este repositorio.

## Ejecutar Ansible en localhost

Instalar Ansible:

```bash
sudo apt install ansible
```

Instalar dependencias de Ansible:

```bash
ansible-galaxy collection install -r ansible/requirements.yml
```

Ejecutar contra la máquina local:

```bash
ansible-playbook -i localhost, -c local ansible/playbook.yml --ask-become-pass
```
