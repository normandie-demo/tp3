# Correction TP 3

## Exécuter un `echo Hello World` via le module *debug* et *msg* sur localhost


```Shell
ansible -i inventory 'localhost' -m debug -a "msg='Hello World'"
```

## Exécuter la commande `hostname` via le module *shell* sur:

1. L’ensemble des serveurs sauf localhost

```Shell
ansible -i inventory '*,!localhost' -m shell -a hostname
```

2. Les serveurs *back*

```Shell
ansible -i inventory 'back' -m shell -a hostname
```

## Exécuter la commande `whoami` via le module *shell* sur:

1. *server-2.scc-edu*

```Shell
ansible -i inventory 'server-2.scc-edu,' -m shell -a whoami
```

2. *server-4.scc-edu*

```Shell
ansible -i inventory 'server-4.scc-edu,' -m shell -a whoami
```

## Installer le paquet **nginx** via le module *dnf* sur *server-1.scc-edu*

```Shell
ansible -i inventory 'server-1.scc-edu' -m dnf -a 'name=nginx' --become --become-user=root --become-method=sudo
```
