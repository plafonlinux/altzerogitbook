---
description: Скринкаст комбайн
---

# OBS Studio

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 10-59-04.png" alt=""><figcaption></figcaption></figure>

Установить OBS Studio в ALT Linux

```bash
sudo apt-get install obs-studio
```

через EPM

```bash
epmi obs-studio
```

Flatpak

```bash
flatpak install flathub com.obsproject.Studio
```





Плагины для OBS Studio

```bash
sudo apt-get install obs-studio-plugin-droidcam
```

```bash
sudo apt-get install obs-studio-plugin-vaapi
```

```bash
sudo apt-get install obs-studio-plugin-input-overlay
```

```bash
sudo apt-get install obs-studio-plugin-multi-rtmp
```





Droidcam для ALT Linux

```bash
sudo apt-get install droidcam
```

или через EPM

```
epmi droidcam
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-08-09 11-04-58.png" alt=""><figcaption></figcaption></figure>

Запуск Droidcam

```bash
sudo modprobe v4l2loopback
```
