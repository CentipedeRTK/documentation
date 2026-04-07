<script setup>
import MountpointAvailabilityChecker from '../components/MountpointAvailabilityChecker.vue'
</script>

# Upgrade RTK base receiver
The first bases on the Centipede-RTK network were built with the u-blox ZED-F9P receiver and a dual-band (L1, L2) antenna, which was the best option available at the time. However, since then, [receivers that support more bands and signals have become available](./hardware-assembly/select-receiver.md). These receivers can provide more observations, which can improve precision and reliability. Therefore, it is recommended to upgrade the receiver and antenna of your base if you have an older setup.

:::warning
First, **disconnect the base from the caster**, as changing the antenna will change the real coordinates of the base station, **you will need to recalculate and reconfigure the coordinates** before reconnecting.
On rtkbase, you can simply disable `NTRIP Service A`.
:::

:::info
Some antennas marked "dual-band" antennas are actually able to receive other bands. Double-check the specifications with the manufacturer to be sure. In this case, changing only the receiver can be enough, so no position recalculation is needed. This can also be checked live using manufacturer software or using [RTCM3 NTRIP Live Stream Analyzer](https://y3n.co/ntrip-rtcm-analyzer/).
:::

Then, replace the old receiver and antenna with a new one. Follow the instructions from [Select receiver](./hardware-assembly/select-receiver.md) to choose the receiver.

After installing the new receiver and antenna, you will need to recalculate the coordinates of the base station, as they will have changed due to the new antenna position. Follow the instructions from [Calculate coordinates](./positioning/index.md) to do this.

Finally, send an email to `contact@centipede.fr` with the new hardware details and the new coordinates report. Once you get a confirmation, you can reconnect the base to the caster.

:::info
If you want to use the base immediately, you can temporarily change the mountpoint name to another **available** one. The important part is to **not use the declared mountpoint name until the new coordinates are calculated and declared.**

<MountpointAvailabilityChecker lang="en" />
:::


