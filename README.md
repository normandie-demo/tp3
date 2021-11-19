# TP numéro 3

## Objectif:

Exécuter une commande Ansible "ad-hoc"

## Besoin:

- Exécuter un `echo Hello World` via le module *debug* et *msg* sur localhost
- Exécuter la commande `hostname` via le module *shell* sur:
  - L’ensemble des serveurs sauf localhost
  - Les serveurs *back*
- Exécuter la commande `whoami` via le module *shell* sur:
  - *server-2.scc-edu*
  - *server-4.scc-edu*
- Installer le paquet **nginx** via le module *dnf* sur *server-1.scc-edu*
