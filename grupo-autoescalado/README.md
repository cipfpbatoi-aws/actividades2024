---
description: Grups d'autoescalat
---

# ⚒️ Grups d'autoescalat

Els grups d'autoescalat ens faciliten la configuració de l'escalat horitzontal d'instàncies, de manera dinàmica, depenent de les nostres necessitats, o la càrrega del sistema.

Els grups d'autoescalat despleguen noves instàncies, o eliminen instàncies EC2, amb unes característiques prèviament definides, depenent d'alguns paràmetres de configuració, denominats 'AutoScaling Policies'.

<figure><img src=".gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

Aquestes regles d'autoescalat poden estar basades en diversos factors, com ara:

* L'autoescalat dinàmic, basat en la demanda de recursos (CPU, memòria...)
* L'autoescalat predictiu, basat en regles basat en regles de calendari, programades automàticament amb regles ML (calcula la demanda futura - horària i setmanal - basant-se en les dades històriques).
* L'autoescalat programat, basat en regles de calendari, que podem programar manualment.
