---
description: Кастомный fastfetch oт PLAFON для ALT Linux
---

# Fastfech

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-00-14.png" alt=""><figcaption></figcaption></figure>

### Устанавливаем Fastfetch <a href="#nastraivaem-neofetch" id="nastraivaem-neofetch"></a>

```bash
sudo apt-get install fastfetch
```

или через EPM

```
epmi fastfetch
```

### Установка шрифтов

01\. Качаем архив со шрифтами и закидываем в папку .fonts в Домашнем каталоге

{% file src="../../.gitbook/assets/FiraCode.zip" %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-04-25.png" alt=""><figcaption></figcaption></figure>

02\. Включаем кастомный шрифт в своём терминале

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-05-33.png" alt=""><figcaption></figcaption></figure>

### Установка кастомной темы

01\. Качаем конфиг с темой и помещаем куда угодно, в моём случае это папка `Fastftech` в `~/Документы`

{% file src="../../.gitbook/assets/plafonfetch.jsonc" %}

02\. Запускаем командой

```bash
fastfetch --logo PostMarketOS_small -c '/home/plafon/Документы/Fastfetch/plafonfetch.jsonc'
```

{% hint style="info" %}
Лично для себя в качестве Logo выбрал PostMarketOS\_small, вы выбирайте что вам больше по душе.
{% endhint %}

Можно создать [Alias](alias.md)

```bash
alias n="fastfetch --logo PostMarketOS_small -c '/home/plafon/Документы/Fastfetch/plafonfetch.jsonc'"
```

### Кастомная тема с ASCII Art

<figure><img src="../../.gitbook/assets/Снимок экрана от 2025-01-11 20-41-57.png" alt=""><figcaption></figcaption></figure>

01\. Скачиваем архив с конфигом

{% file src="../../.gitbook/assets/2025.zip" %}

02\. Запускам fastfetch с указанием пути до конфига

```bash
fastfetch -c /путь/до-конфига.conf
```
