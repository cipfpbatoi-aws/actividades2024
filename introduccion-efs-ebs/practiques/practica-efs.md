# 📎 Pràctica EFS

L'objectiu d'aquesta pràctica es compartir una carpeta EFS amb dues instàncies **EC2**. En aquest cas una instància serà un GNU/Linux i l'altra instància un M$. Windows Server 2022.

Ja tenim les 2 instàncies EC2 en funcionament:

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Ara crearem un sistema de fitxers EFS, i per això hem d'accedir al servei ![](<../.gitbook/assets/image (33).png>)

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

Seleccionarem "_**Crear un sistema de archivos**_". Podem especificar un nom i hem d'assegurar-nos en quina **VPC** tenim les nostres instàncies per assignar aquesta a l'**EFS** que crearem.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

EFS creat:

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
