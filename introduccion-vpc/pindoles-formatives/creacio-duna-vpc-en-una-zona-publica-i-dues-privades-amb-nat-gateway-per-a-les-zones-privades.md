# ⚒️ Creació d'una VPC en una zona pública i dues privades, amb NAT Gateway per a les zones privades

L'existència de zones públiques i privades es basa principalment en la necessitat de seguretat i en els requisits d'accessibilitat dels recursos des de l'exterior.&#x20;

1. **Zones Públiques**:
   * Les zones públiques són segments de xarxa a la teva infraestructura de núvol que estan accessibles des de l'internet públic.
   * Característiques:
     * **Accessibles des de l'exterior**: Les instàncies, serveis i recursos allotjats en aquestes zones poden ser accedits mitjançant adreces IP públiques.
     * **Accessibilitat ampliada**: Aquestes zones s'utilitzen per allotjar recursos que necessiten ser accessibles des de qualsevol lloc a través d'internet, com ara servidors web, serveis d'API públics, etc.
     * **Exposició a la internet**: Donat que els recursos aquí són accessibles públicament, existeix un major risc de seguretat, per la qual cosa es requereixen mesures de seguretat addicionals, com ara grups de seguretat, control d'accés basat en l'autenticació, entre d'altres.
     * **IP Públiques**: Les instàncies i els recursos en aquesta zona tenen assignades adreces IP públiques per a la seva identificació a internet.
2. **Zones Privades**:
   * Les zones privades són segments de xarxa que estan aïllats de l'internet públic i no són accessibles directament des de l'exterior.
   * Característiques:
     * **Aïllament:** Les instàncies, serveis i recursos allotjats en aquestes zones no són accessibles des de l'internet públic, la qual cosa proporciona una capa addicional de seguretat.
     * **Seguretat:** Les zones privades s'utilitzen per allotjar recursos sensibles o crítics que no han de ser exposats a internet, com ara bases de dades, sistemes interns, aplicacions internes, etc.
     * **Accés restringit:** L'accés als recursos en aquestes zones es controla normalment mitjançant mecanismes de seguretat com els grups de seguretat, les llistes de control d'accés (ACLs), o les polítiques de control d'accés IAM (Identity and Access Management).
     * **IP Privades:** Les instàncies en aquesta zona tenen assignades adreces IP privades que no són accessibles des de l'exterior i només són accessibles dins de la xarxa privada de la VPC.

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
