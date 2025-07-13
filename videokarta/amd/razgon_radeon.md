---
description: Как включить разгон на AMD?!
---

# Разгон видеокарты AMD

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 13-41-07.png" alt=""><figcaption><p>CoreCTRL</p></figcaption></figure>

`amdgpu.ppfeaturemask=0xffffffff`

`radeon.cik_support=0 amdgpu.cik_support=1`

Параметры выше, нужно добавить через пробел в `/etc/sysconfig/grub2`

```bash
sudo gnome-text-editor /etc/sysconfig/grub2
```

Должно получится примерно так (_**кавычки важны!**_):

{% hint style="info" %}
Пример:&#x20;

```
GRUB_CMDLINE_LINUX_DEFAULT='quiet splash ваш_пункт1 ваш_пункт2'
```
{% endhint %}

```bash
GRUB_CMDLINE_LINUX_DEFAULT='usbcore.autosuspend=-1 quiet panic=30 splash amdgpu.ppfeaturemask=0xffffffff radeon.cik_support=0 amdgpu.cik_support=1'
```

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-06-11 19-46-31.png" alt=""><figcaption></figcaption></figure>

И пересобираем GRUB чтобы закрепить новые параметры, командой:

```bash
sudo update-grub
```

{% hint style="success" %}
Перезапускаем ПК, опции разгона должны активироваться!
{% endhint %}

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-06-11 19-48-21.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.altlinux.org/Grub" %}
