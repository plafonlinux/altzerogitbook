---
description: Меняем цвет папок в системе
---

# Цветные папки

<figure><img src="../../.gitbook/assets/VzbB5JC-7UI.jpg" alt=""><figcaption></figcaption></figure>

```bash
sudo apt-get install papirus-folders
```

или через EPM

```bash
epmi papirus-folders
```

### Меняем стиль иконок, выбрав нужное **название** из таблицы:

<figure><img src="../../.gitbook/assets/YtzjD05eaes.jpg" alt=""><figcaption></figcaption></figure>

```
papirus-folders -C adwaita --theme Papirus-Dark
```

### Узнать какой стиль применен сейчас в системе:

```
papirus-folders -l --theme Papirus-Dark
```

### Вернуть дефолтные папки:

```
papirus-folders -D --theme Papirus-Dark
```
