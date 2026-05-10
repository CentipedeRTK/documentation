---
title: Access corrections
---

# Access corrections

Corrections are accessible through the NTRIP protocol, which is widely supported by RTK software and hardware. To connect to the Centipede-RTK network, you will need an NTRIP client and the following connection details:
- **Hostname**: `crtk.net`
- **Port (unsecure)**: `2101`
- **Port (secure NTRIP 2.0 with TLS only)**: `443`
- **Mountpoint**
  - `NEAR`: nearest base station with complete MSM7 corrections
  - `NEAR4`: same principle as `NEAR` but with lighter MSM4 corrections
  - Mountpoint can also be selected manually using its name, which can be found on the [coverage map](https://map.centipede-rtk.org/index.php/view/map?repository=cent&project=centipede)
- No credentials, but can also work with:
  - **Username**: `centipede`
  - **Password**: `centipede`
- **Format**: RTCM3
- **NTRIP version**: 1 and 2 are supported

:::warning
**`NEAR` or `NEAR4` mountpoints need to receive NMEA GGA sentences to start sending corrections**
:::

:::warning
**Some receivers do not support high bitrate correction streams (MSM7), like provided by the `NEAR` mountpoint. In this case, it is recommended to use the `NEAR4` mountpoint, which provides lighter corrections.**
:::

:::warning
**Secure NTRIP (with TLS) is only supported by some clients. If your client does not support it, you can use the unsecure port, but be aware that your connection will not be encrypted.** Attackers with access to the network could potentially intercept and modify the correction data, which could lead to incorrect positioning and also access rover position if `NEAR` is used. It is recommended to use secure NTRIP whenever possible.