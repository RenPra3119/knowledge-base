```html
[code]
<h3>HOW TO: Verify Marriott PKI Certificate</h3>
<p><em>* MMC = Microsoft Management Console<br>
* PKI = Public Key Infrastructure (The digital ID card for the server)</em></p>

<hr>

<h4>1. Open the Certificate Store</h4>
<ol>
    <li>Press <strong>Windows Key + R</strong> on your keyboard.</li>
    <li>Type <code>mmc.exe</code> and press <strong>Enter</strong>.</li>
    <li>Click <strong>File > Add/Remove Snap-in...</strong></li>
</ol>

<hr>

<h4>2. Add the Certificates Snap-in</h4>
<ol>
    <li>In the left list ("Available snap-ins"), select <strong>Certificates</strong> and click <strong>Add ></strong>.</li>
    <li>Select <strong>Computer account</strong> and click <strong>Next</strong>.</li>
    <li>Select <strong>Local computer</strong> and click <strong>Finish</strong>.</li>
    <li>Click <strong>OK</strong> to close the snap-in window.</li>
</ol>

<hr>

<h4>3. Check for the Certificate</h4>
<ol>
    <li>In the left pane, expand <strong>Certificates (Local Computer)</strong>.</li>
    <li>Expand the <strong>Personal</strong> folder.</li>
    <li>Click on the <strong>Certificates</strong> folder.</li>
</ol>

<p><strong>What to Look For:</strong></p>
<ul>
    <li>You should see a certificate issued to your property's specific server name (often starts with your MARSHA code, e.g., RNOSO...).</li>
    <li><strong>Managed Properties:</strong> Name usually starts with <strong>M</strong>.</li>
    <li><strong>Unmanaged Properties:</strong> Name usually starts with <strong>U</strong>.</li>
    <li><strong>Check the Expiration Date:</strong> If the date has passed, the certificate is invalid and Mobile Key will fail.</li>
</ul>

<p><strong>Note:</strong> If this certificate is missing or expired, you <strong>MUST</strong> contact Marriott to order a new one before we can proceed with installation.</p>
[/code]
```