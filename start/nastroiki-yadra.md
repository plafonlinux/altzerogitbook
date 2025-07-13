---
description: Всё что вам нужно знать про настройку ядра
---

# Настройки ядра

## Удаляем неиспользуемые ядра

```bash
sudo apt-get remove-old-kernels
```

## Как скачать заголовки (kernel-headers)

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

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
