# 🔨 Pràctica EBS

En aquesta pràctica crearem un RAID1 amb dos discos que afegirem a una instància EC2 GNU/Linux. Una vegada funcionant, verificarem en altra instància que podem recuperar un RAID1 amb un sols disc.

Per aquesta pràctica ens faran falta 2 instàncies GNU/Linux.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

Abans de res ens farà falta crear dos volums, per això accedirem a l'apartat "**Elastic Block Store**"

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

Seleccionarem "_**Crear volumen**_**"** i afegirem dos volums, com és per a dur a terme una prova no cal un disc gran:&#x20;

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

Com podem veure en la captura anterior tenim els dos volums "**Disponible**", per poder fer servir aquest disc hem d'associar-los en alguna instància.

Accedim al primer disc i fem clic en "_**Asociar volumen**_" :

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Ara hem de triar en quina instància volem fer servir aquest volumn: &#x20;

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

En aquest pas també hem de decidir en quin nom volem que es mostre el volum:&#x20;

&#x20;

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

Ara sols ens queda disponible un volum:

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

Ara farem el mateix, però assignarem altre nom de dispositiu:&#x20;

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

Finalment, podem veure que no tenim cap volum **EBS**, disponible:

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

Ara ja tenim disponibles en la nostra instància els dos volums **EBS**:

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Crearem un RAID1 amb els dos volums que hem afegit, primer que res instal·larem el suport **mdadm** a la nostra instància:&#x20;

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



