---
description: Creació d'un grup de seguretat
---

# ⚒️ Creació d'un grup de seguretat

Si volem crear un nou security group, accedim al panell de grups de seguretat, i polsem el botó 'crear grup de seguretat':

<figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption><p>Creació d'un nou security group</p></figcaption></figure>

Omplim les dades d'identificació del security group (nom i descripció), i seleccionem la VPC en la qual podrem fer servir el grup de seguretat:

<figure><img src="../.gitbook/assets/image (185).png" alt=""><figcaption><p>Configuració del nom, la descripció i la VPC</p></figcaption></figure>

Al panell de regles d'entrada podrem afegir totes les regles de tràfic entrant (definint els ports que obrirem a les màquines virtuals que apliquen el security group):

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption><p>Regles de tràfic entrant</p></figcaption></figure>

A cada regla, definirem el protocol (TCP | UDP | ICMP) i el port o ports que volem obrir, així com l'origen de les peticions a les quals es permetrà l'accés.

Per exemple, podem configurar l'obertura del port TCP/22 (SSH) des de qualsevol IP (incloses IP públiques), de la següent manera:

<figure><img src="../.gitbook/assets/image (135).png" alt=""><figcaption><p>Configuració de regla  d'entrada al security group</p></figcaption></figure>

O podem configurar l'obertura del port TCP/22 (SSH) des de qualsevol host que aplique una altra regla preexistent al security group.

La següent regla permet el tràfic TCP/22 (SSH) des de qualsevol màquina que aplique la regla ssh-bastion.

<figure><img src="../.gitbook/assets/image (136).png" alt=""><figcaption><p>Configuració de regla d'entrada al security group</p></figcaption></figure>

De la mateixa manera, podem configurar regles d'eixida, per controlar a quins serveis podran connectar-se les màquines virtuals que apliquen la regla.&#x20;

La següent regla permet tot el tràfic d'eixida, cap a qualsevol desti i port.

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption><p>Configuració de regla d'eixida al security group</p></figcaption></figure>

Una volta configurat el nostre security group, polsem sobre el botó 'Crear grup de seguretat', al final del formulari.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

Tornarem al llistat de regles de seguretat, on estarà disponible la nova regla.&#x20;

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption><p>Llistat de grups de seguretat</p></figcaption></figure>
