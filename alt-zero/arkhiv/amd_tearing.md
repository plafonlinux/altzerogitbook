---
description: Только для X.org
---

# Убираем тиринг на AMD (X11)

{% hint style="info" %}
Тиринг, если в двух словах это “разрыв” картинки, который очень часто встречается на Линуксе. Все дело в устаревшей технологии дисплейного менеджера X.Org, который в ближайшие годы будет заменен полностью, на современную реализацию Wayland.
{% endhint %}

<figure><img src="../../.gitbook/assets/Tearing-dello-schermo-o-input-lag.jpg" alt=""><figcaption><p>Пример тиринга</p></figcaption></figure>

```bash
sudo gedit /etc/X11/xorg.conf.d/20-amdgpu.conf
```

и вставляем:

```bash
Section "Device"
Identifier "AMD"
Driver "amdgpu"
Option "TearFree" "true"
Option "DRI" "3"
EndSection
```

###

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-08-18 08-48-09.png" alt=""><figcaption></figcaption></figure>

### Тест на тиринг

{% embed url="https://www.youtube.com/watch?v=5xkNy9gfKOg" %}
