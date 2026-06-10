# Использование конфига
Перейдите в раздел "Настройка", нажмите [ + ] в правом верхнем углу, и вставьте ссылку:
```
https://raw.githubusercontent.com/mahlenko/shadowrocket-config/refs/heads/main/vpn.conf
```

![Window config add](/screenshot-setup-dark.png#gh-dark-mode-only)
![Window config add](/screenshot-setup.png#gh-light-mode-only)

### Предотвращение утечки IP-адреса
Переходите **Настройки** → **UDP** и включаете **Включить реле** и **Отключить STUN**. "Allow Ports" оставляем пустым. Если хотите закрыть все порты, то укажите 0. Проверяем на [Browserleaks](https://browserleaks.com/dns).

Дополнительные конфиги по типу GEOSITE в соседнем репозитории: [https://github.com/mahlenko/shadowrocket-rules-v2fly](https://github.com/mahlenko/shadowrocket-rules-v2fly)

### Выбор сервера

_🙏 Ранее не знал, может будет полезно кому-то еще_

Если у вас несколько серверов, Shadowrocket позволяет выбрать сервер для нужного правила:
- Выберите конфигурацию -> **Редактировать конфигурацию**
- Правила -> **Выбрать нужное правило**
- Политика -> Внизу список с нужным сервером, выбрать тот, который нужно использовать для конкретного правила.

или в тексте конфига, указать точное название сервера в списке пример для записи:
```
RULE-SET,...,SERVER 1
DOMAIN-SUFFIX,instagram.com,PROXY
IP-CIDR,149.154.160.0/21,SERVER 2
```

### VLESS и MTProto
Протоколы VLESS и MTProto не могут функционировать одновременно. Для использования MTProto при активном VPN-соединении необходимо настроить исключение для прокси-сервера.
Внесите следующие изменения в конфигурационный файл:
1. Откройте конфигурацию и выберите опцию **Редактировать обычный текст**.
2. В конец списка `tun-excluded-routes`, добавьте через запятую IP-адреса ваших серверов MTProto (IP-CIDR).

Также исключение можно добавить из интерфейса:
1. Откройте конфигурацию и выберите опцию **Редактировать конфигурацию**
2. Перейдите в раздел "**Общее**"
3. Добавьте IP в раздел "Исключенные маршруты TUN" (IP-CIDR)

# Using the configuration (en)
Go to the "Config" section, click [ + ] in the upper-right corner, and paste the link:
```
https://raw.githubusercontent.com/mahlenko/shadowrocket-config/refs/heads/main/vpn.conf
```

### Preventing IP address leakage
Go to **Settings** → **UDP** and enable **Enable Relay** and **Disable STUN**. We leave it empty in "Allow Ports". If you want to close all ports, then specify 0. We check for [Browserleaks](https://browserleaks.com/dns ).
