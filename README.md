# Powerdns role

Ансибл роль для установки сервера Powerdns, включая отдельные dns рекурсоры

Требования:

1 Установлен ansible (не проверялось использование других версий)

```bash
pip3 install ansible==2.10.7
```

2 Установлен pip3

```bash
sudo apt install python3-pip
```

3 Установлены зависимости для тестирования роли (при необходимости)

```bash
pip3 install -r requirements.txt --force
```

4 Минимум 2 сервера для установки (авторитативный и рекурсор)

5 Имя авторитативного сервера в inventory.yml должно быть powerdns-master-01

6 Пример необходимых переменных для group_vars и host_vars можно просмотреть в каталоге molecule/default/ данной роли

7 После запуска плейбука с ролью необходимо зайти в web интерфейс, указав api url(http://lan_ip:8081/) и api key (от 16 символов) и создать доменную зону.
