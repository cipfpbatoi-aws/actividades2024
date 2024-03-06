---
description: Alarmes en CloudWatch
---

# ⚒️ Alarmes que detenen, acaben, reinicien o recuperen una instància

Mitjançant les accions d'alarma d'Amazon CloudWatch, podem crear alarmes que aturen, acaben, reinicien o recuperen automàticament les instàncies.&#x20;

Aquestes accions aturar o acabar per ajudar-vos a estalviar diners quan ja no necessita que s'executi una instància o per contra utilitzar les accions reiniciar i recuperar per reiniciar automàticament aquestes instàncies o recuperar-les en nou maquinari si es produeix una fallada del sistema.&#x20;

El rol vinculat al servei AWSServiceRoleForCloudWatchEvents permet que AWS realitzi accions d'alarma en nom seu.&#x20;

Per exemple, si tenim instàncies dedicades a treballs de processament de nòmines per lots o tasques de càlcul científic que s'executen durant un període de temps i després completen el vostre treball.

En lloc de deixar aquestes instàncies inactives, podem aturar-les o acabar-les, cosa que us permetrà estalviar diners.&#x20;

La diferència entre utilitzar les accions d'alarma aturar i acabar és que una instància detinguda es pot reiniciar fàcilment si és necessari i una instància acabada no es pot reiniciar.&#x20;

En canvi, ha de llançar una nova instància. Podem afegir les accions d'aturar, acabar, reiniciar o recuperar qualsevol alarma establerta en una mètrica per instància Amazon EC2:

* Mètriques de monitorització proporcionades per Amazon CloudWatch.&#x20;
* Mètriques personalitzades.
