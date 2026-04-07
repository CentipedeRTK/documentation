# Glossaire
| Terme | Définition |
|------|------------|
| **Base** | Aussi appelée base RTK, station de référence, station : ensemble physique récepteur GNSS + antenne produisant des corrections (observations) que les rovers peuvent utiliser pour obtenir un positionnement de haute précision |
| **Rover** | Ensemble récepteur GNSS qui utilise les corrections d'une base pour calculer sa position avec une grande précision |
| **Caster** | Serveur qui reçoit les corrections de la base et les met à disposition des rovers via le protocole NTRIP |
| **Mountpoint** | Aussi appelé point de montage en français : identifiant unique d'une correction |
| **Correction** | Aussi appelée observation : donnée produite par la base qui permet aux rovers de calculer leur position avec une grande précision |
| **RTK** | Real-Time Kinematic : technique qui utilise les corrections d'une base pour calculer la position d'un rover avec une grande précision en temps réel |
| **Post-processing** | Technique qui utilise les corrections d'une base pour calculer la position d'un rover avec une grande précision après la collecte des données, et non en temps réel. |
| **RINEX** | Receiver Independent Exchange Format : format standard de stockage des observations GNSS, pouvant être utilisé pour le post-traitement, par exemple pour déterminer la position réelle de la base |
| **NTRIP** | Networked Transport of RTCM via Internet Protocol : protocole utilisé pour transmettre les corrections du caster vers les rovers |
| **RTCM3** | Radio Technical Commission for Maritime Services version 3 : format standard des corrections, qui peuvent être utilisées en temps réel par les rovers pour calculer leur position avec une grande précision |
| **MSM7** | Type de message RTCM3 qui contient un jeu complet d'observations avec la plus grande précision, incluant pseudodistance, phase de porteuse, Doppler et intensité du signal pour tous les satellites suivis |
| **MSM4** | Type de message RTCM3 qui contient un jeu réduit d'observations avec une précision plus faible, incluant pseudodistance et phase de porteuse avec une résolution réduite, ainsi que l'intensité du signal pour tous les satellites suivis |
| **GGA** | Type de phrase NMEA contenant la position du rover, utilisée par le caster pour déterminer quelle base est la plus proche du rover pour les mountpoints `NEAR` ou `NEAR4` |
