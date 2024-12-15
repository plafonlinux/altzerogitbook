---
description: Установить Yandex Browser в Linux
---

# Yandex Browser

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-04-30 18-32-49.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
У дистрибутива ALT Linux официальная поддержка от Yandex.
{% endhint %}

## Платформа P11 и Сизиф&#x20;

```bash
sudo apt-get install yandex-browser-stable
```

## Flatpak (не рекомендуется)

```bash
flatpak install flathub ru.yandex.Browser
```









## Решение проблем и баги



* Отключение белой рамки вокруг браузера

<figure><img src="../../../.gitbook/assets/soft-yandex-browser-white-border-02.png" alt=""><figcaption></figcaption></figure>

В адресной строке пишем:

```
browser://flags/
```

В этих скрытых настройках надо найти параметр System window controls.

<figure><img src="../../../.gitbook/assets/soft-yandex-browser-white-border-03.png" alt=""><figcaption></figcaption></figure>

Меняем в нем переключатель на Enabled и перезагружаем браузер

Готово, рамка теперь не белая

<figure><img src="../../../.gitbook/assets/soft-yandex-browser-white-border-04.png" alt=""><figcaption></figcaption></figure>

* Активируем скрукгление окна в GNOME

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2024-08-09 07-01-38.png" alt=""><figcaption></figcaption></figure>

Устанавливаем расширение Rounded Window Corners Reborn

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2024-08-09 07-02-30.png" alt=""><figcaption></figcaption></figure>

### Установить можно через [Менеджер расширений](../../extensions/manager.md), либо через [сайт расширений](https://extensions.gnome.org/extension/7048/rounded-window-corners-reborn/).
