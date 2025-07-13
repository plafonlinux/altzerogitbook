---
description: Делаем красивый терминал на ZSH
---

# Терминал на ZSH

{% hint style="success" %}
Большая благодарность автору канала [`Toxblh. Не только Linux`](https://t.me/toxblh_linux) за предоставленный гайд и сорсы.
{% endhint %}

{% embed url="https://github.com/Toxblh/dotfiles" %}

Качаем мой `.zshrc`:&#x20;

{% file src="../../.gitbook/assets/.zshrc" %}

Закидываем `.zshrc` в папку `/home`

<figure><img src="../../.gitbook/assets/Vu6xVEHHTGc.jpg" alt=""><figcaption><p>Чтобы видеть скрытые файлы и каталоги используем CTRL+H</p></figcaption></figure>

Устанавливаем git и zsh

```bash
sudo apt-get install git zsh
```

Устанавливаем zplug

```bash
git clone https://github.com/zplug/zplug ~/.zplug
```

Выполняем установку всех плагинов zplug, просто вбиваем:

```
zsh
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-08-18 07-48-37.png" alt=""><figcaption></figcaption></figure>

Делаем ZSH по умолчанию для нашего терминала:

```
sudo gedit /etc/passwd
```

и меняем `/bin/bash` на `/bin/zsh`:

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-08-18 08-17-47.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Обязательно делаем `systemctl logout` или перезапускаем ПК.
{% endhint %}
