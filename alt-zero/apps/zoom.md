# Zoom



<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-12-31 17-09-03.png" alt=""><figcaption></figcaption></figure>

Flatpak

```bash
flatpak install flathub us.zoom.Zoom
```



### Баги и решения

Zoom Flatpak не запускается на Wayland сессии в GNOME

01\. Открываем файл `~/.var/app/us.zoom.Zoom/config/zoomus.conf`

02\. Добавляем строчку `enableWaylandShare=true`

03\. Запускаем повторно Zoom
