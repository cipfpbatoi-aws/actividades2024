---
description: Monitorització d'instàncies de manera manual.
---

# ⚒️ Comprovacions d'estat de sistemes.

Les comprovacions d'estat del sistema monitoritzen els sistemes d'AWS on s'executa la instància. Aquestes comprovacions detecten problemes subjacents amb la instància que requereixen la intervenció d'AWS per solucionar-los.

* Pèrdua de connectivitat de xarxa.
* Pèrdua de potència del sistema.
* Problemes de programari al host físic.
* Problemes de maquinari al host físic que afecten la accessibilitat a la xarxa.

Per veure les comprovacions d'estat:

1. Obriu la consola d'Amazon EC2.&#x20;
2. Al panell de navegació, seleccionem Instàncies.&#x20;
3. A la pàgina d'Instàncies a la columna de Comprovacions d'estat, indica l'estat operatiu de cada instància.&#x20;
4. Per veure l'estat d'una instància específica, seleccionem la instància i, a continuació, Comprovacions d'estat.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Comprovacions d'estat</p></figcaption></figure>

Si la instància té una comprovació d'estat fallida, “normalment” haurem de solucionar el problema nosaltres mateixos (per exemple: en reiniciar la instància o fer canvis en la configuració de la instància).

Per veure l'estat de totes les instàncies, utilitzeu l'ordre següent:

```
aws ec2 describe-instance-status
```

```
eee_W_2589232@runweb117359:~$  aws ec2 describe-instance-status
{
    "InstanceStatuses": [
        {
            "AvailabilityZone": "us-east-1c",
            "InstanceId": "i-0d194431a2174655e",
            "InstanceState": {
                "Code": 16,
                "Name": "running"
            },
            "InstanceStatus": {
                "Details": [
                    {
                        "Name": "reachability",
                        "Status": "passed"
                    }
                ],
                "Status": "ok"
            },
            "SystemStatus": {
                "Details": [
                    {
                        "Name": "reachability",
                        "Status": "passed"
                    }
                ],
                "Status": "ok"
            }
        }
    ]
}
```
