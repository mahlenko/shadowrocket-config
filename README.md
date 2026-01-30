# Использование конфига
Перейдите в раздел "Настройка", нажмите [ + ] в правом верхнем углу, и вставьте ссылку:
```
https://raw.githubusercontent.com/mahlenko/shadowrocket-config/refs/heads/main/vpn.conf
```

![Window config add](/screenshot-setup-dark.png#gh-dark-mode-only)
![Window config add](/screenshot-setup.png#gh-light-mode-only)

# Предотвращение утечки IP-адреса
Переходите **Настройки** → **UDP** и включаете **Включить реле** и **Отключить STUN**. "Allow Ports" оставляем пустым. Если хотите закрыть все порты, то укажите 0. Проверяем на [Browserleaks](https://browserleaks.com/dns).

Дополнительные конфиги по типу GEOSITE: https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Shadowrocket

# Using the configuration (en)
Go to the "Config" section, click [ + ] in the upper-right corner, and paste the link:
```
https://raw.githubusercontent.com/mahlenko/shadowrocket-config/refs/heads/main/vpn.conf
```

# Preventing IP address leakage
Go to **Settings** → **UDP** and enable **Enable Relay** and **Disable STUN**. We leave it empty in "Allow Ports". If you want to close all ports, then specify 0. We check for [Browserleaks](https://browserleaks.com/dns ).
