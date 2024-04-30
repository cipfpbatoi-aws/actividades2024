---
description: Creació d'un grup d'autoescalat a partir de la plantilla de llançament.
---

# ⚒️ Creació d'un grup d'autoescalat a partir de la plantilla de llançament.

Al panell EC2, busquem l'opció 'grups d'auto escaling'

<figure><img src="../../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

Al formulari, introduïm el nom del grup d'autoescalat, i seleccionem la plantilla amb la qual es crearan les instàncies EC2, i prenem el botó 'Següent'.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Seleccionem les zones de seguretat en les que es desplegaran les instàncies (a l'exemple, us-east-1a i us-east-1b, donat que és la zona que tenim permesa al nostre laboratori d'AWS Academy, però podem desplegar les nostres instàncies a múltiples zones de disponibilitat) i prenem el botó 'següent'.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Donat que el grup desplegarà múltiples instàncies, amb diferents IP públiques, podem associar el nostre grup d'autoescalat a un balancejador de càrrega, que disposara de la seua pròpia IP pública i s'encarregue de redirigir les peticions a les instàncies desplegades.

De moment, no seleccionarem balancejador de càrrega, donat que volem crear-lo manualment.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Al següent pas, configurarem les polítiques d'autoescalat. A l'exemple, indicarem que volem únicament 1 rèplica en execució, però que si la càrrega de processador supera el 50% de la seua capacitat, arranque fins a tres rèpliques.&#x20;

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

A continuació, podem afegir notificacions, que ens avisen amb les accions d'escalat. De moment no afegirem cap notificació.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

També podem afegir etiquetes al servei d'autoescalat, que ens ajuden a filtrar en les tasques de monitoratge i facturació. A l'exemple no configurarem cap etiqueta.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

Per últim, podem revisar el grup d'autoescalat, i polsar sobre el botó 'crar grup d'autoescalat'.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Al panell dels grups d'autoescalat podrem observar com es crea el grup, i el nombre d'instàncies en execució.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

També podem accedir al panell EC2, i observar les instàncies creades.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

