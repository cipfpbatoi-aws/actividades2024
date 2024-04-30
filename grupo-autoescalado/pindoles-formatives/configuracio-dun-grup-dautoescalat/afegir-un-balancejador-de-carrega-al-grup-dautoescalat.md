---
description: Afegir un balancejador de càrrega al grup d'autoescalat
---

# ⚒️ Afegir un balancejador de càrrega al grup d'autoescalat

Després d'estressar les nostres instàncies, disposem de tres rèpliques, cadascuna en la seu apropia IP pública.

Per a disposar d'un únic punt d'entrada a l'aplicació, podem afegir un balancejador de càrrega a les nostres instàncies, de manera que amb una única IP pública, puguem accedir al servei, encara que les instàncies canvien.&#x20;

Al panell EC2, seleccionem l'opció 'grups d'autoescalat', i al llistat seleccionem el grup d'autoescalat, i prenem el botó editar del menú opcions.

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

Busquem l'opció 'balancejadors de càrrega' i prenem el botó 'agregar un nou balancejador de càrrega'.

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

Com que la nostra aplicació exposa un script php pel port 80, seleccionem Application Load Balancer. i com que volem accedir des d'internet, seleccionem internet-facing.

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

A l'opció 'reenviar a', creem un nou grup de destí.

<figure><img src="../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

I prenem el botó actualitzar, a sota de la pàgina.&#x20;

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

Si naveguem a l'opció 'Balancejadors de càrrega' del panell EC2, podrem observar el nou balancejador de càrrega, i si el seleccionem, podrem visualitzar les seues propietats, com ara, la DNS pública generada.&#x20;

<figure><img src="../../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure>

Esperem que finalitze la seua inicialització, i provem l'accés al servei, amb la DNS generada.

<figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure>

Executa diverses peticions, i observa com cada vegada respon un servidor del grup d'autoescalat.

<figure><img src="../../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure>
