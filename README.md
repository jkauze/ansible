# Playbooks utiles
Lista de playbooks personales para automatizar trabajos de administracion

Playbooks:
---------

- [playbook-checker-mac.yml](https://github.com/jkauze/ansible/blob/master/playbook-checker-mac.yml) - Setea/Verifica que exista el entorno minimo necesario en X maquinas

- [playbook-sync-mac.yml](https://github.com/jkauze/ansible/blob/master/playbook-sync-mac.yml) - Sincroniza/Verifica X maquinas destinos con respecto a una maquina fuente

Recordatorio de requisitos:
---------

- Ansible en la maquina origen
- Tener acceso por key-ssh a los hosts (mediante root)
- host con python > 2.7

Recordatorio de instrucciones:
---------


#### Para verificar antes de ejecutar (como root):
```
# ansible-playbook playbook-<x>-mac.yml --check
```

#### como root:
```
# ansible-playbook playbook-<x>-mac.yml
```

#### como user:
```
# ansible-playbook playbook-<x>-mac.yml -u root
```

#### como user aplicado a user no root con privilegios:
```
# ansible-playbook playbook-<x>-mac.yml -K
```
(Cambiar los becomes y ponerlo dentro de las tareas que lo requieran - debo modificar esto para no tener que hacer esto)