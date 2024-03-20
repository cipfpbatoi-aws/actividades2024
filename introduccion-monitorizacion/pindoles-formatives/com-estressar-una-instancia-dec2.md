---
description: Ferramenta "stress" de Linux
---

# ⚒️ Com estressar una instància d'EC2

Aquí tens un resum dels passos per instal·lar la ferramenta `stress` en una instància Linux d'Amazon, com ara Amazon EC2:

#### 1. Connectar-se a la instància Linux

Utilitza SSH per connectar-te a la teva instància Linux des del terminal o un programa com PuTTY per Windows.

```
ssh -i clau-privada.pem usuari@adreça-ip-de-la-instància
```

#### 2. Instal·lar `stress`

Per a sistemes basats en Debian/Ubuntu (com Amazon Linux 2):

```
sudo apt update
sudo apt install stress
```

Per a sistemes basats en Red Hat (com Amazon Linux 1):

```
sudo yum update
sudo yum install stress
```

#### 3. Provar `stress`

Utilitza `stress` per provar la teva CPU o memòria.&#x20;

Per exemple, per estressar la CPU amb 4 processos durant 60 segons:

```
stress --cpu 4 --timeout 60s
```

Per estressar la memòria amb 1 GB durant 60 segons:

```
stress --vm 1 --vm-bytes 1G --timeout 60s
```

| **Options** | **Short forms** | **Description**                                     |
| ----------- | --------------- | --------------------------------------------------- |
| –hdd        | -d              | stress the storage.                                 |
| –CPU        | -c              | stress the CPU.                                     |
| –vm         | -v              | stress the memory.                                  |
| –io         | -i              | stress io.                                          |
| –timeout    | -t              | decide the time period for the stress (in seconds). |
