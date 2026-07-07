# Sélectionner un récepteur GNSS de base
Lors de la construction d'une base, la première étape consiste à choisir un récepteur GNSS. Le choix du récepteur dépendra de plusieurs facteurs, tels que le budget, les performances requises, les bandes et signaux pris en charge, ainsi que la compatibilité avec le réseau Centipede-RTK.

Les meilleures performances sont obtenues avec le [récepteur Septentrio Mosaic-X5](./receivers/septentrio-mosaic-x5.md). Le [récepteur Unicore UM980](./receivers/unicore-um98x.md) peut également être utilisé comme alternative moins coûteuse.

## Modèles de récepteurs recommandés
- [Septentrio Mosaic-X5](./receivers/septentrio-mosaic-x5.md)
- [Unicore UM980/UM982](./receivers/unicore-um98x.md)

:::warning ATTENTION
Le récepteur u-blox F9P n'est plus accepté comme nouvelle station de base [déclarée](../declaration.md) dans le réseau Centipede-RTK, en raison de son support limité des signaux.
:::

## Futurs récepteurs

* Le module u-blox X20P est désormais utilisable à partir du firmware HPG 2.10, car il réintègre la constellation GLONASS dans la majeure partie du monde. Toutefois, son plan de signaux comprend moins de signaux que les récepteurs sélectionnés ci-dessus ; il est donc moins recommandé. La variante F20P ne prend pas non plus en charge les signaux E6 et B3, ce qui la rend déconseillée pour une station de base.

D'autres récepteurs peuvent également être envisagés, sous réserve d'une approbation au cas par cas.

:::warning ATTENTION
**rtkbase n'est pas encore compatible avec d'autres récepteurs que les modèles u-blox F9P, Mosaic-X5 et UM98x.**
:::