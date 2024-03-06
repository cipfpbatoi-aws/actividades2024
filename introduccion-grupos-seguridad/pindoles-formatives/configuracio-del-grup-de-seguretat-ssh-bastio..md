---
description: Configuració del grup de seguretat 'ssh-bastio'.
---

# ⚒️ Configuració del grup de seguretat 'ssh-bastio'.

A continuació, configurarem el grup de seguretat 'ssh-bastio', que permetrà el tràfic d'entrada al port TCP/22 (SSH), des de qualsevol IP, a les instàncies que apliquen el grup de seguretat.&#x20;

Dins de la pàgina de grups de seguretat, polsem el botó "Crear nou grup de seguretat".

<figure><img src="../.gitbook/assets/image (158).png" alt=""><figcaption><p>Llistat de grups de seguretat</p></figcaption></figure>

Introduïm les dades bàsiques del grup de seguretat 'internet' (nom, descripció i VPC).

<figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption><p>Configuració del nom i la descripció</p></figcaption></figure>

Configurem la regla d'entrada requerida, habilitant la connexió al port TCP/22 (SSH) des de qualsevol IP.

<figure><img src="../.gitbook/assets/image (164).png" alt=""><figcaption><p>Regles d'entrada</p></figcaption></figure>

Deixem el panell de regles d'eixida buit.

<figure><img src="../.gitbook/assets/image (165).png" alt=""><figcaption><p>Regles d'eixida</p></figcaption></figure>

I polsem sobre el botó 'Crear grup de seguretat' per a finalitzar la configuració.&#x20;

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption><p>Confirmació de la creació del grup de seguretat</p></figcaption></figure>

Tornarem al llistat de grups de seguretat, a on podrem comprovar que el grup de seguretat s'ha creat correctament.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>Llistat de grups de seguretat</p></figcaption></figure>

