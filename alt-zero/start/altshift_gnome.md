---
description: Как включить ALT+Shift в GNOME
---

# Как включить Alt+Shift в GNOME

```bash
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Shift>Alt_L']" gsettings set org.gnome.desktop.wm.keybindings switch-input-source-backward "['<Alt>Shift_L']
```

{% hint style="info" %}
Сделать это также можно на этапе установки дистрибутива. Лично я использую клавишу CapsLock, рекомендую хотя-бы попробовать, также можно выбрать на этапе установки.
{% endhint %}
