---
description: Как подключить Xbox контроллер в ALT Linux
---

# Xbox контроллер

<figure><img src="../../.gitbook/assets/1634980031764 (1).jpg" alt=""><figcaption></figcaption></figure>

### - Драйвер для этого _Wireless донгла_, называется **xone**

{% embed url="https://github.com/medusalix/xone" %}

**Установка:**

01\. Устанавливаем заголовки ядра

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

```
epms kernel-headers
```

Смотрим какие заголовки доступны и устанавливаем их

```
epmi kernel-headers-6.12
```

```
epmi kernel-headers-modules-6.12
```

{% hint style="info" %}
Перезапускаем ПК
{% endhint %}

02\. Начинаем установку драйвера

```bash
cd ~/Загрузки
```

```bash
epmi git
```

```bash
git clone https://github.com/medusalix/xone
```

```bash
cd xone
```

```bash
epmi dkms
```

```bash
sudo ./install.sh --release
```

```bash
cd install && sudo sh firmware.sh
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-06-10 16-15-28.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Перезапускаем ПК и должно всё заработать, геймпад законектится и перестанет мигать! 😎👌
{% endhint %}
