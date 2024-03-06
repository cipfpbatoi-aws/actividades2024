# ⚒️ Eliminació de la VPC per defecte.

Com a norma general, és una bona pràctica eliminar la VPC creada automàticament en crear un compte d'AWS, i gestionar manualment la creació de VPCs al nostre compte.

A la consola d'AWS, hem de cercar VPC, i polsar sobre l'enllaç corresponent, per accedir al panell de configuració de VPCs.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Al panell de VPC podrem configurar xarxes virtuals, subxarxes, taules d'encaminament, portes d'enllaç a internet, adreces IP públiques elàstiques (fixes), VPN...
{% endhint %}

Al panell VPC, polsarem sobre l'enllaç 'Les seues VPC'.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

L'enllaç carregarà una pàgina amb el llistat de VPCs existents al nostre entorn. Podem seleccionar una VPC i observar la seua configuració.&#x20;

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Per a eliminar una VPC, la seleccionem al llistat, obrim el menú d'accions, i polsem sobre l'opció 'Esborrar VPC'.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

En polsar sobre el botó 'Esborrar VPC' ens mostrarà la informació de tots els elements que s'esborraran (xarxa, subxarxa, Gateway) i ens demanarà confirmació de l'esborrat.&#x20;

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

