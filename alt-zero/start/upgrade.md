---
description: Полное обновление системы ALT Linux
---

# Обновление системы

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/start/sudo" %}
Обязательно включаем данный пункт
{% endembed %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 09-00-14.png" alt=""><figcaption></figcaption></figure>

### Стандартный метод

```bash
sudo apt-get update
```

```bash
sudo apt-get dist-upgrade
```

```bash
sudo update-kernel
```

```bash
sudo apt-get clean
```

{% hint style="success" %}
При желании, можно перезапустить ПК, когда у вас появится свободная минутка.
{% endhint %}

### Либо можно одной командой посредством EPM

```
epm update && epm full-upgrade
```

### Можно использовать кастомный Alias

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/terminal/alias" %}

У меня в системе, например, алиас `up`:

```bash
alias up="sudo apt-get update && sudo apt-get dist-upgrade -y && sudo update-kernel && flatpak update -y && sudo apt-get clean"
```

или посредством EPM

```bash
alias up="epm update && epm full-upgrade"
```

{% embed url="https://plafon.gitbook.io/alt-zero/alt-zero/start/epm" %}
