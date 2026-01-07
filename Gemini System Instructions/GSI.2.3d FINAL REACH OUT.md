# GSI.2.3d FINAL REACH OUT 
DYNAMIC COMPONENTS

#### **Cause Template (HTML)**
*Select the relevant lines and remove non-applicable items.*

```html
<h4>SECURITY SERVICE IMPACT</h4>
<ul>
    <li><strong>System:</strong> Vostio AM | Visionline | Vision | ElSafe | Vostio LS | DoorBird</li>
    <li><strong>Impacts:</strong> Users | Keys | Locks | Safes | BluFi</li>
</ul>

<h4>ROOT CAUSE</h4>
<ul>
    <li><strong>Software:</strong> Corrupt install | Missing files | Incorrect FW | Out of Date driver</li>
    <li><strong>Hardware:</strong> Damaged parts | Elsafe failure</li>
    <li><strong>Config:</strong> Bad device/Network settings | Windows permissions</li>
    <li><strong>Data:</strong> DB support (add/remove)</li>
    <li><strong>Training:</strong> Tool misuse | Misunderstanding</li>
</ul>
```

#### **Resolution Notes Template (HTML)**
*Select the relevant categories and remove non-applicable items.*

```html
<h4>OUT-OF-SCOPE</h4>
<ul>
    <li><strong>Local Net:</strong> Firewall | DCOM | Perms | AV | Port fwd | Unreachable | Layer 8</li>
    <li><strong>3rd Party:</strong> PMS | Mobile Key provider | Hilton DKTK</li>
</ul>

<h4>IN-SCOPE</h4>
<ul>
    <li><strong>Vostio/VL/Vision:</strong> User/device setup | Startup lag | LS3G Locklink data</li>
    <li><strong>Win Apps:</strong> VL/Vision Svr | Client</li>
    <li><strong>Encoders:</strong> RFID | 4010 | Timelox | Rev2+ | Mag</li>
    <li><strong>Locks:</strong> LCU Prog fail | Internal HW fail | Red light(DB) | Wrong time | Legacy Key Rejected</li>
    <li><strong>Lock Parts:</strong> LCU (_Standard _RC _MOC) | LCA | Batt Case | Lockcase | Pushbar | BLE | Zigbee | RS485 GW</li>
    <li><strong>Elsafe:</strong> _Win _HH errors | Lang file | Decode</li>
    <li><strong>BluFi:</strong> Net range</li>
</ul>

<h4>TOOLS & INTERFACES</h4>
<ul>
    <li><strong>Win Tools:</strong> RFIDConfig | LS3G | LS2G | Locklink | Safelink</li>
    <li><strong>Mobile:</strong> Vostio Svc Tool | Vostio LS App</li>
    <li><strong>Web UI:</strong> Vostio AM | Vostio LS</li>
    <li><strong>Web Tools:</strong> Encoder GUI | RS485 GW | PMS Converter</li>
</ul>

<h4>REMEDIATION</h4>
<ul>
    <li><strong>SW:</strong> Reinstall/repair UI | Reprog Device (Vostio Tool | LS3G| LS2G | Locklink | Safelink)</li>
    <li><strong>Data:</strong> Create/Remove/Replace a Card/User/Door | Migrate Data | Upgrade Needed</li>
    <li><strong>HW:</strong> Reconfig | Internal Failure | RMA</li>
    <li><strong>Net:</strong> Add FW/AV exceptions | Verify port fwd | Check PMS</li>
</ul>
```