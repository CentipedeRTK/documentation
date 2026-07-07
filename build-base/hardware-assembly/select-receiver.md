# Select a base GNSS receiver
When building a base station, the first step is to select a GNSS receiver. The choice of the receiver will depend on several factors, such as the budget, the required performance, the supported bands and signals, and the compatibility with the Centipede-RTK network.

Best performance is reached with [Septentrio Mosaic-X5 receiver](./receivers/septentrio-mosaic-x5.md). [Unicore UM980 or UM982 receivers](./receivers/unicore-um98x.md) can also be used, as lower-cost alternatives. u-blox F9P receiver is not accepted anymore as a [declared](../declaration.md) base station in the Centipede-RTK network, due to its limited signal support.

## Recommended receiver models
- [Septentrio Mosaic-X5](./receivers/septentrio-mosaic-x5.md)
- [Unicore UM980/UM982](./receivers/unicore-um98x.md)

:::warning
The u-blox F9P receiver is no longer accepted as a new [declared](../declaration.md) base station in the Centipede-RTK network due to its limited signal support.
:::

## Future receivers
- u-blox X20P module is now usable since firmware HPG 2.10, since it includes back GLONASS constellation in most of the world. However, the signal plan contains less signals than the above selected receivers so it is less recommended. F20P variant is also missing signals E6 and B3, so it is not recommended for a base station.

Other receivers may also be considered, subject to approval on a case-by-case basis. 

:::warning
***rtkbase* is not compatible yet with other receivers than ublox F9P, Mosaic-X5 and UM98x.**
:::
