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

Crearem un **RAID 1** amb els dos volums que hem afegit, primer que res instal·larem el suport **mdadm** a la nostra instància:&#x20;

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Creem el **RAID 1**:

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

Afegim el **RAID** al fitxer de configuració:

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

Verifiquem el **RAID**:

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

A continuació donem format al nou **RAID**:

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

Verifiquem que podem muntar el **RAID**:

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

Ens descarregarem un fitxer per tindre contingut al RAID:

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

Ara "desassociarem" un dels dos discos assignats a la primera instància:

<figure><img src="../.gitbook/assets/Screenshot from 2024-04-21 08-39-41.png" alt=""><figcaption></figcaption></figure>

Per associar a la nova a instància, on especificarem a quina instància i el nom del disc:

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

Ara ja tenim accessible el disc en la nostra instància.&#x20;

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

Amb el comandament mdadm reconstruïm el RAID1 i podem veure&#x20;

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
