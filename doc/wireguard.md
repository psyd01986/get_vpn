## Установка и настройка wireguard

## Перед установкой
- Изменить в файле [docker/wireguard-server-compose.yml](../docker/wireguard-server-compose.yml) значение переменной SERVERURL на свой ВНЕШНИЙ IP
```bash
    environment:
      - SERVERURL=95.164.47.201 #ваш внешний IP
```

- Запустить сервер
```bash
# Запуск сервера
docker-compose -f ./wireguard-server-compose.yml up -d
# Остановка сервера
docker-compose -f ./wireguard-server-compose.yml down
```

## Добавление новых пользователей:
- в [docker/wireguard-server-compose.yml](../docker/wireguard-server-compose.yml) через запятую допишите новых пользователей
```bash
- PEERS=name1,hpc2,name2,name3,NEWname1,NEWname2 # etc...
```
- остановите и запустите заново сервис, старые пользователи остануться , новые будут добавлены в директорию config


- [docker-wireguard](https://github.com/linuxserver/docker-wireguard)
- [instalation](https://www.wireguard.com/install/)
- [exclude ip from tunel](https://www.procustodibus.com/blog/2021/03/wireguard-allowedips-calculator/)
- [Инструменты управления wireguard](https://habr.com/ru/articles/738890/)
