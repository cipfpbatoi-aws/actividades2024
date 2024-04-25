# ⚒️ Connexió a internet a través d'una passarel·la NAT

Una passarel·la NAT (Network Address Translation) és un component clau en una infraestructura de xarxa que permet que les instàncies en zones privades d'una VPC accedeixin a internet de forma segura, tot traduint les seves adreces IP privades a adreces IP públiques. Aquí tens una explicació de com funciona i com es connecta a internet a través d'aquesta passarel·la:

1. **Funcionament de la Passarel·la NAT**:
   * Les instàncies en una zona privada tenen adreces IP privades que no són accessibles des de l'exterior.
   * Quan una instància en una zona privada vol accedir a internet per actualitzacions de software, per descarregar fitxers, o per accedir a serveis externs, envia una sol·licitud a la passarel·la NAT.
   * La passarel·la NAT actua com un intermediari entre les instàncies privades i internet. Quan rep una sol·licitud d'una instància privada, tradueix la seva adreça IP privada a una adreça IP pública assignada a la passarel·la NAT.
   * La passarel·la NAT envia la sol·licitud a internet utilitzant la seva adreça IP pública.
   * Quan rep una resposta de l'exterior, la passarel·la NAT tradueix l'adreça IP de destinació (adreça IP pública) de la resposta a l'adreça IP privada de la instància corresponent i reenvia la resposta a la instància privada.
2. **Connexió a Internet a través de la Passarel·la NAT**:
   * Per connectar-se a internet a través de la passarel·la NAT, les instàncies en zones privades utilitzen la seva adreça IP privada com a adreça de destinació per a les sol·licituds de sortida.
   * Quan una instància en una zona privada envia una sol·licitud de sortida, aquesta sol·licitud es redirigeix a través de la passarel·la NAT.
   * La passarel·la NAT tradueix l'adreça IP de la instància privada a una adreça IP pública assignada a la passarel·la NAT i reenvia la sol·licitud a internet.
   * Quan la resposta de la sol·licitud arriba, la passarel·la NAT tradueix l'adreça IP de destinació (adreça IP pública) de la resposta a l'adreça IP privada de la instància corresponent i reenvia la resposta a la instància privada.
   * Això permet que les instàncies en zones privades accedeixin a internet de forma segura, ja que les seves adreces IP privades no són visibles a l'exterior, i només es comuniquen amb internet a través de la adreça IP pública de la passarel·la NAT.
