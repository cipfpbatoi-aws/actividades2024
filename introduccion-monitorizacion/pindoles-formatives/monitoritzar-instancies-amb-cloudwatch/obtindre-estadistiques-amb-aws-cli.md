---
description: AWS-CLI
---

# ⚒️ Obtindre estadístiques amb AWS-CLI

AWS CLI, que significa Amazon Web Services Command Line Interface, és una eina que proporciona una interfície de línia de comandes unificada per interactuar amb diversos serveis d'Amazon Web Services (AWS). Amb AWS CLI, els usuaris poden realitzar una varietat de tasques, com administrar instàncies d'EC2, emmagatzematge a S3, configurar serveis de xarxa com VPCs i grups de seguretat, gestionar bases de dades a RDS, entre d'altres coses.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>AWS-CLI</p></figcaption></figure>

AWS CLI permet als usuaris executar comandes des de la línia de comandes del seu terminal local, la qual cosa facilita l'automatització de tasques i la integració amb scripts i eines de desenvolupament. Això resulta especialment útil per a administradors de sistemes, desenvolupadors i qualsevol persona que treballe amb serveis en el núvol d'AWS i prefereix una interfície de línia de comandes sobre una interfície gràfica d'usuari.

Podem obtenir les mètriques de les instàncies a través d'AWS-CLI, per això hem de fer el següent:

Obtén el ID de la instància EC2 per a la qual desitges obtenir la mètrica. Pots obtenir-lo utilitzant la comanda `describe-instances` de AWS CLI.

```
aws ec2 describe-instances --query 'Reservations[*].Instances[*].[InstanceId, State.Name]' --output text
```

Amb l'ID de la instància EC2, pots obtenir la mètrica de CPUUtilization utilitzant la comanda `get-metric-statistics` de CloudWatch. Assegura't de substituir "INSTANCE\_ID" amb l'ID de la teua instància EC2.

```
aws cloudwatch get-metric-statistics \
    --namespace "AWS/EC2" \
    --metric-name "CPUUtilization" \
    --dimensions Name=InstanceId,Value=INSTANCE_ID \
    --start-time "$(date -u +%Y-%m-%dT%TZ --date '-1 hour')" \
    --end-time "$(date -u +%Y-%m-%dT%TZ)" \
    --period 300 \
    --statistics Maximum

```

Aquesta comanda et retornarà la mètrica CPUUtilization per a la instància EC2 especificada durant l'últim període d'una hora. Pots ajustar el temps i el període segons les teues necessitats.

És important tenir en compte que per a utilitzar aquestes comandes, necessitaràs tenir configurades les credencials d'AWS CLI i els permisos adequats per a accedir a les mètriques de CloudWatch i a la informació de les instàncies EC2.

Podem veure un cas real al següent exemple:

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 9.27.29.png" alt=""><figcaption><p>AWS-CLI / CPUUtilization</p></figcaption></figure>
