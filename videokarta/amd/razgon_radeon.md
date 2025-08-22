---
description: Как включить разгон на AMD?!
---

# Разгон видеокарты AMD

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 13-41-07.png" alt=""><figcaption><p>CoreCTRL</p></figcaption></figure>

Необходимо добавить эти параметры в опции загрузки ядра:

```
amdgpu.ppfeaturemask=0xffffffff radeon.cik_support=0 amdgpu.cik_support=1
```

Для GRUB

```bash
sudo nano /etc/sysconfig/grub2
```

Должно получится примерно так (_**кавычки важны!**_):

{% hint style="info" %}
Пример:&#x20;

```
GRUB_CMDLINE_LINUX_DEFAULT='quiet splash ваш_пункт1 ваш_пункт2'
```
{% endhint %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-06-11 19-46-31.png" alt=""><figcaption></figcaption></figure>

И пересобираем GRUB чтобы закрепить новые параметры, командой:

```bash
sudo update-grub
```

{% hint style="success" %}
Перезапускаем ПК, опции разгона должны активироваться!
{% endhint %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-06-11 19-48-21.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.altlinux.org/Grub" %}



## Для ALT Atom&#x20;

В атомарной версии дистрибутива для запуска системы используется bootc

Редактируем конфигурацию образа

```bash
sudo nano /etc/apm/image.yml
```

В секцию commands: необходимо добавить наши параметры в виде массива:

```toml
commands:
    - 'echo "kargs = [\"amdgpu.ppfeaturemask=0xffffffff\", \"radeon.cik_support=0\", \"amdgpu.cik_support=1\"]" > /usr/lib/bootc/kargs.d/01-my_flag.toml'
```

Должно получиться вот так:

{% hint style="danger" %}
Существует баг, пока не пофиксили, но секция install не должна быть пустой. Я поставил например tmux, можно выбрать любой пакет без разницы.
{% endhint %}

<figure><img src="../../.gitbook/assets/photo_2025-08-22_17-29-13.jpg" alt=""><figcaption></figcaption></figure>

После этого пересобираем образ с применением настроек:

```
apm s image apply
```

<figure><img src="../../.gitbook/assets/photo_2025-08-22_17-32-03.jpg" alt=""><figcaption></figcaption></figure>

Перезагружаем систему и теперь всё работает

<figure><img src="../../.gitbook/assets/photo_2025-08-22_17-33-51.jpg" alt=""><figcaption></figcaption></figure>
