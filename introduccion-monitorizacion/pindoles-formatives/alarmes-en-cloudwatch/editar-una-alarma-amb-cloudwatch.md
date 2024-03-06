# ⚒️ Editar una alarma amb CloudWatch

Una vegada dins de la consola de CloudWatch, observaràs diverses opcions a l'esquerra. Selecciona "Alarmes" del menú per accedir a la llista de totes les alarmes configurades.

En la llista de les teues alarmes, podràs veure totes les alarmes existents. Utilitza el filtre de la part superior si tens moltes alarmes i necessites trobar-ne una específica.

Una vegada trobada l'alarma que vols editar, selecciona-la fent clic en el seu nom.

<figure><img src="../../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

A la pàgina de configuració de l'alarma, observaràs diverses pestanyes com ara "Visió general", "Mètriques", "Definició d'alarma", "Accions" i altres.

Fes clic a "Accions" i selecciona "Editar" per començar a modificar la configuració de l'alarma seleccionada.

<figure><img src="../../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>

&#x20;Ara que ets a la pàgina d'edició de l'alarma, podràs veure tots els detalls de la configuració actual.

Pots modificar el nom de l'alarma, la descripció i altres metadades per identificar l'alarma fàcilment.

<figure><img src="../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

La part més important de l'edició d'una alarma és la configuració de les condicions que la disparen.

En aquesta secció, pots ajustar els valors umbrals per a les mètriques que l'alarma està supervisant.

* **Definició de Mètrica**: Selecciona la mètrica que vols supervisar (com ara CPU, tràfic de xarxa, errors de servidor, etc.).
* **Condicions**: Defineix si vols que l'alarma s'activi quan la mètrica és "superior a", "inferior a", "igual a", etc.
* **Valor**: Estableix el límit que dispara l'alarma. Per exemple, si supervises la CPU, pots posar un límit del 80% per rebre una notificació quan la CPU superi aquest límit.

<figure><img src="../../.gitbook/assets/image (188).png" alt=""><figcaption><p>Condicions de la mètrica.</p></figcaption></figure>

Un cop configurades les condicions, pots especificar les accions que es realitzen quan l'alarma es dispara.

* **Accions de Notificació**: Decideix si vols rebre una notificació per correu electrònic, missatge de text, o activar altres serveis com AWS Lambda.
* **Sistemes d'Accions**: Configura els passos que s'han de seguir en cas que l'alarma es dispare. Per exemple, pot reiniciar una instància o tancar un servidor.

<figure><img src="../../.gitbook/assets/image (189).png" alt=""><figcaption><p>Notificació.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption><p>Accions a realitzar sobre la EC2</p></figcaption></figure>

Quan estigues satisfet amb tots els ajustos, fes clic en "Guardar canvis" per aplicar les modificacions a l'alarma.

Torna a la llista d'alarmes per verificar que els canvis s'han aplicat correctament i que l'alarma està configurada com desitges.

Recorda revisar periòdicament les teues alarmes per assegurar-te que encara s'ajusten a les teues necessitats de monitoratge i notificació.

Pots repetir aquest procés per modificar altres alarmes o crear-ne de noves segons evolucionen les teues necessitats en AWS.
