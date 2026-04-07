<script setup>
import MountpointAvailabilityChecker from '../../components/MountpointAvailabilityChecker.vue'
</script>

# Mettre à niveau le récepteur de base RTK
Les premières bases du réseau Centipede-RTK ont été construites avec un récepteur u-blox ZED-F9P et une antenne bi-bande (L1, L2), qui constituait la meilleure option disponible à l'époque. Depuis, [des récepteurs prenant en charge davantage de bandes et de signaux sont apparus](./hardware-assembly/select-receiver.md). Ces récepteurs peuvent fournir davantage d'observations, ce qui peut améliorer la précision et la fiabilité. Il est donc recommandé de mettre à niveau le récepteur et l'antenne de votre base si vous disposez d'une ancienne installation.

:::warning
Commencez par **déconnecter la base du caster**, car le changement d'antenne modifiera les coordonnées réelles de la station de base. **Vous devrez recalculer et reconfigurer les coordonnées** avant de la reconnecter.
Sur rtkbase, vous pouvez simplement désactiver `NTRIP Service A`.
:::

:::info
Certaines antennes indiquées comme « bi-bande » sont en réalité capables de recevoir d'autres bandes. Vérifiez attentivement les spécifications auprès du fabricant pour en être sûr. Dans ce cas, il peut suffire de changer uniquement le récepteur, sans recalculer la position. Cela peut aussi être vérifié en direct avec le logiciel du fabricant ou avec l'outil [RTCM3 NTRIP Live Stream Analyzer](https://y3n.co/ntrip-rtcm-analyzer/).
:::

Remplacez ensuite l'ancien récepteur et l'ancienne antenne par du matériel neuf. Suivez les instructions de [Sélectionner un récepteur](./hardware-assembly/select-receiver.md) pour choisir le récepteur.

Après l'installation du nouveau récepteur et de la nouvelle antenne, vous devrez recalculer les coordonnées de la station de base, car elles auront changé à cause de la nouvelle position de l'antenne. Suivez les instructions de [Calculer les coordonnées](./positioning/index.md) pour le faire.

Enfin, envoyez un e-mail à `contact@centipede.fr` avec les nouveaux détails matériels et le nouveau rapport de coordonnées. Une fois la confirmation reçue, vous pourrez reconnecter la base au caster.

:::info
Si vous souhaitez utiliser la base immédiatement, vous pouvez temporairement changer le nom du mountpoint pour un autre nom **disponible**. L'important est de **ne pas utiliser le nom de mountpoint déclaré tant que les nouvelles coordonnées n'ont pas été calculées et déclarées.**

<MountpointAvailabilityChecker lang="fr" />
:::
