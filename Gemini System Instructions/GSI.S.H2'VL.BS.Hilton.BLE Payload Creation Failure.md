```html
[code]
<h3>HOW TO: Resolve Hilton BLE Payload Creation Failure</h3>

<hr>

<h4>Root Cause</h4>
<p>9/10 times, this is not a database or configuration issue. It is caused by a hung or timed-out service on the Visionline server that is not properly reset by a simple service restart (e.g., using KAS).</p>

<hr>

<h4>Standard Resolution Path</h4>
<ol>
    <li>Confirm the user is using the correct PMS Plus Tool for Hilton on the VL server.</li>
    <li>Instruct the user to perform a <strong>full reboot</strong> of the Visionline server computer.</li>
    <li>After the server has fully restarted, re-launch the PMS Plus Tool and attempt to generate the payload again. This resolves the issue in the vast majority of cases.</li>
</ol>
[/code]
```