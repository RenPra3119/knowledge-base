---
title: Software & Visionline
---

# Visionline Software Guides

## Time & Daylight Savings

### Quick Fix (Set Clock)
Use **LockLink**. Go to Set Clock > Verify Time > Tap Lock.

### Permanent Fix (DST Settings)
*   **Method:** Setup > System Parameters > Daylight Savings.
*   **Best Practice:** Set to "By Each Guest Card" (Vision 6.3+).
*   *Note:* Changing this requires reprogramming every lock once.

## Legacy Media Errors
*Error: "Chip does not have appropriate sectors"*

**Cause:** License missing "Mifare Ultralight" option.
**Fix:** Request "Option Code" for Ultralight/EV1 from Licensing Team. Apply via Tools > Option Code.

## Recovery Procedures

### Hilton BLE Payload Failure
**Fix:** Full reboot of the Visionline Server. Simply restarting the service is often insufficient.

### VL 1.30.2 Readout Bug
**Symptom:** Readout key works at door, but shows blank events in software.
**Fix:** Requires FOC Option Code `Temp DATA Dir Code`.
