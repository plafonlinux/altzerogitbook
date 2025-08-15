---
description: Лучший видеоредактор
---

# DaVinci Resolve

<figure><img src="../.gitbook/assets/uOxMCNPt3TI.jpg" alt=""><figcaption></figcaption></figure>

## Качаем и устанавливаем сам DaVinci Resolve

<figure><img src="../.gitbook/assets/Снимок экрана от 2022-10-30 18-20-53.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.blackmagicdesign.com/products/davinciresolve" %}

Распаковываем скачанный архив

```bash
cd ~/Downloads
```

```bash
unzip DaVinci_Resolve_18.0.4_Linux.zip
```

Устанавливаем DaVinci Resolve 18

```bash
./DaVinci_Resolve_18.0.4_Linux.run -i
```

{% hint style="info" %}
Для ребят с видеокартами от NVIDIA на этом всё. Приятного творчества!
{% endhint %}

## ДЛЯ ВИДЕОКАРТ AMD RADEON

### Доустанавливаем этот пакет:

```bash
sudo apt-get isntall libGLU
```

```bash
sudo apt-get install ffmpeg
```

```bash
sudo apt-get install rocm-opencl-runtime 
```

```bash
sudo apt-get install hip-runtime-amd
```

{% hint style="success" %}
Теперь всё и для лагеря "красных"! Приятного творчества и нам :tada::clap:
{% endhint %}

<figure><img src="../.gitbook/assets/Снимок экрана от 2022-11-01 09-39-04.png" alt="amd radeon fedora linux mesa opencl"><figcaption><p>Видеокарта AMD Radeon отображается корректно в Fedora Linux</p></figcaption></figure>

Проверяем всё ли работает утилитой `clinfo`

```
epmi clinfo
```

```bash
clinfo
```

```bash
Number of platforms                               1
  Platform Name                                   AMD Accelerated Parallel Processing
  Platform Vendor                                 Advanced Micro Devices, Inc.
  Platform Version                                OpenCL 2.1 AMD-APP (3452.0)
  Platform Profile                                FULL_PROFILE
  Platform Extensions                             cl_khr_icd cl_amd_event_callback 
  Platform Extensions function suffix             AMD
  Platform Host timer resolution                  1ns

  Platform Name                                   AMD Accelerated Parallel Processing
Number of devices                                 1
  Device Name                                     gfx1010:xnack-
  Device Vendor                                   Advanced Micro Devices, Inc.
  Device Vendor ID                                0x1002
  Device Version                                  OpenCL 2.0 
  Driver Version                                  3452.0 (HSA1.1,LC)
  Device OpenCL C Version                         OpenCL C 2.0 
  Device Type                                     GPU
  Device Board Name (AMD)                         AMD Radeon RX 5700 XT
  Device PCI-e ID (AMD)                           0x731f
  Device Topology (AMD)                           PCI-E, 0000:0c:00.0
  Device Profile                                  FULL_PROFILE

................
```





## Баги и ошибки

{% hint style="warning" %}
Как посмотреть почему не запускается DaVinci Resolve на Linux ?

Достаточно в терминале выполнить: `/opt/resolve/bin/resolve`
{% endhint %}





### Ошибка: `/lib64/libgdk_pixbuf-2.0.so.0`

```bash
/opt/resolve/bin/resolve: symbol lookup error: /lib64/libgdk_pixbuf-2.0.so.0: undefined symbol: g_task_set_static_name
```

<figure><img src="../.gitbook/assets/Снимок экрана от 2024-05-01 11-54-39.png" alt=""><figcaption></figcaption></figure>

### Решение:

```bash
sudo rm -rf /opt/resolve/libs/libglib-2.0.so* && sudo rm -rf /opt/resolve/libs/libgio-2.0.so* && sudo rm -rf /opt/resolve/libs/libgmodule-2.0.so*
```

### Ошибка: libpango undefined symbol: g\_string\_free\_and\_steal <a href="#post-title-t3_12z32r1" id="post-title-t3_12z32r1"></a>

{% hint style="info" %}
Код ошибки:&#x20;

```
./resolve: symbol lookup error: /lib64/libpango-1.0.so.0: undefined symbol: g_string_free_and_steal
```
{% endhint %}

### Удалить все по запросу `glib` в папке /opt/resolve/libs

<figure><img src="../.gitbook/assets/Снимок экрана от 2024-03-16 22-40-23.png" alt=""><figcaption></figcaption></figure>







































## <mark style="color:red;">Архив ошибок</mark>

### РЕШЕНО: DaVinci не запускается на версии ядра 6.6.\*

<figure><img src="../.gitbook/assets/Снимок экрана от 2023-12-17 22-57-37.png" alt=""><figcaption></figcaption></figure>

Решение:

Перейти на версию ядра LTS, я перешёл на un-std

<figure><img src="../.gitbook/assets/Снимок экрана от 2023-12-18 22-39-53.png" alt=""><figcaption></figcaption></figure>
