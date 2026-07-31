# Install svxlink pour Debian (Bookworm et Trixie)

Ce dépôt contient deux scripts d’installation pour **svxlink** depuis les sources
officielles, avec sons AssoRF (qc_QC) et service systemd prêt à l’emploi :

- `install_svx_bookworm.sh` : pour Debian 12 Bookworm
- `install_svx_trixie.sh`   : pour Debian 13 Trixie

## Installation sur Debian 12 Bookworm

```bash
sudo apt update && \
sudo apt install -y git && \
git clone https://github.com/RadioamateursduFjord/install_svx.git && \
cd install_svx && \
sudo bash install_svx_bookworm.sh
```

## Installation sur Debian 13 Trixie

```bash
sudo apt update && \
sudo apt install -y git && \
git clone https://github.com/RadioamateursduFjord/install_svx.git && \
cd install_svx && \
sudo bash install_svx_trixie.sh
```

## Configuration svxlink

Après l’installation, la configuration se trouve dans :

- `/etc/svxlink/svxlink.conf`
- les fichiers de modules dans `/etc/svxlink/`

Redémarrer svxlink après modifications :

```bash
sudo systemctl restart svxlink.service
sudo systemctl status svxlink.service
```
