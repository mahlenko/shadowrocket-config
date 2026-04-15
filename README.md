# Использование конфига
Перейдите в раздел "Настройка", нажмите [ + ] в правом верхнем углу, и вставьте ссылку:
```
https://raw.githubusercontent.com/mahlenko/shadowrocket-config/refs/heads/main/vpn.conf
```

![Window config add](/screenshot-setup-dark.png#gh-dark-mode-only)
![Window config add](/screenshot-setup.png#gh-light-mode-only)

### Предотвращение утечки IP-адреса
Переходите **Настройки** → **UDP** и включаете **Включить реле** и **Отключить STUN**. "Allow Ports" оставляем пустым. Если хотите закрыть все порты, то укажите 0. Проверяем на [Browserleaks](https://browserleaks.com/dns).

Дополнительные конфиги по типу GEOSITE: https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Shadowrocket

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
