# 🛠️ Volúmenes

La gestió dels volums la farem des d'aquest apartat:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Com podeu comprovar tenim els dos volums que fan referència a les dues instàncies **EC2** que tenim en aquest moment.&#x20;

A continuació crearem un volum, la següent imatge mostra com les principals característiques que podem ajustar (el tipus de volum, la mida, les zones, el xifratge, entre altres). &#x20;

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Depenent de quin ús farem servir el volum, seleccionarem el tipus. Nosaltres en aquest cas farem servir el d'ús general.&#x20;

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Una vegada seleccionats les principals característiques podem crear el volum.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Així es mostra el volum creat:&#x20;

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Una vegada creat podem assignar-li un nom i d'aquesta manera poder identificar-lo:

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Si seleccionem un **volum** i fem clic en l'opció "_**Acciones**_" veurem les diferents accions que podem fer:

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

Ara associarem un volum a una instància. Seleccionem a quina instància i el nom del dispositiu que tindrà en la nostra instància, encara que després canviarà el nom com diu l'avís. &#x20;

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Ara podem veure que tots els volums estan en ús:

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

I si volem associar un volum que està en ús a una instància no ens deixa, primer hem de "_desassociar_" abans aquest:

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

A continuació anem a veure el volum creat en la instància EC2:

