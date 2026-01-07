# GSI.S.H2'HW.TS.Cannot Unlock CU on Remote Controllers
```html
[code]
<h3>HOW TO: Troubleshoot "Cannot Unlock CU" on Remote Controllers</h3>
<p><em>* RC = Remote Controller<br>
* CU = Controller Unit (in this context, the external device the RC is trying to control)<br>
* VL = Visionline<br>
* LS3G = Lock Service 3G<br>
* NC/NO = Normally Closed / Normally Open</em></p>

<hr>

<h4>1. Root Cause Analysis: What "Cannot Unlock CU" Actually Means</h4>
<p>This error rarely indicates a problem with the RC's main board. It means:</p>
<ul>
    <li>The RC is reading the key correctly.</li>
    <li>The RC is sending the "unlock" signal correctly.</li>
</ul>
<p><strong>The Problem:</strong> The signal is being sent to the wrong place, or the device it is talking to is asleep, broken, or wired incorrectly.</p>

<p><strong>Common Causes:</strong></p>
<ul>
    <li><strong>Programming Mismatch:</strong> You told the RC to use its <em>internal</em> relay, but you wired it to an <em>external</em> device.</li>
    <li><strong>Physical Mismatch:</strong> You are using the wrong screw terminals on the back of the RC.</li>
    <li><strong>Hardware Failure (External):</strong> The gateway, power supply, or electrified strike is dead or needs a reboot.</li>
    <li><strong>Visionline Mismatch:</strong> The door setup in Visionline does not match the physical wiring.</li>
</ul>

<hr>

<h4>2. Wiring & Configuration Rules</h4>
<p>An RC can function in two ways. You <strong>MUST</strong> know which method is being used.</p>

<p><strong>Path A: Internal Relay (Controlling a Simple Lock/Strike Directly)</strong></p>
<ul>
    <li><strong>Visionline:</strong> The "External Relay" box is <strong>NOT</strong> checked.</li>
    <li><strong>Physical Wiring:</strong> Power on Pins 1 (-) & 2 (+). The signal output is on <strong>Pins 5 & 6</strong>.</li>
</ul>

<p><strong>Path B: External Relay (Talking to a Gateway or Third-Party Controller)</strong></p>
<ul>
    <li><strong>Visionline:</strong> The "External Relay" box <strong>IS</strong> checked.</li>
    <li><strong>Physical Wiring:</strong> Power on Pins 1 (-) & 2 (+). The signal output is on <strong>Pins 11 & 12</strong>.</li>
</ul>

<hr>

<h4>3. Diagnostic Flowchart</h4>

<p><strong>Step 1: Does the RC give a green light when you present a valid key?</strong></p>
<ul>
    <li><strong>NO:</strong> This is not a "Cannot Unlock CU" issue. It is a power or key validity problem. Stop here.</li>
    <li><strong>YES:</strong> The RC logic is working. Proceed to Step 2.</li>
</ul>

<p><strong>Step 2: What is the RC <em>supposed</em> to be unlocking?</strong></p>
<ul>
    <li><strong>A lock/strike directly:</strong> You are on <strong>Path A</strong>. Go to Step 3.</li>
    <li><strong>A Gateway (RS485, Zigbee, etc.):</strong> You are on <strong>Path B</strong>. Go to Step 4.</li>
</ul>

<p><strong>Step 3: Troubleshooting Path A (Internal Relay - Pins 5 & 6)</strong></p>
<ol>
    <li>In VL, confirm the "External Relay" box is <strong>NOT</strong> checked. If it is, uncheck it and re-initialize the RC.</li>
    <li>Get a multimeter and set it to continuity mode.</li>
    <li>Place probes on <strong>Pins 5 & 6</strong>.</li>
    <li>Present a valid key.
        <ul>
            <li><strong>If it beeps:</strong> The RC is working. The problem is in the wiring <em>after</em> the RC or the lock hardware.</li>
            <li><strong>If it does NOT beep:</strong> The RC's internal relay has failed. Request an RMA.</li>
        </ul>
    </li>
</ol>

<p><strong>Step 4: Troubleshooting Path B (External Relay - Pins 11 & 12)</strong></p>
<ol>
    <li>In VL, confirm the "External Relay" box <strong>IS</strong> checked. If not, check it and re-initialize the RC.</li>
    <li>Confirm wires from the Gateway are on <strong>Pins 11 & 12</strong>.</li>
    <li><strong>Check the Gateway:</strong> Is it powered on? Try power-cycling the Gateway.</li>
    <li>If the Gateway seems fine, test the RC relay with a multimeter on <strong>Pins 11 & 12</strong>.
        <ul>
            <li><strong>If it beeps:</strong> The RC is working. The problem is the Gateway or the wiring.</li>
            <li><strong>If it does NOT beep:</strong> The RC's external relay has failed. Request an RMA.</li>
        </ul>
    </li>
</ol>
[/code]
```