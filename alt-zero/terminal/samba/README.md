---
description: Установка Samba в ALT Linux
---

# Samba

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-08-18 11-14-52.png" alt=""><figcaption></figcaption></figure>

```bash
sudo apt-get install samba samba-client gvfs-shares gvfs-backends -y
```

Опции монтирования NFS

```sh
_netdev,nofail,user,exec,x-gvfs-show
```
