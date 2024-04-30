---
description: Prova del grup d'autoescalat
---

# ⚒️ Prova del grup d'autoescalat

El nostre grup d'autoescalat està configurat per mantindre almenys 1 rèplica, i afegir rèpliques fins a 5, en cas que augmente la càrrega del processador de les rèpliques en execució.

Com que a l'estat inicial, soles tindrem una instància en execució, podem provar que almenys manté una instància, terminant la instància existent.&#x20;

<figure><img src="../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

Si refresquem el llistat, podrem observar com, passats uns segons, s'inicia una nova instància del nostre grup d'autoescalat.&#x20;

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

A continuació, provarem l'escalat horitzontal, estressant el processador de la màquina desplegada.

{% hint style="info" %}
Per comoditat, farem servir l'aplicació de consola stress, executada amb ssh.
{% endhint %}

En primer lloc, localitzem la IP pública de la màquina a estressar.

<figure><img src="../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

I executem els següents comandaments, fent servir la clau privada de la màquina.

```
ssh -i certificado.pem ubuntu@ip_publica sudo apt install -y stress &;
ssh -i certificado.pem ubuntu@ip_publica stress --cpu 999 --timeout 3600 &;

```

Si refresquem el panell EC2, podem observar les dades de la nova rèplica, iniciada per la càrrega del processador.&#x20;

<figure><img src="../../.gitbook/assets/image (248).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Prova a carregar la nova instancia, i observa com arranca una tercera.&#x20;
{% endhint %}
