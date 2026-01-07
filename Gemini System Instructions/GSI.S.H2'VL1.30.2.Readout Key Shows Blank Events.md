```html
[code]
<h3>HOW TO: Fix Readout Key Showing Blank Events (VL v1.30.2)</h3>

<hr>

<h4>Root Cause</h4>
<p>A known bug in Visionline v1.30.2 causes a failure when reading event logs from a Readout key. The key appears to function correctly at the lock, but when it is read back at the encoder, the Visionline software displays a blank event log, as if no data was collected.</p>

<hr>

<h4><strong>CRITICAL: Solution Requires a Special Option Code</strong></h4>
<p>This issue cannot be resolved through standard troubleshooting. It requires a specific, free of charge (FOC) option code to patch the system's data handling directory.</p>

<hr>

<h4>Standard Resolution Path</h4>
<ol>
    <li>Submit a Free of Charge (FOC) option code request through the standard ordering process.
        <ul>
            <li><strong>CRITICAL:</strong> In the comment section of the request, you <strong>MUST</strong> include the note: <code>"Temp DATA Dir Code"</code>.</li>
        </ul>
    </li>
    <li>Once you receive the option code, upload it to the Visionline server like any other license.</li>
    <li>After the code has been successfully applied, have the user create a brand new Readout key.
        <ul>
            <li>Old or existing Readout keys will not work.</li>
        </ul>
    </li>
    <li>Test the new key:
        <ul>
            <li>Use the new Readout key at a lock.</li>
            <li>Place the key on the encoder and read the events in Visionline.</li>
            <li>Confirm that the event data is now visible as expected.</li>
        </ul>
    </li>
</ol>
[/code]
```