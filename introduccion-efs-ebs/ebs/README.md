---
description: Elastic Block Store
---

# 📀 EBS

<figure><img src="../.gitbook/assets/image (8) (1).png" alt="" width="150"><figcaption></figcaption></figure>

**Amazon Elastic Block Store (EBS)** és un servei d'emmagatzematge de blocs proporcionat per **Amazon Web Services (AWS)**. Ofereix volums d'emmagatzematge persistents a nivell de bloc per a l'ús amb instàncies d'**Amazon EC2 (Elastic Compute Cloud)**.

Algunes característiques de **EBS**: &#x20;

1. **Emmagatzematge de Blocs**: EBS proporciona volums d'emmagatzematge a nivell de bloc que es poden adjuntar a instàncies d'EC2.
2. **Persistència**: Les dades als volums d'EBS persisteixen independentment de la vida útil en execució d'una instància EC2. Això significa que pots aturar i reiniciar instàncies sense perdre dades als volums d'EBS.
3. **Instantànies (Snapshots)**: Els volums d'EBS es poden fer còpies de seguretat amb instantànies, que són còpies dels volums en un punt específic en el temps. Aquestes instantànies es poden utilitzar per crear nous volums o restaurar dades.
4. **Opcions de Rendiment**:
   * **Volums Respaldat per SSD**:
     * _Propòsit General (gp2)_: Adequat per a una àmplia gamma de càrregues de treball, oferint un equilibri entre preu i rendiment.
     * _IOPS Provisionades (io1)_: Dissenyat per a càrregues de treball intensives en E/S, et permet especificar IOPS (operacions d'entrada/sortida per segon) per a un rendiment previsible.

Per poder accedir a **EBS** hem d'accedir des del servei ![](<../.gitbook/assets/image (1) (1) (1).png>), a continuació en el panell de l'esquerra podem veure les opcions i en el tercer apartat vegem **EBS**:

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

En accedir al panell de _**Volúmenes**_ podem veure els discs de les nostres instàncies que tenim en ús.&#x20;

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>



