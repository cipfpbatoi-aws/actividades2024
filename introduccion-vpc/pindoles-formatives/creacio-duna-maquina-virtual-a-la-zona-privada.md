# ⚒️ Creació d'una màquina virtual a la zona privada

Per a provar la connectivitat de la zona privada, desplegarem una instància nova amb Ubuntu Server.&#x20;

Al buscador de serveis, introduïm 'EC2', i seleccionem l'opció corresponent.

<figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

Al panell EC2, polsarem sobre l'enllaç 'Instàncies'.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

I polsem el botó 'Llançar instància'

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

La consola d'AWS ens mostrarà el formulari per a la configuració d'una nova màquina virtual.

Introduïm el nom de la nova instància.

<figure><img src="../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

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
* Subnet: smx-subnet-private1... (subxarxa privada de smx-vpc).
* Auto-assign public IP: disable (no volem IP pública).
* Select existing security group
* Security group: smx-ssh-all (que permetia connectar via SSH des de qualsevol IP)

<figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

Deixem les opcions de configuració d'emmagatzemament per defecte, i polsem sobre el botó 'llançar instància'.

<figure><img src="../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

Tornem al panell d'instàncies EC2, i esperem que la instància finalitze el seu desplegament.

<figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

Mentre la instància finalitza la seua inicialització, podem observar la IP privada assignada (no té assignada cap IP pública).

<figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

Com que la màquina virtual no té assignada una IP pública, no podem connectar a la mateixa des d'internet ni des de la consola Web d'AWS Academy.

Per a poder connectar, hem de configurar al client SSH la propagació de clau privada, i connectar a la instància interna a través d'una instància pública, que farem servir com a host bastió.&#x20;

En primer lloc, al client que connectarà amb l'amfitrió bastió, hem d'inicialitzar l'agent ssh, i hem d'afegir la clau d'autenticació al keychain:

```bash
client:~$ eval `ssh-agent -s`
client:~$ ssh-add .ssh/labuser.pem
```

<figure><img src="../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

A continuació, connectem amb la IP pública de l'amfitrió bastió, desplegat a la subxarxa pública de la nostra VPC.

```bash
client:~$ ssh ubuntu@54.209.41.69 -i .ssh/labsuser.pem 
```

<figure><img src="../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

I per últim, connectem a l'amfitrió de la subxarxa privada, amb SSH, des de l'amfitrió bastió

```bash
ubuntu@ip-172-16-10-90:~$ ssh ubuntu@172.16.20.199
```

<figure><img src="../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

Una volta connectat a la instància interna, podem comprovar com  disposem de connectivitat amb internet, a través de la passarel·la NAT, intentant actualitzar el sistema operatiu, executant un apt update;

<figure><img src="../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>
