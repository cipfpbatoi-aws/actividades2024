---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🛠️ Sistemes de fitxers

Panell principal per a la gestió del sistema de fitxers:

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Tenim dues opcions per crear el sistema de fitxers **EFS**, en el nostre cas la versió ràpida i la versió on podem especificar més paràmetres de configuració, etc. Primer farem servir l'opció ràpida. En aquest cas, podem especificar el nom i, hem de seleccionar per a quina **VPC** ha d'estar disponible.&#x20;

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Ja tenim creat el sistema de fitxers **EFS**:

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Si accedim pel **nom** o l'identificador del sistema de fitxers **EFS** creat,  podem veure les diferents opcions i accions disponibles:

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

A continuació crearem un sistema de fitxers **EFS**, però amb l'opció "_**Personalizar**_":

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

D'aquesta forma podem ajustar diferents paràmetres:&#x20;

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

xifratge, cicle de vida, etc.:

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Més paràmetres de configuració del sistema de fitxers:

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Selecció de la **VPC** on volem tindre disponible el nostre sistema de fitxers **EFS**:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Més configuracions del sistema de fitxers **EFS**:

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Finalement hem de "_**Revisar y crear**_":

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Ara anem "muntar" el sistema de fitxers **EFS** sobre una instància, seleccionarem "_**Asociar**_"

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Diferents opcions per a muntar el sistema de fitxers **EFS**, en aquest cas fent servir **DNS**:

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

o per **IP**:

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Comprovarem el funcionament:&#x20;
