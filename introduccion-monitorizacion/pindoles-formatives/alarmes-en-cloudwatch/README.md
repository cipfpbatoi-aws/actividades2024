---
description: Qué son i per a que serveixen.
---

# ⚒️ Alarmes en CloudWatch

Les alarmes de CloudWatch amb AWS són mecanismes que es poden configurar per a supervisar els recursos i les mètriques en el núvol d'Amazon Web Services (AWS). Aquestes alarmes permeten als usuaris definir condicions específiques basades en mètriques de CloudWatch i rebre notificacions automàtiques quan es produeixen certes situacions o quan es superen certs llindars.

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="128"><figcaption></figcaption></figure>

Les alarmes de CloudWatch poden ser útils per a diverses situacions, com ara:

1. **Monitoreig de rendiment**: Poden alertar quan una mètrica, com la utilització de la CPU o la latència de les sol·licituds, supera o baixa de determinats límits, el que pot indicar problemes de rendiment.
2. **Escalabilitat automàtica**: Poden desencadenar accions automàtiques, com ara l'escalatge automàtic d'instàncies d'EC2, en resposta a canvis en les mètriques de rendiment.
3. **Gestió de costos**: Poden avisar quan s'estiguin utilitzant recursos de manera ineficient o s'estiguin acostant a llindars de costos predeterminats.
4. **Supervisió dels serveis**: Poden detectar falles o errors en els serveis, com ara l'estat de les instàncies d'EC2 o l'estat dels servidors de base de dades, i enviar alertes per a una acció immediata.

Per configurar una alarma de CloudWatch, primerament has de seleccionar la mètrica que vols supervisar, definir els llindars que desitges, i especificar com vols rebre les notificacions (per exemple, per correu electrònic, missatge de text, etc.). Una vegada configurada l'alarma, CloudWatch es manté vigilant i enviarà notificacions sempre que es compleixin les condicions definides. Això permet una gestió proactiva dels recursos d'AWS i ajuda a garantir que els serveis funcionen de manera òptima.
