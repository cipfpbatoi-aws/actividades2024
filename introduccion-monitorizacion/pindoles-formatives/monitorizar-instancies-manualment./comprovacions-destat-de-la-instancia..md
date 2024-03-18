---
description: Monitorització d'instàncies de manera manual.
---

# ⚒️ Comprovacions d'estat de la instància.

Monitorització de la configuració de programari i de xarxa de la instància individual.

Amazon EC2 verifica l'estat de la instància mitjançant l'enviament d'una sol·licitud del protocol de resolució d'adreces (ARP) a la interfície de xarxa (NIC).

* Error de comprovacions d'estat del sistema.
* Configuració de xarxa o d'inici incorrecte.
* Memòria esgotada.
* Sistema de fitxers danyat.
* Kernel incompatible.

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption><p>Comprovació d'estat de l'instancia.</p></figcaption></figure>

Per informar de l'estat d'una instància:&#x20;

1. Obrim la consola dAmazon EC2.
2. Al panell de navegació, premem Instàncies.
3. Seleccioneu la instància, escolliu la pestanya Comprovacions de estat, premem Accions i al segon menú Accions situat a la part inferior de la pàgina i feu clic a Notificar estat d'instància).
4. Ompliu el formulari Notificar estat d'instància i feu clic a Enviar.

Des de la línia d'ordre report-instance-status (AWS CLI) per enviar comentaris sobre l'estat d'una instància deteriorada:

```
aws ec2 report-instance-status \ --instances i-0d194431a2174655e \ --status impaired \ --reason-codes code 
```

Els codis de motiu per al comandament `aws ec2 report-instance-status` depenen del context de les teves instàncies d'EC2 i de per què estàs executant aquest comandament. Aquí tens alguns exemples de codis de motiu comuns i les seves descripcions:

* `instance-stuck-in-state` : La instància està atascada en un estat concret i no es mou al següent estat.
* `unresponsive` : La instància no respon a les sol·licituds.
* `not-accepting-credentials` : La instància no està acceptant credencials.
* `internal-error` : S'ha produït un error intern a la instància.
* `pending-termination` : La instància està en estat de terminació pendent.
* `scheduled-for-retirement` : La instància està programada per a la jubilació.
* `scheduled-for-maintenance` : La instància està programada per a manteniment.

Quan executes el comandament `aws ec2 report-instance-status`, necessites proporcionar un valor específic per a `--reason-codes`. Per exemple, si vols informar que una instància està "atascada en un estat", utilitzaries:

aws ec2 report-instance-status --instances i-0d194431a2174655e --status impaired --reason-codes instance-stuck-in-state
