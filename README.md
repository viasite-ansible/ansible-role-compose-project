Create project from docker-compose.yml, setup dns, nginx, ssl, cron, shell.

Based on role site - https://github.com/viasite-ansible/ansible-role-site

## Features
- Create `update.sh` for project updates
- Generate docker-compose.yml, nginx configs
- DNS (Cloudflare, Selectel)
- SSL, Letsencrypt

#### Settings
See `defaults/main.yml`.

arole compose-project --limit popstas_server
arole compose-project --limit popstas_server --tags init-db

## Details
- Creates `cp_root` dir, `cp_root/data`, places configs in data, run update.sh
