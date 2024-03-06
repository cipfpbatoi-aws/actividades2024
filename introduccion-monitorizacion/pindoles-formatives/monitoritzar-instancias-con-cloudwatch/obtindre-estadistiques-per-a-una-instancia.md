---
description: Exemple de dades de la CPU
---

# ⚒️ Obtindre estadístiques per a una instancia

El següent exemple mostra com utilitzar l'AWS Management Console o l'AWS CLI per determinar la utilització de CPU màxima d'una instància EC2 específica.

1. Obrim la consola de CloudWatch.
2. Al panell de navegació, Mètriques.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-08 a las 13.41.42.png" alt=""><figcaption></figcaption></figure>

3. Trieu l'opció Mètriques per instància.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-08 a las 13.47.11.png" alt=""><figcaption></figcaption></figure>

4. Trieu l'espai de noms de mètrica d'EC2.&#x20;

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-08 a las 13.44.00.png" alt=""><figcaption></figcaption></figure>

5. Al camp de cerca, polsarem Intro. Triem la fila de la instància concreta, que mostra un gràfic per a la mètrica CPUUtilization de la instància. Per assignar un nom al gràfic, farem servir la icona del llapis. Per canviar l'interval de temps, seleccionem un dels valors predefinits o el podem personalitzar.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-08 a las 14.17.27.png" alt=""><figcaption></figcaption></figure>

6. Per canviar l'estadística o el període de temps de la mètrica, des de la pestanya Mètriques diagramades, triarem la capçalera de columna o un valor individual i, a continuació, escolliu un valor diferent.
