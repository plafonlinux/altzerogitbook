# Droidcam

## DroidCam[​](https://alt-gnome.wiki/droidcam.html#droidcam) <a href="#droidcam" id="droidcam"></a>

DroidCam — приложение, позволяющее превратить ваше мобильное устройство в веб-камеру компьютера.

<figure><img src="https://alt-gnome.wiki/droidcam/droidcam-1.png" alt="Droidcam"><figcaption></figcaption></figure>

### Установка из репозитория[​](https://alt-gnome.wiki/droidcam.html#%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-%D0%B8%D0%B7-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D1%8F) <a href="#ustanovka-iz-repozitoriya" id="ustanovka-iz-repozitoriya"></a>

```bash
epmi droidcam
```

### Настройка DroidCam[​](https://alt-gnome.wiki/droidcam.html#%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B8%D0%BA%D0%B0-droidcam) <a href="#nastroika-droidcam" id="nastroika-droidcam"></a>

DroidCam требует модуль ядра `v4l2loopback`, который можно установить через терминал:

```bash
epmi kernel-modules-v4l2loopback-***
```

`***` - версия ядра `un-def` или `std-def`. Узнать нужную версию через терминал

```bash
uname -r
```

Необходимо включить установленный модуль. Для этого нужно отредактируйте файл `/etc/modules-load.d/modules.conf`

```bash
sudo nano /etc/modules-load.d/modules.conf
```

В конце файла перейдите на новую строку и добавьте `v4l2loopback`

<figure><img src="https://alt-gnome.wiki/droidcam/v4l2loopback.gif" alt="v4l2loopback_module"><figcaption></figcaption></figure>

Выйти из Nano можно нажав `Ctrl + X` и согласившись с сохранением изменений. После этого обязательно перезагрузите устройство.

Готово! DroidCam успешно настроен и готов к работе.



## Источник:

{% embed url="https://alt-gnome.wiki/droidcam.html#%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B8%D0%BA%D0%B0-droidcam" %}
