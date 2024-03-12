# 📀 EBS

**Amazon Elastic Block Store (EBS)** és un servei d'emmagatzematge de blocs proporcionat per **Amazon Web Services (AWS)**. Ofereix volums d'emmagatzematge persistents a nivell de bloc per a l'ús amb instàncies d'**Amazon EC2 (Elastic Compute Cloud)**.

#### Característiques:

1. **Emmagatzematge de Blocs**: EBS proporciona volums d'emmagatzematge a nivell de bloc que es poden adjuntar a instàncies d'EC2.
2. **Persistència**: Les dades als volums d'EBS persisteixen independentment de la vida útil en execució d'una instància EC2. Això significa que pots aturar i reiniciar instàncies sense perdre dades als volums d'EBS.
3. **Instantànies (Snapshots)**: Els volums d'EBS es poden fer còpies de seguretat amb instantànies, que són còpies dels volums en un punt específic en el temps. Aquestes instantànies es poden utilitzar per crear nous volums o restaurar dades.
4. **Opcions de Rendiment**:
   * **Volums Respaldat per SSD**:
     * _Propòsit General (gp2)_: Adequat per a una àmplia gamma de càrregues de treball, oferint un equilibri entre preu i rendiment.
     * _IOPS Provisionades (io1)_: Dissenyat per a càrregues de treball intensives en E/S, et permet especificar IOPS (operacions d'entrada/sortida per segon) per a un rendiment previsible.

Per poder accedir a EBS hem d'accedir des del servei ![](<.gitbook/assets/image (1).png>), a continuació en el panell de l'esquerra podem veure les opcions de EBS:

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

En accedir al panell de _**Volúmenes**_ podem veure els discs de les nostres instàncies que tenim en ús.&#x20;

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>



<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**Amazon Elastic Block Store (EBS)** es un servicio de almacenamiento de bloques proporcionado por **Amazon Web Services (AWS)**. Ofrece volúmenes de almacenamiento persistentes a nivel de bloque para su uso con instancias de **Amazon EC2 (Elastic Compute Cloud)**. Aquí tienes un resumen de EBS:

#### Características:

1. **Almacenamiento de Bloques**: EBS proporciona volúmenes de almacenamiento a nivel de bloque que pueden adjuntarse a instancias de EC2.
2. **Persistencia**: Los datos en los volúmenes de EBS persisten independientemente de la vida útil en ejecución de una instancia EC2. Esto significa que puedes detener y reiniciar instancias sin perder datos en los volúmenes de EBS.
3. **Instantáneas (Snapshots)**: Los volúmenes de EBS pueden respaldarse tomando instantáneas, que son copias de los volúmenes en un punto específico en el tiempo. Estas instantáneas se pueden utilizar para crear nuevos volúmenes o restaurar datos.
4. **Opciones de Rendimiento**:
   * **Volúmenes Respaldados por SSD**:
     * _Propósito General (gp2)_: Adecuado para una amplia gama de cargas de trabajo, ofreciendo un equilibrio entre precio y rendimiento.
     * _IOPS Provisionadas (io1)_: Diseñado para cargas de trabajo intensivas en E/S, te permite especificar IOPS (operaciones de entrada/salida por segundo) para un rendimiento predecible.



