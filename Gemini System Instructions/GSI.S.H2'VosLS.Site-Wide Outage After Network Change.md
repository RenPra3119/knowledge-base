# GSI.S.H2'VosLS.Site-Wide Outage After Network Change
[code]
<h3>HOW TO: Resolve Vostio LS Outage After Network Change</h3>
<p><em>* VLS = Vostio Location Services<br>
* LSP = Local Service Provider (Network Vendor)<br>
* SSID = Wi-Fi Network Name</em></p>

<hr>

<h4>1. Root Cause Analysis</h4>
<p>When a property's network infrastructure is changed (e.g., new LSP, new Wi-Fi SSID/password), all VLS BluFi devices will go offline.</p>
<ul>
    <li><strong>Reason:</strong> BluFi devices have their Wi-Fi credentials "hard-coded" via a template. They cannot automatically discover or adapt to new network settings.</li>
</ul>

<p><strong>CRITICAL: The "Chicken-and-Egg" Problem</strong></p>
<ul>
    <li>Devices must be <strong>online</strong> to receive a new configuration template from the cloud.</li>
    <li>Devices <strong>cannot get online</strong> because their saved Wi-Fi settings are now incorrect.</li>
    <li><em>This means you cannot simply "push" an update to offline devices.</em></li>
</ul>

<hr>

<h4>2. The Two Resolution Paths</h4>
<p>There are only two ways to resolve this. Path A is strongly preferred.</p>

<h4>Path A: The Easy Way (Temporary Network Rollback)</h4>
<p>This is the fastest and most efficient method. It requires cooperation from the customer's LSP.</p>
<ol>
    <li>Instruct the LSP to <strong>temporarily change the new network's SSID and password BACK to the OLD credentials</strong> that the BluFis were originally programmed with.</li>
    <li>Wait 30-60 minutes. The majority of BluFi devices will see their "home" network and automatically reconnect.</li>
    <li>Once the devices are online, create a new BluFi Template in the VLS portal with the <strong>NEW</strong> network credentials.</li>
    <li>Apply this new template to all BluFi devices. Wait 20-30 minutes for them to receive and apply the update.</li>
    <li>Once the devices have the new settings, instruct the LSP to <strong>switch the network back to the NEW SSID and password</strong>. The devices will disconnect and then reconnect to the new network.</li>
</ol>

<h4>Path B: The Hard Way (Manual On-Site Reprovisioning)</h4>
<p>Use this method if the LSP is unable or unwilling to perform Path A. <strong>This requires a technician to physically visit every single BluFi device.</strong></p>

<p><strong>Step 1: Create New Template in VLS Portal</strong></p>
<ul>
    <li>Log into the Bluzone (Vostio LS) portal.</li>
    <li>Create a brand new BluFi Template containing the credentials for the <strong>NEW</strong> network.</li>
    <li><em>For networks using MAC Authentication, the Security Type should be set to "Open."</em></li>
    <li>Apply this new template to all offline BluFi devices in the portal.</li>
</ul>

<p><strong>Step 2: On-Site Reprovisioning Process</strong></p>
<p>The on-site technician must have an iPhone with the <strong>"HID IoT Installer"</strong> app and valid login credentials. For <strong>EACH</strong> offline BluFi device:</p>
<ol>
    <li>Open the HID IoT Installer app and log in.</li>
    <li>Select the correct Location (e.g., "Main - Floor 1").</li>
    <li>Find the specific BluFi by name (e.g., "Meeting Room A") and select it.</li>
    <li>Scan the QR code on the physical BluFi device.</li>
    <li>The app will state the device is unprovisioned. Tap <strong>"Provision."</strong></li>
    <li>The app will connect to the device via Bluetooth and push the new Wi-Fi settings from the template you created.</li>
    <li>The BluFi will reboot and attempt to connect to the new network. It should come online in the VLS portal within a few minutes.</li>
    <li>Repeat this process for every single offline device.</li>
</ol>
[/code]