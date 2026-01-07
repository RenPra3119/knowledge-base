# GSI.S.H2'VL.Understand the Visionline Ecosystem
```html
[code]
<h3>HOW TO: Understand the Visionline Ecosystem (Terminology)</h3>
<p><em>* VL = Visionline<br>
* LCU = Lock Controller Unit<br>
* AES = Advanced Encryption Standard<br>
* PMS = Property Management System</em></p>

<hr>

<h4>1. The Core Components (The Big Pieces)</h4>
<ul>
    <li><strong>Visionline Server:</strong> The "Big Brain." The central computer that runs everything. If this is down, the system is offline.</li>
    <li><strong>Visionline Client:</strong> The "Little Brain." The software on front desk PCs that talks to the main server.</li>
    <li><strong>RFID Encoder:</strong> The device that writes data onto keycards.
        <ul>
            <li><strong>Black Encoders:</strong> Legacy units, connect via USB or Ethernet.</li>
            <li><strong>4010 Encoders:</strong> Newer Linux-based units, usually connect via Ethernet.</li>
        </ul>
    </li>
</ul>

<hr>

<h4>2. The Guts (Physical Lock Parts)</h4>
<ul>
    <li><strong>LCU (Lock Controller Unit):</strong> The logic board inside the door lock. It decides if a key is valid.</li>
    <li><strong>Lock Case:</strong> The metal mortise with the latch and deadbolt. It provides the physical security.</li>
    <li><strong>Spindle:</strong> The metal square connecting the handle to the lock case. If broken or misaligned, the handle will not retract the latch.</li>
    <li><strong>Zigbee Board:</strong> An optional radio board inside the lock for "Online" communication with the server.</li>
    <li><strong>Broker (Hilton BLE Board):</strong> A third-party Bluetooth board (Hilton specific) that connects to the LCU to allow Mobile Key access.</li>
</ul>

<hr>

<h4>3. The Service Tools</h4>
<ul>
    <li><strong>LS3G (Lock Service 3G):</strong> The primary service software installed on a laptop. Used to talk directly to a lock for programming, log reading, and troubleshooting.</li>
    <li><strong>USB Interface 3G:</strong> The service cable that connects the laptop to the lock. It requires specific FTDI drivers.</li>
    <li><strong>DKTK (Digital Key Toolkit):</strong> A Hilton-specific tool (tablet/phone) used to "commission" (pair) Bluetooth Brokers.</li>
    <li><strong>SysMon (System Monitor):</strong> A diagnostic tool on the VL server that displays the online status of gateways and encoders.</li>
</ul>

<hr>

<h4>4. The Cards (Access vs. Function)</h4>

<p><strong>Access Cards (Open Doors)</strong></p>
<ul>
    <li><strong>Guest Card:</strong> Opens the room and cancels the previous guest.</li>
    <li><strong>Staff Card:</strong> For employees. Can be restricted by time or shift.</li>
    <li><strong>Emergency Card:</strong> The "Master" key. Opens all locks (except double-locked deadbolts in some configs) and cannot be blocked.</li>
    <li><strong>Operator Card:</strong> Used ONLY to log in to the Visionline software. Does not open doors.</li>
</ul>

<p><strong>Function Cards (Perform Actions)</strong></p>
<ul>
    <li><strong>Power Down Key:</strong> A pre-made emergency guest key for system outages.</li>
    <li><strong>Cancel Card:</strong> Carries a "block list" to the lock to stop lost/stolen staff cards.</li>
    <li><strong>Read-out Card:</strong> Extracts the event log from a lock.</li>
    <li><strong>Stand Open Card:</strong> Toggles a door to remain unlocked.</li>
    <li><strong>EMI Card:</strong> Initializes the lock's communication with Energy Management Systems (e.g., Inncom).</li>
    <li><strong>Discovery Card:</strong> Forces a lock to pair with a nearby thermostat.</li>
</ul>

<hr>

<h4>5. Integrations & Middleware</h4>
<ul>
    <li><strong>Middleware (e.g., Marriott Flow 2):</strong> The translator. It sits between the PMS and Visionline to ensure they understand each other's commands.</li>
    <li><strong>PMS Interface:</strong> The communication channel (often a TCP port like 4000) between the Middleware and Visionline.</li>
    <li><strong>Heartbeat Test:</strong> The Middleware's connectivity check. If Visionline doesn't answer, the interface shuts down.</li>
    <li><strong>Encoder Mapping:</strong> A setting in the Middleware that translates a PMS encoder ID (e.g., "1") to a Visionline Device Name (e.g., "FrontDesk_Left").</li>
    <li><strong>Common Room Conversion:</strong> Translates a PMS room code (e.g., "P") into a Visionline Door Name (e.g., "Pool").</li>
</ul>

<hr>

<h4>6. Concepts & Actions</h4>
<ul>
    <li><strong>System ID:</strong> The unique digital fingerprint of the property. Every lock and card must share this ID to function.</li>
    <li><strong>Housekeeping:</strong> An automated database task that deletes old events to prevent performance issues.</li>
    <li><strong>Initialize Lock:</strong> Using LS3G to give a lock its identity (e.g., "You are Room 101").</li>
    <li><strong>Commissioning (Hilton):</strong> Using the DKTK tool to link a Bluetooth Broker to a specific room in the cloud.</li>
    <li><strong>Factory Reset / Coldstart:</strong> Completely wiping a lock's memory. Requires a specialized "Reset Token" from the server.</li>
    <li><strong>Power Open:</strong> A specialized token used with LS3G to open a lock with dead batteries/failed electronics.</li>
</ul>
[/code]
```