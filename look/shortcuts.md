---
description: Shortcuts GNOME
---

# Горячие клавиши

### Вариант #1

Классический вариант через утилиту conky

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-01-06 09-11-37.png" alt=""><figcaption><p>Пример как выглядит мой конфиг для conky</p></figcaption></figure>

Устанавливаем `conky`

```bash
epmi conky
```

{% hint style="info" %}
Файл конфигурации лежит здесь: `~/.config/conky/conky.conf`
{% endhint %}

<details>

<summary>Пример моего варианта конфига</summary>

```lua
conky.config = {
    alignment = 'top_left',
    background = false,
    border_width = 1,
    cpu_avg_samples = 2,
    default_color = 'white',
    default_outline_color = 'white',
    default_shade_color = 'white',
    double_buffer = true,
    draw_borders = false,
    draw_graph_borders = true,
    draw_outline = false,
    draw_shades = false,
    extra_newline = false,
    font = 'DejaVu Sans Mono:size=12',
    gap_x = 50,
    gap_y = 870,
    minimum_height = 5,
    minimum_width = 5,
    net_avg_samples = 2,
    no_buffers = true,
    out_to_console = false,
    out_to_ncurses = false,
    out_to_stderr = false,
    out_to_x = true,
    own_window = true,
    own_window_transparent = true,
    own_window_argb_visual = true,
    own_window_type = 'desktop',
    show_graph_range = false,
    show_graph_scale = false,
    stippled_borders = 0,
    update_interval = 1.0,
    uppercase = false,
    use_spacer = 'none',
    use_xft = true,
    out_to_wayland = true,
}

conky.text = [[
Nautilus - Super+1
Firefox - Super+2
Telegram - Super+3
DaVinci - Super+4
Audacity - Super+5
OBS - Super+6
Krita - Super+7
GitBook - Super+8
YT Downloader - Super+9

DaVinci Resolve

Shift + 1 - Home
Shift + 2 - Media
Shift + 3 - Edit
Shift + 4 - Fusion
Shift + 5 - Color
Shift + 6 - Fairlight
Shift + 7 - Экспорт проекта

]]
```

</details>

### Вариант #2

<figure><img src="../../.gitbook/assets/Снимок экрана от 2024-01-06 09-00-38.png" alt=""><figcaption><p>Расширение Shortcuts для GNOME</p></figcaption></figure>

{% embed url="https://extensions.gnome.org/extension/1144/shortcuts/" %}

<details>

<summary>Shortcuts конфиг</summary>

```json
[
    {
        "name": "Dash панель",
        "shortcuts": [
            {
                "key": "Super + 1",
                "description": "Nautilus"
            },
            {
                "key": "Super + 2",
                "description": "Firefox"
            },
            {
                "key": "Super + 3",
                "description": "Telegram"
            },
            {
                "key": "Super + 4",
                "description": "DaVinci"
            },
            {
                "key": "Super + 5",
                "description": "Audacity"
            },
            {
                "key": "Super + 6",
                "description": "OBS Studio"
            },
            {
                "key": "Super + 7",
                "description": "Krita"
            },
            {
                "key": "Super + 8",
                "description": "GitBook"
            }
        ]
    },            
            
{
        "name": "DaVinci Resolve",
        "shortcuts": [           
            
            {
                "key": "Shift + 2",
                "description": "Media"
            },
            {
                "key": "Shift + 4",
                "description": "Edit"
            },
            {
                "key": "Shift + 5",
                "description": "Fusion"
            },
            {
                "key": "Shift + 6",
                "description": "Color"
            },
            {
                "key": "Shift + 7",
                "description": "Fairlight"
            },
            {
                "key": "Shift + 8",
                "description": "Экспорт проекта"
            }
        ]
    },
    {
        "name": "Навигация в системе",
        "shortcuts": [
            {
                "key": "Super + Enter",
                "description": "Открыть терминал"
            },
            {
                "key": "Super+Q",
                "description": "Закрыть окно"
            },
            {
                "key": "Super + F",
                "description": "Полноэкранный режим"
            },
            {
                "key": "Super + Влево",
                "description": "Окно на рабочий стол влево"
            },
            {
                "key": "Super + Вправо",
                "description": "Окно на рабочий стол вправо"
            },   
            {
                "key": "Super + -",
                "description": "Свернуть все окна"
            }
        ]
    },
    {
        "name": "Вкладки",
        "shortcuts": [
            {
                "key": "Ctrl + T",
                "description": "Открыть новую вкладку"
            },
            {
                "key": "Ctrl + W",
                "description": "Закрыть вкладку"
            },
            {
                "key": "Ctrl + Shift + T",
                "description": "Открыть закрытую вкладку"
            },
            {
                "key": "Ctrl+L",
                "description": "Фокус строки поиска"
            }
        ]
    },
    {
        "name": "Снимок экрана",
        "shortcuts": [
            {
                "key": "Alt + Print",
                "description": "Снимок экрана"
            },
            {
                "key": "Shift + Print",
                "description": "Выделить область снимка"
            },
            {
                "key": "Ctrl + Print",
                "description": "Сделать снимок и скопировать его в clipboard"
            },
            {
                "key": "Ctrl + Alt + Shift + R",
                "description": "Захвать экрана"
            }
        ]
    }
]
```

</details>
