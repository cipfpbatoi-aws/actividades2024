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

Tenim dues opcions per crear el sistema de fitxers **EFS**, en el nostre cas la versió ràpida i la versió on podem especificar més paràmetres de configuració, etc. Nosaltres farem servir l'opció estesa on podem especificar més paràmetres.&#x20;

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

D'aquesta forma podem ajustar diferents paràmetres:&#x20;

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

xifratge, cicle de vida, etc.:

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

Més paràmetres de configuració del sistema de fitxers:

<figure><img src="../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

Selecció de la **VPC** on volem tindre disponible el nostre sistema de fitxers **EFS** i on seleccionarem el nostre security group:

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Més configuracions del sistema de fitxers **EFS**:

<figure><img src="../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

Finalement hem de "_**Revisar y crear**_":

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Abans de "muntar" el nostre sistema de fitxers, hem d'afegir al nostre grup de seguretat que permata les connexions **NFS**, per això hem d'accedir al servei ![](<../.gitbook/assets/image (7).png>) i en l'apartat **Red y Seguridad** opció  **Security Group** editar regles d'entrada:

&#x20;

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Una vegada hem afegit la regla, el nostre grup de seguretat queda de la següent forma:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Ara anem "muntar" el sistema de fitxers **EFS,** per això accedim al servei ![](<../.gitbook/assets/image (10).png>) una vegada seleccionat farem clic en "_**Asociar**_"

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

On trobem diferents opcions per a muntar el sistema de fitxers, en aquest cas fent servir **DNS**:

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

o per **IP**:

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Ara sols ens falta comprovar el funcionament en una instància, en aquest cas hem fet servir client nfs de l'opció **DNS**:

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

&#x20;
