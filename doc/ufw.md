## UFW

```bash
ufw enable
ufw logging high
ufw default deny incoming
ufw default allow outgoing
ufw allow ssh
ufw allow 16022 # если нестандартный порт ssh
ufw allow 51820/udp
# Просмотр правил 
ufw status verbose
```

## Полезные ссылки
- [установка ufw](https://linuxconfig.org/how-to-install-and-use-ufw-firewall-on-linux)
- [настройка ufw](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-with-ufw-on-ubuntu-22-04)
