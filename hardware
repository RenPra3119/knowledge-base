---
title: Hardware Troubleshooting
---

# Hardware Guides

## Lock Service 3G (LS3G)

### Install Drivers on ARM64 (Surface Pro X)
*Fix for yellow triangle in Device Manager on ARM PCs.*

1.  **Diagnosis:** Check Settings > System > About. If "ARM-based processor", standard drivers will fail.
2.  **Download:** Go to [FTDI VCP Drivers](https://ftdichip.com/drivers/vcp-drivers/). Download the **ZIP** for Windows Universal (ARM64).
3.  **Install:**
    *   Extract ZIP to Desktop.
    *   Device Manager > Right-click Device > Update Driver.
    *   Browse to the `\ARM64\Release` folder inside your download.

### Voltage Readings (The 10V Lie)
*   **Standard Locks (LCU):** 10V is a placeholder. It requires an operation (opening door) to calibrate to real voltage (4.5V).
*   **RCs / MOCs:** LS3G **cannot** read voltage on these. It will always show 10V. Use a multimeter.
    *   *Warning:* If an RC shows *less* than 10V in software, you have a severe power failure.

### Get Lock Events
**The Critical Rule:** LS3G does not sync live. You must (1) Readout at the door, (2) Save to Laptop, (3) Upload to Server.

1.  **At Door:** Readout > LockLog > **SAVE**.
2.  **On Network:** Database > LockLog > Select Saved Log > **UPLOAD**.
3.  **In Visionline:** Reports > Read-outs.

---

## Lock Hardware

### Jumpstart a Lock (Hard Reset)
*For legacy LockLink units only.*

1.  **Kill Power:** Remove one battery. Insert card 20 times to drain capacitors.
2.  **Prep LL:** Select Room > Upload > Prog.
3.  **The Move:** Simultaneously insert the battery AND the service cable.
    *   *Success:* Loading bar appears.
    *   *Fail:* Red light. Drain power and retry.

### Cannot Unlock CU (Remote Controllers)
*Error: "Cannot Unlock CU"*

*   **Path A (Direct Lock):** In Visionline, "External Relay" is **unchecked**. Wire to Pins 5 & 6.
*   **Path B (Gateway/3rd Party):** In Visionline, "External Relay" is **checked**. Wire to Pins 11 & 12.
