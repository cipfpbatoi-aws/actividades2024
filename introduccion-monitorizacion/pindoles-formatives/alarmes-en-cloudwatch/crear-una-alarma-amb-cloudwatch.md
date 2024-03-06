# ⚒️ Crear una alarma amb CloudWatch

Podem crear una alarma de CloudWatch que vaig monitoritzar mètriques de CloudWatch per a una de les seves instàncies. CloudWatch us enviarà una notificació automàticament quan la mètrica arribi a un límit que heu especificat.&#x20;

Per crear una alarma mitjançant la consola d'Amazon EC2:

1.- Obrirem la consola d'Amazon EC2.

2.- Al panell de navegació, seleccionem Instàncies.

3.- Seleccionarem la instància i triarem Accions > Monitorització i solució de problemes > Administrar alarmes de CloudWatch.

4.- A Administrar alarmes de CloudWatch > Afegeix o edita alarma > Crear una alarma.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 11.40.43.png" alt=""><figcaption></figcaption></figure>

5.- A l'opció Notificació d'alarma, triarem si voleu activar o desactivar per configurar les notificacions de l'Amazon Simple Notification Service (Amazon SNS). Introduirem un tema d'Amazon SNS existent o escriurem un nom per crear un tema nou.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 11.41.15.png" alt=""><figcaption></figcaption></figure>

6.- A Acció d'alarma, seleccionarem si volem activar o desactivar l'opció per especificar l'acció que cal fer quan s'activi l'alarma. Seleccionarem una acció al menú desplegable.

7.- Llindars d'alarma, seleccioneu la mètrica i els criteris per a la alarma.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 11.41.51.png" alt=""><figcaption></figcaption></figure>

8.- Opcionalment a “Mostrejar dades de mètrica”, triarem la opció Afegeix al panell.

9.- Finalment polsarem a crear.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 11.43.13.png" alt=""><figcaption><p>Comprovacions d'estat</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-02-15 a las 11.46.57.png" alt=""><figcaption><p>Alarma activada</p></figcaption></figure>
