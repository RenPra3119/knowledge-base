
[code]
<h3>HOW TO: Understand LS3G Voltage Readings</h3>
<p><em>* LS3G = Lock Service 3G<br>
* LCU = Lock Control Unit (Standard battery-powered lock brain)<br>
* RC = Remote Controller<br>
* MOC = Multi-Output Controller (Elevator Reader)</em></p>

<hr>

<h4>1. The "10-Volt Lie" Explained</h4>
<p>The LS3G software has a quirk where it can display a voltage of "10V".</p>
<ul>
    <li>This is <strong>NOT</strong> a real reading. It is a default placeholder value in the software.</li>
    <li>A battery-powered lock (LCU) runs on ~4.5V. A 10V reading is physically impossible.</li>
    <li>An RC or MOC runs on 12V or 24V, so a 10V reading is also incorrect.</li>
</ul>

<hr>

<h4><strong>CRITICAL: Voltage Reading Rules by Device Type</strong></h4>
<p>How you interpret the voltage in LS3G depends entirely on what you are connected to.</p>

<p><strong>Rule 1: For Standard Locks (LCUs)</strong></p>
<ul>
    <li>After a firmware upload or changing a power-related setting (e.g., battery type), the LCU's voltage calibration is reset.</li>
    <li>LS3G will temporarily display the default <strong>10V</strong> placeholder.</li>
    <li>The lock needs to perform a few operations (e.g., being opened with a card) to recalibrate itself.</li>
    <li>A subsequent parameter readout will then show the correct voltage (typically <strong>4.0V - 4.8V</strong>).</li>
    <li><strong>Conclusion:</strong> A 10V reading on a battery lock is temporary and normal after programming.</li>
</ul>

<p><strong>Rule 2: For RCs and MOCs (Elevator Readers)</strong></p>
<ul>
    <li>These devices are powered by an external 12V or 24V power supply.</li>
    <li>The LS3G software <strong>CANNOT</strong> read the true voltage of these devices.</li>
    <li>It will <strong>ALWAYS</strong> display the default 10V placeholder, regardless of the actual input power.</li>
    <li><strong>Conclusion:</strong> The LS3G voltage reading for RCs and MOCs is completely meaningless. You <strong>MUST</strong> use a multimeter to diagnose power issues with these devices.</li>
</ul>

<p><strong>Rule 3: The Exception That Proves the Rule</strong></p>
<ul>
    <li>There is only ONE time the LS3G voltage reading for an RC or MOC is useful.</li>
    <li>If LS3G displays a voltage <strong>LESS THAN 10V</strong> (e.g., 8.2V, 6.5V) for an RC or MOC, this indicates a <strong>SEVERE</strong> power supply or wiring issue. The device is receiving so little power that it cannot even maintain its own default placeholder value in the software.</li>
    <li><strong>Conclusion:</strong> If you see less than 10V on an RC or MOC, you have definitively found a power problem.</li>
</ul>
[/code]