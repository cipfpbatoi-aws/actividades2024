---
description: Desplegament d'una màquina virtual Ubuntu Server 22.04 a AWS Academy
---

# ⚒️ Desplegament d'un host bastió SSH a la subxarxa  pública

En primer lloc, [accedim a la consola d'AWS](broken-reference).

<figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption><p>Consola d'AWS</p></figcaption></figure>

En el buscador, introduïm les sigles 'EC2', i seleccionem l'opció 'EC2 - servidors virtuals en el núvol'.

![](<.gitbook/assets/image (13).png>)&#x20;

A la pàgina d'instàncies podrem polsar sobre el link 'instancies en execució' i visualitzar el llistat d'instàncies desplegades a la nostra infraestructura al núvol d'AWS. &#x20;

<figure><img src=".gitbook/assets/image (113).png" alt=""><figcaption><p>Opció 'instàncies en execució' del panel EC2</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (114).png" alt=""><figcaption><p>Llistat d'instàncies desplegades</p></figcaption></figure>

Per a desplegar una nova instància, haurem de polsar sobre un dels botons 'Llançar instància'.

<figure><img src=".gitbook/assets/image (115).png" alt=""><figcaption><p>Botó llançar instància.</p></figcaption></figure>

Omplim el formulari, seguint les instruccions de l'assistent de desplegament de nova instància.&#x20;

* Introduïm el nom de la nova instància. Al nostre exemple l'anomenarem bastion-host

<figure><img src=".gitbook/assets/image (116).png" alt=""><figcaption><p>Configuració del nom de la instància</p></figcaption></figure>

* Seleccionem la imatge de sistema operatiu i aplicacions (AMI - Amazon Machine Image) que volem carregar a la nova instància. Al nostre cas, seleccionem un Ubuntu Server 22.04 de 64 bits.

<figure><img src=".gitbook/assets/image (117).png" alt=""><figcaption><p>Selecció d'AMI</p></figcaption></figure>

* Seleccionem el tipus d'instància que volem desplegar, que determinarà la configuració del processador i la memòria de la instància. Al nostre cas, farem servir instàncies t2.micro, aptes per a la capa gratuïta de serveis, per tal d'abaratir els costos del nostre laboratori.

<figure><img src=".gitbook/assets/image (118).png" alt=""><figcaption><p>Selecció de tipus d'instància.</p></figcaption></figure>

* Seleccionem el parell de claus que farem servir per a connectar a la instància de manera remota, amb un client SSH. Com que és la nostra primera màquina, podem crear un nou parell de claus.

<figure><img src=".gitbook/assets/image (119).png" alt=""><figcaption><p>Creació d'un nou parell de claus</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (120).png" alt=""><figcaption><p>Configuració del nou parell de claus</p></figcaption></figure>

<figure><img src=".gitbook/assets/image (121).png" alt=""><figcaption><p>Selecció del parell de claus que farem servir al nou host</p></figcaption></figure>

* A la configuració de xarxa podem seleccionar els grups de seguretat (regles de tallafoc) que volem aplicar a la nova instància. Al nostre cas, crearem un nou grup de seguretat per a permetre l'accés per SSH al nostre nou host, o podem fer servir un grup de seguretat existent, si el tenim prèviament configurat.&#x20;

<figure><img src=".gitbook/assets/image (122).png" alt=""><figcaption><p>Configuració d'accés per SSH des d'internet</p></figcaption></figure>

* Farem scroll fins a trobar l'opció 'Llançar instància', i el polsarem, per a aprovisionar la mateixa.&#x20;

<figure><img src=".gitbook/assets/image (123).png" alt=""><figcaption><p>Llançar la instància</p></figcaption></figure>

Rebrem un missatge, indicant que la nova instància ha iniciat correctament, i un enllaç per poder veure totes les instàncies del nostre entorn virtual. Polsem sobre el botó 'Veure totes les instàncies'.

<figure><img src=".gitbook/assets/image (124).png" alt=""><figcaption><p>Informació sobre la creació de la nova instància</p></figcaption></figure>

Podem observar totes les instàncies en execució, i podem seleccionar una instància, per tal de comprovar els seus paràmetres:

<figure><img src=".gitbook/assets/image (125).png" alt=""><figcaption><p>Informació de la instància en execució</p></figcaption></figure>

Ara podem connectar per SSH a l'amfitrió bastió, fent servir la clau privada descarregada, i operar el mateix.
