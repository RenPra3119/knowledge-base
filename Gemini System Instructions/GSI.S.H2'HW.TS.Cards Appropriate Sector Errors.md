# GSI.S.H2'HW.TS.Cards Appropriate Sector Errors
```html
[code]
<h3>HOW TO: Troubleshoot "Appropriate Sector" Errors (Legacy Media)</h3>
<p><em>* VL = Visionline<br>
* UL = Mifare Ultralight (Low cost/Low security media)<br>
* EV1 = Evolution 1 (Newer standard)</em></p>

<hr>

<h4>1. The Symptom</h4>
<p>You attempt to encode a keycard, fob, or wristband and receive the error message: <strong>"The chip does not have any appropriate sectors for this card."</strong></p>

<p><strong>The Trap:</strong></p>
<ul>
    <li>You might think the encoder is broken. (It's not).</li>
    <li>You might think the cards are defective. (They aren't).</li>
</ul>

<hr>

<h4>2. The Root Cause (It's a License Issue)</h4>
<p>This error almost always occurs after a <strong>Server Upgrade</strong> or a <strong>License Change</strong>.</p>
<ul>
    <li>Modern Visionline licenses default to high-security card standards.</li>
    <li>If the customer is using older media the system must be explicitly told to allow it.</li>
    <li>If "Mifare Ultralight" is missing from the license options, the system sees the card, realizes it has no security sectors, and throws the error.</li>
</ul>

<hr>

<h4>3. Diagnosis: Confirming the Mismatch</h4>

<p><strong>Step A: Verify the Media Type</strong></p>
<ul>
    <li>Ask the customer what they are using (White/Red Wristbands, generic white cards).</li>
    <li>Use the <strong>NXP TagInfo</strong> app (on a phone) or look up the Sales Order.</li>
    <li>If the media is <strong>Mifare Ultralight (UL)</strong> or <strong>Ultralight EV1</strong>, proceed to Step B.</li>
</ul>

<p><strong>Step B: Check Visionline Support</strong></p>
<ol>
    <li>Log into Visionline.</li>
    <li>Go to <strong>Reports > System Settings</strong>.</li>
    <li>Scroll down to the <strong>Options</strong> section.</li>
    <li>Look for a list titled <strong>"Supported Cards"</strong> or <strong>"Card Technology"</strong>.</li>
    <li><strong>CRITICAL:</strong> Does it list <code>Mifare Ultralight</code>?
        <ul>
            <li><strong>YES:</strong> The issue might actually be the card or encoder hardware.</li>
            <li><strong>NO: STOP.</strong> You have found the root cause. The license is missing the option.</li>
        </ul>
    </li>
</ol>

<hr>

<h4>4. The Resolution</h4>
<p>You cannot fix this in the settings menu. You must update the System License.</p>
<ol>
    <li>Obtain the <strong>System Code</strong> from <code>Reports > System Settings</code>.</li>
    <li>Contact the <strong>Global Licensing Team</strong> (or submit an internal order).</li>
    <li>Request a <strong>"License Update"</strong> or <strong>"Option Code"</strong> to enable: <strong>Mifare Ultralight Support</strong> (and/or Ultralight EV1 depending on media).</li>
    <li>Once you receive the code, go to <strong>Tools > Option Code</strong> in Visionline and apply it.</li>
    <li>Restart Visionline services. The error will vanish.</li>
</ol>
[/code]
```