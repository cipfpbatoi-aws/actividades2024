# ⚒️ Creació d'una VPC en una zona pública i dues privades, amb NAT Gateway per a les zones privades

TO-DO: explicació existència zones públiques i privades, i característiques de cada tipus.

{% hint style="danger" %}
Encara que el tutorial funcione, al fer servir un servei administrat per al NAT gateway, el consum de crèdit es alt.

Sería preferible buscar una alternativa IAAS, per exemple, amb un servidor de comunicacions Ubuntu amb UFW.
{% endhint %}

Per a les nostres proves, crearem una VPC amb una zona pública, i dues zones privades.

Accedim al panell de VPCs.

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

Al panell VPC, polsarem sobre l'enllaç 'Les seues VPC'.

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

I polsem el botó 'Crear VPC'

<figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

La consola d'AWS ens mostrarà el formulari per a la creació de xarxes privades, donant-nos dues opcions:

* Crear únicament la VPC.
* Crear la VPC, i més (subxarxes, taules de ruta i interconnexions entre les subxarxes).

Al nostre exemple, farem servir l'opció 'Crear VPC i més', i omplirem la resta del formulari amb les dades solicitades:

<figure><img src="../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

Polsem el botó 'Crea xarxa' i ens crearà els següents elements:

* xarxa smx-vpc (172.16.0.0/16)
  * subxarxa smx-subnet-public1 (172.16.10.0/24)
    * Taula de rutes smx-rtb-public
    * Connexió amb smx-internet-gateway
  * subxarxa smx-subnet-private1 (172.16.20.0/24)
    * Taula de rutes smx-rtb-private1
    * Connexió amb smx-vpce-s3
    * Connexió amb smx-nat-public
  * subxarxa smx-subnet-private2 (172.16.21.0/24)
    * Taula de rutes smx-rtb-private1
    * Connexió amb smx-vpce-s3
    * Connexió amb smx-nat-public

En finalitzar el procés de creació, podrem observar tots els elements instanciats.

<figure><img src="../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

Observa els elements creats, accedint a les diferents opcions del panell VPC

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>
