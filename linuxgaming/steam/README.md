---
description: Самая крутая игровая платформа для Линукса
---

# Steam

<figure><img src="../../../.gitbook/assets/1634980031764.jpg" alt=""><figcaption><p>Steam запущенный на GNU/Linux</p></figcaption></figure>

### Установка:

Обычная версия

```
epm play steam
```

<details>

<summary>Если Steam постоянно просит пароль от рута!</summary>

```bash
sudo gedit /etc/polkit-1/rules.d/10-steam-nm.rules
```

```bash
polkit.addRule(function(action, subject) {
    if (action.id == "org.freedesktop.NetworkManager.settings.modify.system" &&
        subject.process.binary.indexOf("steam") !== -1) {
      return polkit.Result.NO;
    }
});
```

</details>

Flatpak версия

```bash
flatpak install flathub com.valvesoftware.Steam
```

### Включаем мониторинг игр MangoHud в Steam Flatpak

<figure><img src="../../../.gitbook/assets/overlay_example.gif" alt=""><figcaption></figcaption></figure>

```bash
flatpak install org.freedesktop.Platform.VulkanLayer.MangoHud
```

Включить для всех игр разом:

```bash
flatpak override --user --env=MANGOHUD=1 com.valvesoftware.Steam
```

Отключить для всех игр разом:

```bash
flatpak override --user --env=MANGOHUD=0 com.valvesoftware.Steam
```

Включить отдельно для каждой игры в Steam (Vulkan + OpenGL):

```bash
mangohud %command%
```

Включить отдельно для каждой игры в Steam (только Vulkan):

```bash
MANGOHUD=1
```

### Чтобы заработало на Flatpak версии Steam:

**Метод 01:** Поместим наш конфиг в папку `.var`

```bash
~/.var/app/com.valvesoftware.Steam/config/MangoHud/MangoHud.conf
```

**Метод 02:** Или дадим доступ Steam (Flatapk) к нашему хосту:

```bash
flatpak override --user --filesystem=xdg-config/MangoHud:ro com.valvesoftware.Steam
```

### Включаем Proton (Steam Play) для запуска игр на линуксе

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 10-53-32.png" alt=""><figcaption><p>Steam Play включает Proton</p></figcaption></figure>

### Кэш шейдеров улучшает плавность игры

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 10-55-01.png" alt=""><figcaption></figcaption></figure>

### Дополнительные параметры запуска (ProtonDB) вставляются здесь:

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 10-56-36.png" alt=""><figcaption></figcaption></figure>

### Мой диск не видно в Steam из Flatpak

Добавляем путь до нашего `диска/каталога` в утилите `Flatseal`

```bash
flatpak install flathub com.github.tchx84.Flatseal
```

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 10-59-55.png" alt="flatseal steam flatpak"><figcaption><p>Добавляем нужный каталог в Steam Flatpak через утилиту Flatseal</p></figcaption></figure>

Например у меня это диск примонтированный как каталог `/games`&#x20;

## Проблемы и баги на ALT Linux

### 01. Перестали запускаться игры через Proton в Steam Flatpak на ALT Linux (нативные игры работают)

<details>

<summary>Описание проблемы в Телеграме</summary>

\#1 [https://t.me/plafonyoutube/3350](https://t.me/plafonyoutube/3350)

\#2 [https://t.me/plafonyoutube/3351](https://t.me/plafonyoutube/3351)

\#3 [https://t.me/plafonyoutube/3352](https://t.me/plafonyoutube/3352)

</details>

Для начала можно попробовать это:

```bash
sudo sysctl user.max_user_namespaces=99999999
```

Если не помогло, то уже сюда:

## <mark style="color:red;">Решение</mark> [<mark style="color:blue;">здесь</mark>](https://plafon.gitbook.io/alt-zero/alt-zero/apps/flatpak#problema-s-bubblewrap-na-alt-linux-or-ne-zapuskayutsya-flatpak-prilozheniya)<mark style="color:red;">.</mark>
