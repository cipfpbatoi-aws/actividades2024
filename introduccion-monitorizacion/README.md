# ⚒️ Monitoritzant instàncies EC2 de AWS

La monitorització és un aspecte important del manteniment de la fiabilitat, la disponibilitat i el rendiment de les instàncies d'Amazon Elastic Compute Cloud (Amazon EC2) i les solucions d'AWS.

<figure><img src=".gitbook/assets/Captura de pantalla 2024-01-25 a las 19.24.52.png" alt=""><figcaption><p>EC2 Monitoring</p></figcaption></figure>

És convenient recopilar dades de monitorització de totes les parts de les solucions d'AWS perquè sigui més senzill depurar un error que es produeix a diferents parts del codi, en cas que passi. Això no obstant, abans de començar a monitoritzar Amazon EC2, hauria de crear un pla de monitoratge que inclogués el següent:

* Quins són els objectius del monitoratge? &#x20;
* Quins recursos monitoritzareu?
* Amb quina freqüència monitoritzarà aquests recursos?
* Quines eines de monitorització va a utilitzar?
* Qui s'encarregarà de fer les tasques de monitorització?
* Qui hauria de rebre una notificació quan sorgeixin problemes?

Després de definir els objectius i de crear el pla de monitorització, el pas següent consisteix a establir un punt de referència per a l'exercici normal d'Amazon EC2 a l'entorn.

Convé mesurar lús de la instància dAmazon EC2 en diferents ocasions i amb diferents condicions de càrrega. A mesura que monitoritzeu Amazon EC2, cal guardar un historial de les dades de monitorització que recopila. Realitzar comparatives dús actual dAmazon EC2 amb les dades històriques per identificar patrons de càrrega normal i anomalies en lús dels recursos, així com desenvolupar mètodes per solucionar-los.

Per exemple, podeu monitoritzar l'ús de la CPU, la I/O de disc i l'ús de la xarxa de les instàncies EC2. Si la càrrega no arriba als valors del punt de referència establert, és possible que haguem de tornar a configurar o optimitzar la instància per reduir la utilització de la CPU, millorar l'E/S de disc o reduir el trànsit de xarxa.

Per establir un punt de referència ha de, com a mínim, monitoritzar els elements següents:

|                        Elements                       |          Mètrica EC2         |                                                                Agent / CloudWatch                                                               |
| :---------------------------------------------------: | :--------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------: |
|                          CPU                          |        CPUUtilization        |                                                                                                                                                 |
|                         Xarxa                         |    NetworkIn / NetworkOut    |                                                                                                                                                 |
|                          Disc                         |  DiskReadOps / DiskWriteOps  |                                                                                                                                                 |
|                        R/W Disc                       | DiskReadByte / DiskWriteByte |                                                                                                                                                 |
| Ús de memoria, intercavi amb disc, espai del disc ... |                              | \[Instàncies de Linux i Windows Server] Recopilar mètriques i registres d'instàncies d'Amazon EC2 i servidors locals amb l'agent de CloudWatch. |

AWS proporciona diverses eines que podeu utilitzar per monitoritzar Amazon EC2. Podeu configurar algunes d'aquestes eines per monitoritzar-les, però altres eines requereixen intervenció manual.
