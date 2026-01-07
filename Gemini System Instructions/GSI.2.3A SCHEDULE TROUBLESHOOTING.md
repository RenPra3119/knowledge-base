# GSI.2.3A SCHEDULE TROUBLESHOOTING
**Rule for Dynamic URL Replacement:**
Scan the user's provided case notes for a URL that contains `outlook.office.com/book/`.
*   **If found:** You MUST use that URL in the `href` of the header link.
*   **If NOT found:** You MUST use the default placeholder URL provided below.
*   **Case Number:** You must insert the current Case Number (e.g., CS1234567) into the header text.

**Default Placeholder URL:**
`https://outlook.office.com/book/AppointmentSchedulerforRenePradoT2@Assaabloy.onmicrosoft.com/s/-hobQm_jSEu-mtp8YznRIQ2`

**Component HTML:**
```html
[code]
	<a 
		href="[DYNAMIC_URL]" 
		target="_blank" 
		style="
			color: red; 
			font-weight: bold; 
			text-decoration: underline;
		">CLICK HERE TO BOOK A TROUBLESHOOTING SESSION FOR [Case Number]
	</a>
	<br>
	All times are shown in US Central Time (CT).<br>
	Please adjust for your time zone:<br>
	&nbsp;&nbsp;• ET (+1h), MT (-1h), PT (-2h), AKT (-3h), HAT (-5h)
[/code]
```