---
description: ALT Booster утилита компаньон для настройки ALT Workstation (GNOME)
tags:
  - altbooster
  - osalt
---

# 🚀 ALT Booster

<figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-30.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://github.com/plafonlinux/altbooster" %}

**Доступные версии:** \
\
<mark style="color:$success;">**GitHub (main)**</mark> - v5.6.9      <mark style="color:$danger;">**(alpha)**</mark> - v5.7-alpha\
<mark style="color:blue;">**p11**</mark>**:** v5.6.7                <mark style="color:orange;">**Sysiphus**</mark>**:** v5.6.9

#### 1. Установка из GitHub (рекомендуется, самая свежая версия)

```
su - -c 'apt-get install git'
```

```
git clone https://github.com/plafonlinux/altbooster.git
cd altbooster
./install.sh
```

#### 2. Установка из репозитория ALT Linux (альтернатива)

_Примечание:_ версия в репозитории может отставать от GitHub-релиза.

**Вариант A: через apt-get**

```
sudo apt-get update && sudo apt-get install plafon-altbooster
```

**Вариант B: через EPM**

```
epmi plafon-altbooster
```

#### 3. Запустить

```
altbooster
# или через меню приложений GNOME
```

#### Удаление

```
./uninstall.sh
```

## Об ALT Booster

#### Приложения, Расширения, Flatpak:

* Поиск и установка приложений из p11, Cизифа, epm play и Flathub
* Список рекомендуемых приложений
* Поиск и установка расширений для GNOME
* Список рекомендуемых расширений
* Управления приложениями во Flatpak (обновление, удаление, заморозка)
* Включение Flathub и настройка Flatpak в системе

<div><figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-36.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-38.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-41.png" alt=""><figcaption></figcaption></figure></div>

Очистка системы, твики и планировщики

<div><figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-52.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-56.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-56-58.png" alt=""><figcaption></figcaption></figure></div>

Полноценный бэкапер для вашей системы

* Создание временных точек доступа по аналогии с TimeShift
* Создание полноценного переносного зеркала Btrfs или EXT4
* Создание переносного архива посредством Borg \
  \
  и многое другое ....

<div><figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-57-03.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-57-06.png" alt=""><figcaption></figcaption></figure> <figure><img src=".gitbook/assets/Снимок экрана от 2026-03-29 11-57-09.png" alt=""><figcaption></figcaption></figure></div>

