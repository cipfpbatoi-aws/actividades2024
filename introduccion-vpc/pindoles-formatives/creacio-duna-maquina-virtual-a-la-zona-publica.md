# ⚒️ Creació d'una màquina virtual a la zona pública

Per a provar la connectivitat de la zona pública, desplegarem una instància nova amb Ubuntu Server, i connectarem amb SSH a la IP pública assignada.&#x20;

Al buscador de serveis, introduïm 'EC2', i seleccionem l'opció corresponent.

<figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

Al panell EC2, polsarem sobre l'enllaç 'Instàncies'.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

I polsem el botó 'Llançar instància'

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

La consola d'AWS ens mostrarà el formulari per a la configuració d'una nova màquina virtual.

Introduïm el nom de la nova instància.

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

Seleccionem el sistema operatiu que volem tindre instal·lat a la instància, així com l'arquitectura.

<figure><img src="../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

Continuem amb la selecció del tipus d'instància, que determinarà les capacitats de la màquina virtual (tipus de CPU, quantitat de CPU virtuals, quantitat de memòria).

<figure><img src="../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

Seleccionem el parell de claus RSA que volem fer servir per a connectar-nos a la instància (per aquest exemple, podem fer servir el parell de claus 'vockey', creats automàticament pel laboratori).

<figure><img src="../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

A continuació, editem la configuració de xarxa de la nova instància, polsant el botó 'editar' de la secció corresponent.

<figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

Hem de seleccionar:

* VPC: smx-vpc (creada anteriorment a aquest tema).
* Subnet: smx-subnet-public... (subxarxa pública de smx-vpc).
* Auto-assign public IP: enable (ens assignarà una IP publica automàticament)&#x20;
* Create security group (perquè encara no hem creat cap)
* Security group name: smx-ssh-all
* Description: permet connexions SSH des de qualsevol IP&#x20;

<figure><img src="../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

La resta d'opcions del security group les deixem per defecte.

<figure><img src="../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

Deixem les opcions de configuració d'emmagatzemament per defecte, i polsem sobre el botó 'llançar instància'.

<figure><img src="../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

Tornem al panell d'instàncies EC2, i esperem que la instància finalitze el seu desplegament.

<figure><img src="../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

Mentre la instància finalitza la seua inicialització, podem observar les IP assignades (tant la pública com la privada).

<figure><img src="../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

Com que la màquina virtual té assignada una IP pública, podem connectar a la mateixa des de qualsevol client SSH, fent servir la clau privada 'vockey' generada amb el laboratori.

Per descarregar la clau privada, podem accedir al panell d'AWS Academy, en el que hem iniciat el laboratori, polsar sobre l'enllaç 'AWS Details', i descarregar la clau privada, en format PEM o PPK.

<figure><img src="../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

Una volta descarregada, podem connectar amb el nostre client SSH preferit.

<figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

O podem fer servir el terminal web inclòs a AWS Academy (en aquest cas hem de fer servir la clau privada \~/.ssh/labuser.pem).

<figure><img src="../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>

Una volta connectats a la màquina virtual, podem provar si existeix connectivitat amb internet, per exemple, executant un apt update.

<figure><img src="../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>
