[code]
<h3>HOW TO: Install LS3G Drivers on ARM64 Devices (Surface Pro X)</h3>
<p><em>* ARM64 = CPU Architecture used by Surface Pro X and other "Always Connected" PCs.<br>
* x64/x86 = Standard Intel/AMD Architecture.<br>
* FTDI = The manufacturer of the USB Service Cable chip.</em></p>

<hr>

<h4>1. Diagnosis: Is this an ARM Device?</h4>
<p>If the Lock Service 3G cable is not detected (yellow triangle in Device Manager), check the system type.</p>
<ol>
    <li>Go to <strong>Settings > System > About</strong>.</li>
    <li>Look at <strong>System type</strong>.</li>
    <li>If it says <strong>"ARM-based processor"</strong> or <strong>"64-bit operating system, ARM-based processor,"</strong> the standard installer will <strong>FAIL</strong>.</li>
</ol>

<hr>

<h4>2. Download the Correct Driver Package</h4>
<p><em>Do not rely on the drivers included with the Visionline installer.</em></p>
<ol>
    <li>Go to the FTDI Chip website: <a href="https://ftdichip.com/drivers/vcp-drivers/">https://ftdichip.com/drivers/vcp-drivers/</a></li>
    <li>Scroll down to the table.</li>
    <li>Locate the row for <strong>Windows</strong> (Universal).</li>
    <li>Download the <strong>ZIP file</strong> link (Setup Executable often fails on ARM).<br>
    <em>Filename Example:</em> <code>CDM-v2.12.36.20-for-ARM64-WHQL-Certified.zip</code></li>
    <li><strong>Extract</strong> the ZIP file to a folder on the desktop (e.g., <code>New Folder</code>).</li>
</ol>

<hr>

<h4>3. The "Force Feed" (Manual Installation)</h4>
<p><em>The automatic installer often fails to locate the ARM folder. You must point to it manually.</em></p>
<ol>
    <li>Plug in the USB Service Cable.</li>
    <li>Open <strong>Device Manager</strong>.</li>
    <li>Locate the device under "Other Devices" (usually "FT232R USB UART" or similar with a yellow warning icon).</li>
    <li>Right-click the device > <strong>Update driver</strong>.</li>
    <li>Select <strong>"Browse my computer for drivers"</strong>.</li>
    <li>Click <strong>Browse...</strong> and navigate to the extracted folder from Step 2.</li>
    <li><strong>CRITICAL:</strong> You must select the <code>\ARM64\Release</code> sub-folder inside the download.</li>
    <li>Click <strong>Next</strong>.</li>
    <li>Windows should now successfully install the driver and recognize the device as a "USB Serial Port."</li>
</ol>

<hr>

<h4>4. Verification</h4>
<ol>
    <li>Open <strong>Lock Service 3G</strong>.</li>
    <li>Go to <strong>Setup > System ID</strong>.</li>
    <li>Verify that the "Port" dropdown now lists a COM port (e.g., COM3, COM4).</li>
    <li>If the port appears, the driver is working.</li>
</ol>
[/code]