---
title: Hardware Troubleshooting
---
# Hardware Guides
# [Lock Service 3G (LS3G)][Lock Service 3G (LS3G)]
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
