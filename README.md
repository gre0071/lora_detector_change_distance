## THIS MODULE IS CURRENTLY UNDER DEVELOPMENT
---

---
# README
# LoRaWAN Detection - Change distance
This detector serves for detection changing distance between device and gateway. Detection is for fixed-position devices, if the attacker transfers the device, the RSSI (Received Signal Strength Indication) changes. This may vary depending on the environment, such as weather. Therefore, it is possible to set the variance for RSSI. Base RSSI value is defined by the first received message from device to detector.

![alt text](https://github.com/gre0071/lora_detector_change_distance/blob/master/change_distance.png)

## Description
## Interfaces
- Input: One UniRec interface
Template must contain fields TIMESTAMP, RSSI, PHY_PAYLOAD.

- Output: One UniRec interface
Template contain this fields DEV_ADDR, TIMESTAMP, BASE_RSSI, RSSI, VARIANCE.
  
## Parameters
### Module specific parameters
- `-a  --variance <double>`         Define variance, default value 10% (0.1).

### Common TRAP parameters
- `-h [trap,1]`      Print help message for this module / for libtrap specific parameters.
- `-i IFC_SPEC`      Specification of interface types and their parameters.
- `-v`               Be verbose.
- `-vv`              Be more verbose.
- `-vvv`             Be even more verbose.
