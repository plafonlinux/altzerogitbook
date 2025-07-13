---
description: Управление виртуальными машинами
---

# QEMU (Virt-manager)

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-08-18 09-16-49.png" alt=""><figcaption></figcaption></figure>

Установка инструмента libvirt

```bash
sudo apt-get install libvirt libvirt-kvm
```

```bash
sudo gpasswd -a user vmusers
```

{% hint style="warning" %}
Меняем `user` на своё имя пользователя в системе
{% endhint %}

Включаем libvirt

```bash
sudo systemctl enable libvirtd
```

```bash
sudo systemctl start libvirtd
```

```bash
sudo apt-get install qemu
```

```bash
sudo apt-get install virt-manager
```



{% embed url="https://www.altlinux.org/Libvirt_(Qemu%2BKVM%2BVirt-manager)" %}
