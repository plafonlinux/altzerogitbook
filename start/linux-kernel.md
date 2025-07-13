---
description: Всё что вам нужно знать про настройку ядра
---

# Linux Kernel

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

## Удаляем неиспользуемые ядра

```bash
sudo apt-get remove-old-kernels
```

## Как скачать заголовки (kernel-headers)

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Ищем доступные заголовки в репозитории:

```
epms kernel-headers
```

Смотрим какие доступны и устанавливаем в зависимости от своего ядра (например для ядра 6.12):

```
epmi kernel-headers-6.12
```

```
epmi kernel-headers-modules-6.12
```

{% hint style="info" %}
Перезапускаем ПК
{% endhint %}

## Как поменять версию ядра (GUI)

{% hint style="info" %}
Для взаимодействия с ядрами в дистрибутиве ALT Linux, существуем фирменная утилита "Центр управления"
{% endhint %}

<div><figure><img src="../.gitbook/assets/Снимок экрана от 2023-06-10 10-03-07.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Снимок экрана от 2023-06-10 10-03-11.png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/Снимок экрана от 2023-06-10 10-03-27.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="success" %}
Выбираем в утилите доступную версию ядра, необходимые модули и нажимаем "Обновить ядро".
{% endhint %}

Далее

{% hint style="success" %}
Перезагружаем ПК
{% endhint %}
