# GSI.S.H2'VL1.30.x DB.Recovery for Lock Factory Reset
[code]
<h3>HOW TO: Recover DB for Lock Factory Reset (VL v1.30.x)</h3>

<hr>

<h4>Root Cause</h4>
<p>In Visionline v1.30.x, if the database is corrupted or the system context is lost, the software may prevent you from programming, initializing, or factory resetting locks, effectively locking you out of your own hardware. Standard troubleshooting fails because the modern software versions lack the legacy recovery tools needed to reclaim the system's identity.</p>

<hr>

<h4><strong>CRITICAL: This is a LAST RESORT Recovery Procedure</strong></h4>
<ul>
    <li>This is a non-standard, <strong>high-risk</strong> process. It should only be performed after all standard troubleshooting has failed and you have been advised to do so by T2/T3/CRT.</li>
    <li>The primary goal of this procedure is <strong>ONLY</strong> to regain control of the physical locks so they can be factory reset.</li>
    <li><strong>DO NOT</strong> continue to use the database after this recovery. It will be unstable and is considered compromised.</li>
    <li>The <strong>FINAL</strong> step after regaining control of your locks will be to perform a full Visionline database rebuild and re-license your system.</li>
</ul>

<hr>

<h4>Requirements</h4>
<ul>
    <li>A Visionline v1.30.x System ID key from the problematic system.</li>
    <li>A valid staff key made on the v1.30.x system.</li>
    <li>Visionline v1.27.1 installation file.</li>
    <li>The <strong>TLRecovery.exe</strong> tool from the v1.27.1 installation package.</li>
    <li>Lock Service 3G (LS3G) compatible with v1.27.1.</li>
</ul>

<hr>

<h4>Phase 1: Time Travel (Software Downgrade)</h4>
<ol>
    <li>Completely uninstall Visionline v1.30.x from the server.</li>
    <li>Perform a fresh installation of Visionline v1.27.1 as a new, blank demo system.</li>
</ol>

<hr>

<h4>Phase 2: The Heist (System ID Recovery)</h4>
<ol>
    <li>On the new v1.27.1 server, locate and run the <code>TLRecovery.exe</code> tool.</li>
    <li>Choose <strong>Option 2 ("Set System ID")</strong>.</li>
    <li>When prompted, place the v1.30.x System ID key on the encoder.</li>
    <li>When prompted, place the v1.30.x staff key on the encoder.</li>
    <li>The tool will recover the System ID from the keys and apply it to your blank v1.27.1 database.</li>
</ol>

<hr>

<h4>Phase 3: Reclaim Your Locks</h4>
<ol>
    <li>On the now-recovered v1.27.1 system, register and download data to your LS3G laptop.</li>
    <li>Go to the physical lock(s) that you were unable to program.</li>
    <li>You should now be able to successfully connect with LS3G and perform a <strong>Factory Reset</strong> and/or <strong>Initialize Lock</strong>.</li>
</ol>

<hr>

<h4>Phase 4: Rebuild from the Ashes</h4>
<ol>
    <li>Once all locks are recovered and functional, <strong>STOP</strong> using the v1.27.1 system.</li>
    <li>Proceed with a standard database rebuild process onto the desired, current version of Visionline (e.g., v1.30.2).</li>
    <li>Since the system code will be new, you will need to re-order the appropriate licenses for your system.</li>
</ol>
[/code]