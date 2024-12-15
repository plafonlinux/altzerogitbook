# Включаем "шорткат" для Терминала

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-10-29 14-47-10.png" alt=""><figcaption><p>Команда для пакета gnome-console не аналогичная, а kgx</p></figcaption></figure>

{% hint style="warning" %}
Пакет `gnome-terminal` заменён на более современный `gnome-console`
{% endhint %}

Установка нового терминала и удаление старого:

```
sudo apt-get install gnome-console && sudo apt-get remove --purge gnome-terminal
```

{% hint style="success" %}
Команда для вызова новой Консоли не `gnome-console`, а `kgx`
{% endhint %}

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-10-29 14-52-56.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Я в последнее время использую комбинацию Super+Enter и Super+T, но общепринятый стандарт это CTRL+ALT+T
{% endhint %}

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-10-29 14-46-14.png" alt=""><figcaption><p>Для одной команды можно создавать сколько угодно команд</p></figcaption></figure>
