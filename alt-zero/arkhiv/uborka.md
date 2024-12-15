# Удаляем ненужный "мусор"

{% hint style="info" %}
Изначально в версии ALT GNOME Regular очень много ненужных пакетов и игр, удаляем их в одну проверенную команду.
{% endhint %}

```bash
apt-get remove --purge epiphany epiphany-data cpu-x gnome-shell-extensions gnome3-minimal gnome-maps mc
```

{% hint style="danger" %}
Даже если какие-то пакеты уже были удалены из новых сборок ALT GNOME Regular, терминал пропустит их и удалит всё остальное.
{% endhint %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-10-28 14-19-49.png" alt=""><figcaption><p>ALT Gnome Regular Sisyphus | Альт GNOME Регулярка Сизиф</p></figcaption></figure>
