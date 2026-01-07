```html
[code]
<h3>HOW TO: Set Time & Daylight Savings (DST)</h3>
<p><em>* DST = Daylight Saving Time<br>
* LL = LockLink<br>
* VL = VingCard Vision</em></p>

<hr>

<h4>1. Setting the Time (The Quick Fix)</h4>
<p>Use this method if the lock is just drifting or showing the wrong time, but is otherwise programmed correctly.</p>
<ol>
    <li>In LockLink: Go to the <strong>Main Menu</strong>.</li>
    <li>Tap <strong>Set Clock</strong>.</li>
    <li>Verify the time shown on the screen is correct (it pulls from your PC/Tablet system time).</li>
    <li>Tap the <strong>Set Clock</strong> button in the dialog box.</li>
    <li>Insert the Contact Card into the lock.</li>
</ol>
<p><strong>Success:</strong> The lock accepts the new time immediately.</p>
<p><strong>Note:</strong> Performing a full <strong>Upload > Prog</strong> or <strong>Upload > Data</strong> will <em>also</em> automatically set the time, but those processes take longer.</p>

<hr>

<h4>2. Handling Daylight Savings Time (The Permanent Fix)</h4>
<p>If your locks are an hour off twice a year, you need to configure how Vision handles DST.</p>

<p><strong>Step A: Check Vision Settings</strong></p>
<ol>
    <li>In Vision: Go to <strong>Setup > System Parameters</strong>.</li>
    <li>Click the <strong>Daylight Savings</strong> tab.</li>
    <li>Look at "Method of DST transfer to locks". You have two choices:</li>
</ol>

<p><strong>Choice 1: "By LockLink" (The Hard Way)</strong></p>
<ul>
    <li>Legacy method. Requires you to update locks manually.</li>
    <li><strong>How it works:</strong> Vision sends DST dates to the LockLink. You must then visit <em>every</em> lock and perform <strong>Set Clock</strong> or <strong>Upload Data</strong> once a year (usually in January) to load the new year's DST schedule.</li>
</ul>

<p><strong>Choice 2: "By Each Guest Card" (The Smart Way - Vision 6.3+)</strong></p>
<ul>
    <li>Recommended. Guest cards carry the time correction.</li>
    <li><strong>How it works:</strong> When a guest uses a new card, the card tells the lock, "Hey, it's DST now," and the lock updates itself.</li>
    <li><strong>The Catch:</strong> When you first switch to this mode, you MUST reprogram <strong>every single lock</strong> (Upload > Prog) once to teach them to listen to cards for time updates.</li>
</ul>

<hr>

<h4>3. Common Issues</h4>
<ul>
    <li><strong>"Time Drift":</strong> Cheap electronics drift. A lock can lose 2-3 minutes a month. If a guest key doesn't work, set the time first.</li>
    <li><strong>"Red Light on Entry":</strong> Often caused because the lock thinks it is 2:00 PM (checkout time) but it is actually 11:00 AM because the clock is wrong. <strong>Set Clock</strong> fixes this.</li>
</ul>
[/code]
```