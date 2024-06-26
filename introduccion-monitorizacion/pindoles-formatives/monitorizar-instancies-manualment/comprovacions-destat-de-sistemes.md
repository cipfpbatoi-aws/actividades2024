---
description: Monitorització d'instàncies de manera manual.
---

# ⚒️ Comprovacions d'estat de sistemes

Les comprovacions d'estat del sistema monitoritzen els sistemes d'AWS on s'executa la instància. Aquestes comprovacions detecten problemes subjacents amb la instància que requereixen la intervenció d'AWS per solucionar-los.

* Pèrdua de connectivitat de xarxa.
* Pèrdua de potència del sistema.
* Problemes de programari al host físic.
* Problemes de maquinari al host físic que afecten la accessibilitat a la xarxa.

Aquesta comprovació verifica que la instància és accessible. Amazon EC2 verifica si els paquets de xarxa poden arribar a la instància.

Si aquesta comprovació no es realitza correctament, pot haver-hi un problema amb la infraestructura que allotja la instància (per exemple, als sistemes de programari, xarxes o alimentació d'AWS). Podeu reiniciar o reemplaçar la instància, esperar que els sistemes d'Amazon EC2 resolguin el problema o cercar suport tècnic.

Aquesta comprovació no verifica si el sistema operatiu i les aplicacions estan acceptant trànsit.

Per veure les comprovacions d'estat:

1. Obriu la consola d'Amazon EC2.&#x20;
2. Al panell de navegació, seleccionem Instàncies.&#x20;
3. A la pàgina d'Instàncies a la columna de Comprovacions d'estat, indica l'estat operatiu de cada instància.&#x20;
4. Per veure l'estat d'una instància específica, seleccionem la instància i, a continuació, Comprovacions d'estat.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p>Comprovacions d'estat correcta.</p></figcaption></figure>

Si la instància té una comprovació d'estat fallida, “normalment” haurem de solucionar el problema nosaltres mateixos (per exemple: en reiniciar la instància o fer canvis en la configuració de la instància).

Per veure l'estat de totes les instàncies a través d'AWS-CLI, utilitzarem l'ordre següent:

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

