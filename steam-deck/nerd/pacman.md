---
description: Установка сторонних пакетов используя pacman
---

# Установка пакетов через Pacman

#### Быстрый старт

{% embed url="https://plafon.gitbook.io/alt-zero/steam-deck/nerd/ustanovka-parolya-superpolzovatelya" %}
Если вы уже активировали суперпользователя, то пропускаем данный пункт
{% endembed %}

```
sudo steamos-readonly disable
```

```
sudo pacman-key --init
```

```
sudo pacman-key --populate archlinux
```

```
sudo pacman -Syu
```

{% hint style="success" %}
Если "страшно", то командой ниже, можно включить обратно Read-only для SteamOS. В любом случае все эти манипуляции "слетят" и обнулятся при последующем обновлении SteamOS.
{% endhint %}

```
sudo steamos-readonly enable
```







## Детальное описание всех действий

#### 1. Установите пароль Sudo (если вы еще этого не сделали)

{% embed url="https://plafon.gitbook.io/alt-zero/steam-deck/nerd/ustanovka-parolya-superpolzovatelya" %}

#### 2. Отключите режим только для чтения

***

* Откройте Konsole.
* Введите `sudo steamos-readonly disable` и нажмите Enter.
* Введите свой пароль sudo, когда будет предложено.
* Эта команда отключит защиту файловой системы root от записи, что позволит вам вносить изменения.

#### 3. Инициализируйте связку ключей Pacman

***

* В Konsole введите `sudo pacman-key --init` и нажмите Enter. Это инициализирует связку ключей Pacman.
* Затем введите `sudo pacman-key --populate archlinux` и нажмите Enter. Это заполнит связку ключей ключами подписи Arch Linux.
* Наконец, введите `sudo pacman -Syu` и нажмите Enter, чтобы обновить список пакетов вашей системы и обновить все устаревшие пакеты.

#### 4. Повторно включите режим только для чтения (рекомендуется)

***

После того как вы закончите устанавливать пакеты или вносить системные изменения, обычно рекомендуется повторно включить режим только для чтения для стабильности системы и предотвращения случайных модификаций.

* В Konsole введите `sudo steamos-readonly enable` и нажмите Enter.
* Введите свой пароль sudo, когда будет предложено.
