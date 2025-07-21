---
description: Лезем под капот GNOME
---

# Dconf Editor

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

01\. Чтобы экспортировать все изменённые настройки с Dconf&#x20;

```bash
dconf dump / > ~/gnome-full-settings-backup.dconf
```

02\. Чтобы импортировать свой конфиг

```
dconf load / < ~/gnome-full-settings-backup.dconf
```
