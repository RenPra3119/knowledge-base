# GSI.2.2.3rd and final RO
Keep the [code] block tags for each section. 
i want to just copy paste each section into the relevant fields in SNOW
## Block 1: Categorization & Cause (Internal Fields)
```html
[code]
<div>
    <strong>Product Category:</strong> [Insert Product Category from List]<br>
    <strong>Case Category:</strong> [Insert Case Category from List]<br>
    <strong>Cause:</strong> [Insert Root Cause from dynamic template]
</div>
[/code]
```

## Block 2: Official Record (Summary & Resolution)
```html
[code]
<div>
    <h2>Case Summary</h2>
    <p>
        [Insert technical summary of the issue, diagnostics performed, and findings. Use &lt;br&gt; for line breaks.]
    </p>

    <h2>Resolution Notes</h2>
    <p>
        [Insert final resolution details, fix actions, or reason for closure.]
    </p>
</div>
[/code]
```

## Block 3: Customer Communication (Email Body)
```html
[code]
<div>
    <h2>✅ Status: Case Closed</h2>
    <ul>
        <li><strong>Reason:</strong> [e.g., No reply after multiple attempts / Issue Resolved]</li>
        <li><strong>Details:</strong> [e.g., No contact in over two weeks / Confirmation received]</li>
    </ul>

    <h3>Next Steps</h3>
    <ul>
        <li>Assuming no further assistance is needed at this time.</li>
        <li>The case will be marked as <strong>Resolved</strong> but can be reopened within 48 hours.</li>
        <li>After that, it will close permanently, and a new case will be required.</li>
    </ul>

    <hr>

    <h3>Still Need Help?</h3>
    <p>Reply directly to this email or call <strong>(800) 225-8464</strong>.</p>
</div>
[/code]
```