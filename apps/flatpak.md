---
description: Установка поддержки Flatpak в ALT Linux
---

# Flatpak

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-51-52.png" alt="" width="375"><figcaption></figcaption></figure>

### Установка Flatpak и Flathub в ALT Linux

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/repo/flathub" %}

### Управление Flatpak приложениями

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-49-28.png" alt=""><figcaption></figcaption></figure>

Обновить все Flatpak приложения:

```bash
flatpak update
```

Посмотреть список приложений Flatpak:

```bash
flatpak list
```

Удалить Flatpak приложение:

```
flatpak remove org.название.приложения
```

Удалить неиспользуемые библиотеки:

```bash
flatpak remove --unused
```

Удаляем папку приложения с .var после удаления самого приложения:

```bash
flatpak remove --delete-data
```

{% hint style="warning" %}
Если вы используете команду epm full-upgrade, то нет надобности обновлять Flatpak приложения отдельно, так как данная команда, помимо самой системы, обновляет и Flatpak-и.
{% endhint %}



Приложения для управления Flatpak-ами

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/apps/warehouse" %}

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/apps/flatseal" %}









## Проблемы и баги на ALT Linux

### Проблема с bubblewrap на ALT Linux | Не запускаются Flatpak приложения

{% hint style="warning" %}
Недавно столкнулся с проблемой, то что у ядра по-умолчанию нет возможности создавать userspace непревилигированным пользователям. Это предпочтительный режим для современных операционных систем. Ядро должно разрешать непривилегированным пользователям создавать новые пространства имен пользователей.

Подробнее можно почитать [здесь](https://github.com/flatpak/flatpak/wiki/User-namespace-requirements).
{% endhint %}

### Решение:

```bash
su -
echo kernel.unprivileged_userns_clone=1 > /etc/sysctl.d/50-bubblewrap.conf
sysctl -w kernel.unprivileged_userns_clone=1
chmod 775 /usr/bin/bwrap
exit
```

```bash
systemctl --user restart flatpak-portal.service
```

{% hint style="info" %}
Так как при обновлении пакета bubblewrap это всё дело может слететь, то я написал маленький сервис, который будет проверять обновлялся ли bubblewrap и если да, то будет применять команду 4.
{% endhint %}

Создайте файл `/etc/systemd/system/check-bwrap-update.service`:

```bash
[Unit]
Description=Check bubblewrap update

[Service]
Type=oneshot
ExecStart=/usr/bin/bash -c "test $(find /usr/bin/bubblewrap -mtime 0 |wc -l) -eq 1 && sudo chmod 775 /usr/bin/bwrap"

[Install]
WantedBy=multi-user.target

```

```bash
sudo systemctl daemon-reload
```

```bash
sudo systemctl enable check-bwrap-update.service
```



