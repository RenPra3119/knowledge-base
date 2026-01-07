```html
[code]
<h3>HOW TO: Get Lock Events (LS3G)</h3>
<p><em>* LS3G = Lock Service 3G (the software on your service laptop)<br>
* VL = Visionline (the main server software)</em></p>

<hr>

<h4><strong>CRITICAL: The Two-Step Process Explained</strong></h4>
<p>LS3G is a simple data collector. It does not talk to Visionline in real-time.</p>
<ul>
    <li><strong>Step 1 is Collecting:</strong> You go to a lock and pull the raw data (the LockLog).</li>
    <li><strong>Step 2 is Uploading:</strong> You connect the laptop to the network and send that collected data to the VL server.</li>
</ul>
<p><strong>If you do not perform both steps, the data will never appear in Visionline.</strong></p>

<hr>

<h4>1. In LS3G: Collect and Save the Lock Events (At the Door)</h4>
<ol>
    <li>Connect the USB service cable to the lock.</li>
    <li>In LS3G, go to <strong>Readout > LockLog</strong>.</li>
    <li>Select the number of events you want to pull and click the <strong>Readout</strong> button.</li>
    <li>The events will populate the list. You will only see card registration numbers, not names. This is normal.</li>
    <li><strong>CRITICAL:</strong> Click the <strong>Save</strong> button. This saves the collected events to the local database on your LS3G laptop, preparing them for upload.</li>
</ol>

<hr>

<h4>2. In LS3G: Upload the Saved Events (On the Hotel Network)</h4>
<ol>
    <li>Ensure your LS3G laptop is connected to the same network as your VL server.</li>
    <li>In LS3G, go to <strong>Database > LockLog</strong>.</li>
    <li>You will now see a "Stored logs" section at the top. Find and select the log you just saved.</li>
    <li>Click the <strong>Upload</strong> button.</li>
    <li>A progress bar will confirm the data is being sent to the VL server.</li>
</ol>

<hr>

<h4>3. In Visionline: View the Uploaded Report</h4>
<ol>
    <li>On any VL client or server PC, go to the <strong>Reports</strong> tab.</li>
    <li>Double-click on <strong>Read-outs</strong>.</li>
    <li>Your uploaded log will now appear in the list, identified by the door name and the time of the readout.</li>
    <li>When you open this report, Visionline will automatically cross-reference the raw registration numbers with its main database and display the associated user/guest names.</li>
</ol>
[/code]
```