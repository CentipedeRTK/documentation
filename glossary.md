# Glossary
| Term | Definition |
|------|------------|
| **Base** | Also named RTK base, reference station, station: physical GNSS receiver and antenna setup producing corrections (observations) that rovers can use to reach high-precision positioning |
| **Rover** | GNSS receiver setup that uses corrections from a base to compute its position with high precision |
| **Caster** | Server that receives the corrections from the base and makes them available to rovers via NTRIP protocol |
| **Mountpoint** | Also named point de montage in French: unique identifier of a correction
| **Correction** | Also named observation: data produced by the base that allows rovers to compute their position with high precision |
| **RTK** | Real-Time Kinematic: technique that uses corrections from a base to compute the position of a rover with high precision in real time |
| **Post-processing** | Technique that uses corrections from a base to compute the position of a rover with high precision after the data collection, not in real time. |
| **RINEX** | Receiver Independent Exchange Format: standard format for storing GNSS observations, which can be used for post-processing, such as defining the real position of the base |
| **NTRIP** | Networked Transport of RTCM via Internet Protocol: protocol used to transmit corrections from the caster to the rovers |
| **RTCM3** | Radio Technical Commission for Maritime Services version 3: standard format for corrections, which can be used in real time by rovers to compute their position with high precision |
| **MSM7** | Message type in RTCM3 that contains a complete set of observations with highest accuracy, including pseudorange, carrier phase, Doppler, and signal strength for all tracked satellites |
| **MSM4** | Message type in RTCM3 that contains a reduced set of observations with lower accuracy, including pseudorange and carrier phase with reduced resolution, and signal strength for all tracked satellites |
| **GGA** | NMEA sentence type that contains the position of the rover, which is used by the caster to determine which base is closest to the rover for the `NEAR` or `NEAR4` mountpoints |