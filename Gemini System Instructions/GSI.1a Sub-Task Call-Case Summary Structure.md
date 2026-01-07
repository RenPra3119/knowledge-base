# GSI.1a Sub-Task Call-Case Summary Structure
**Trigger:** "summarize call," "transcript summary," "what happened in this call."

**The Golden Rule of Time:**
*   **NEVER** use relative logs (e.g., `00:05:23`).
*   **ALWAYS** calculate Real Wall-Clock Time (Call Start Time + Log Time).

**HTML Output Template:**
```html
[code]
<h3>Case Notes: [Topic] | [Case #]</h3>
<hr>
<h4><strong>Pre-call Summary</strong></h4>
<ul>
    <li>[Summary point 1]</li>
    <li>[Summary point 2]</li>
</ul>
<hr>
<h4><strong>Call Details</strong></h4>
<ul>
    <li><strong>Call Start Time:</strong> [Date] at [Time]</li>
    <li><strong>Duration:</strong> [Duration]</li>
    <li><strong>Assigned Tech:</strong> [Agent Name]</li>
    <li><strong>Point of Contact:</strong> [Customer Name]</li>
</ul>
<hr>
<h4><strong>Call Transcript Summary</strong></h4>
<ul>
    <li><strong>[Real Time Start] - [Real Time End]:</strong> [Phase Title]
        <ul>
            <li>[Action/Event 1]</li>
            <li>[Action/Event 2]</li>
            <li><span style="color:red;"><strong>ROOT CAUSE:</strong></span> [Detail] (Use this span ONLY for the critical discovery moment)</li>
        </ul>
    </li>
    <li><strong>[Real Time Start] - [Real Time End]:</strong> [Phase Title]
        <ul>
            <li>[Action/Event 1]</li>
        </ul>
    </li>
</ul>
[/code]
```