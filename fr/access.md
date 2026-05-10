---
title: Accéder aux corrections
---

# Accéder aux corrections

Les corrections sont accessibles via le protocole NTRIP, largement pris en charge par les logiciels et matériels RTK. Pour vous connecter au réseau Centipede-RTK, vous aurez besoin d'un client NTRIP et des informations de connexion suivantes :
- **Hostname**: `crtk.net`
- **Port (non sécurisé)**: `2101`
- **Port (sécurisé NTRIP 2.0 avec TLS)**: `443`
- **Mountpoint (Point de montage)**
  - `NEAR`: Sélection automatique de la base opérationnelle la plus proche de vous. Le flux de "correction" est complet (MSM7).
  - `NEAR4`: Même principe que `NEAR` mais avec un débit plus faible (MSM4)
  - Le mountpoint peut aussi être sélectionné manuellement par son nom, que vous trouverez sur la [carte de couverture](https://map.centipede-rtk.org/index.php/view/map?repository=cent&project=centipede)
- Aucune identification n'est nécessaire, mais cela fonctionne aussi avec :
  - **Username**: `centipede`
  - **Password**: `centipede`
- **Format**: RTCM3
- **Version NTRIP**: les versions 1 et 2 sont prises en charge

:::warning
**Les points de montage `NEAR` ou `NEAR4` doivent recevoir des trames NMEA GGA pour commencer à envoyer les corrections**
:::

:::warning
**Certains récepteurs ne prennent pas en charge les flux de correction à haut débit binaire (MSM7), comme ceux fournis par le point de montage`NEAR`. Dans ce cas, il est recommandé d'utiliser le point de montage `NEAR4`, qui propose des corrections plus légères.**
:::

:::warning
**Le NTRIP sécurisé (avec TLS) n'est pris en charge que par certains clients. Si votre client ne le prend pas en charge, vous pouvez utiliser le port non sécurisé, mais soyez conscient que votre connexion ne sera pas chiffrée.** Des attaquants ayant accès au réseau pourraient potentiellement intercepter et modifier les données de correction, ce qui pourrait entraîner un positionnement incorrect et également accéder à la position du rover si `NEAR` est utilisé. Il est recommandé d'utiliser le NTRIP sécurisé dès que cela est possible.
:::