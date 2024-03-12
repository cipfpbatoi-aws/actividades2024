---
description: Configuració del grup de seguretat 'ssh-extern'.
---

# ⚒️ Estadístiques per a métriques en CloudWatch

Les estadístiques són agregacions de dades de mètriques corresponents a períodes especificats.&#x20;

<figure><img src="../../.gitbook/assets/blog-febrero-5-2021 (1).png" alt="" width="375"><figcaption></figcaption></figure>

CloudWatch ens proporciona estadístiques en funció dels punts de dades de mètriques proporcionades per les dades personalitzades o per altres serveis d'AWS per a CloudWatch. Les acumulacions es fan utilitzant l'espai de noms, el nom de mètrica, les dimensions i la unitat de mesura de punt de dades, dins del període de temps que especifiqueu.

| Estadística | Descripció                                                |
| ----------- | --------------------------------------------------------- |
| Minimum     | El valor més baix observat durant el període especificat. |
| Maximum     | El valor més alt observat durant el període especificat.  |

| Estadística | Descripció                                                                                                                                                                                                                                                                                                                  |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sum         | Tots els valors enviats per a mètrica coincident se sumen. Aquesta estadística pot ser útil per determinar el volum total duna mètrica.                                                                                                                                                                                     |
| Average     | El valor de Sum/SampleCount durant el període específic. En comparar aquesta estadística amb Minimum i Maximum, podem determinar l'àmbit complet d'una mètrica i com està a prop l'ús mitjà als valors Minimum i Maximum. Aquesta comparació ens ajuda a saber quan augmentar o reduir els recursos segons les necessitats. |
| SampleCount | El recompte (nombre) de punts de dades utilitzats per al càlcul estadístic.                                                                                                                                                                                                                                                 |
| pNN.NN      | El valor del percentil especificat. Podeu especificar qualsevol percentil amb fins a dos decimals (per exemple, p95.45).                                                                                                                                                                                                    |

