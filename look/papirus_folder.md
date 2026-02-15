---
description: Меняем цвет папок в системе
---

# Цветные папки

<figure><img src="../.gitbook/assets/VzbB5JC-7UI.jpg" alt=""><figcaption></figcaption></figure>

### Меняем стиль иконок, выбрав нужное **название** из таблицы:

<figure><img src="../.gitbook/assets/YtzjD05eaes.jpg" alt=""><figcaption></figcaption></figure>

```
papirus-folders -C adwaita --theme Papirus-Dark
```

### Узнать какой стиль применен сейчас в системе:

```
papirus-folders -l --theme Papirus-Dark
```

### Список доступых стилей для папок:

```
papirus-folders -l
```

<figure><img src="../.gitbook/assets/Снимок экрана от 2026-02-15 12-12-22.png" alt=""><figcaption></figcaption></figure>

### Вернуть дефолтные папки:

```
papirus-folders -D --theme Papirus-Dark
```
