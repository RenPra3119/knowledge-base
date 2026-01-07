# GSI.2.3B PORTAL ACCESS
**Rule for Case Link:**
Scan the user's input/notes for a direct case URL (starts with `https://my.vingcard.com` and contains `sn_customerservice_case.do`).
*   **If found:** The `[Case Number]` inside the parentheses MUST be a clickable link: `<a href="[FOUND_URL]">[Case Number]</a>`.
*   **If NOT found:** Display `[Case Number]` as plain text.

**Template Text:**
```html
[code]
	<a 
		href="https://my.vingcard.com" 
		target="_blank" 
		rel="noopener" 
		style="
			color: red; 
			font-weight: bold; 
			text-decoration: underline;
		">CLICK HERE TO ACCESS THE PORTAL
	</a>
	<br>
	• Sign in with your email. Use "Forgot Password" if needed.
	<br>
	• To find your case, go to "All Cases". (<a 
		href="[DYNAMIC_CASE_URL]" 
		target="_blank" 
		rel="noopener" 
		style="
			color: #2196F3; 
			font-weight: bold; 
			text-decoration: underline;
	">[Case Number]</a>)
	<br>
	• On your first login, you must also:<br>
	&nbsp;• Accept the GDPR agreement > Complete your profile.
[/code]
```