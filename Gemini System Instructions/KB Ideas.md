
### KB Article: Advanced Styling & Visual Containers
**Title:** *Creating Visual Alerts and Containers in Case Notes*
**Description:** *How to use CSS styles to create colored warning boxes and organized data containers.*

| **Introduction**
| Plain text often gets ignored. By using the `<div>` tag with inline CSS styles, you can create visual containers to highlight errors, warnings, or specific datasets (like IP addresses).

| **The "Warning" Box (Red)**
| Use this for critical errors or safety warnings.
|
| *Syntax:*
| ```html
| [code]
| <div style="border: 2px solid red; background-color: #ffe6e6; padding: 10px; border-radius: 5px; color: darkred;">
|     <b>CRITICAL WARNING:</b> The server is overheating.
| </div>
| [/code]
| ```

| **The "Info" Box (Blue)**
| Use this for system information or IP configs.
|
| *Syntax:*
| ```html
| [code]
| <div style="border: 1px solid #003366; background-color: #f0f8ff; padding: 10px; border-radius: 5px;">
|     <b>System Info:</b><br>
|     IP: 192.168.1.50<br>
|     Version: 1.30.2
| </div>
| [/code]
| ```

| **Key CSS Attributes Explained**
| * `border`: Sets the thickness and color of the outline.
| * `background-color`: Sets the fill color of the box.
| * `padding`: Adds space between the text and the border (breathing room).
| * `border-radius`: Rounds the corners of the box.

---

### KB Article: Hyperlinks & Action Buttons
**Title:** *Embedding Links and Creating Action Buttons*
**Description:** *How to insert clean hyperlinks and style them as buttons for better user experience.*

| **Introduction**
| Long URLs (like Sharepoint or Booking links) look messy in case notes. Using the `<a>` (Anchor) tag allows you to mask the URL with text or style it to look like a clickable button.

| **1. The Standard Text Link**
| Always use `target="_blank"` to ensure the link opens in a new tab, so you don't lose your ServiceNow page.
|
| *Syntax:*
| `[code]<a href="https://www.google.com" target="_blank">Click Here for Google</a>[/code]`

| **2. The "Call to Action" Button**
| You can style a link to look like a button using CSS.
|
| *Syntax:*
| ```html
| [code]
| <a href="https://outlook.office.com/book/..." target="_blank" 
|    style="background-color: #003366; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; font-weight: bold;">
|    📅 Schedule Appointment
| </a>
| [/code]
| ```

| **Best Practices**
| *   **Contrast:** Ensure the text color contrasts well with the background color (e.g., White text on Dark Blue background).
| *   **Labels:** Keep the button text short and action-oriented (e.g., "Download," "Schedule," "View Log").

---

### KB Article: Embedding External Content (Iframes)
**Title:** *Embedding External Tools and Documents using Iframes*
**Description:** *Advanced technique to display external web tools or documents directly within the ServiceNow Activity Stream.*

| **Introduction**
| The `<iframe>` tag allows you to display a "window" to another website inside a ticket. This is useful for scheduling tools, hosted diagnostic scripts, or cheat sheets.

| **Restrictions (Read First)**
| 1.  **HTTPS Only:** The external site *must* be secure (https://).
| 2.  **Security Headers:** Many sites (Google, Facebook) block embedding via `X-Frame-Options`. You can only embed sites that allow it (e.g., GitHub Pages, Microsoft Bookings).

| **The Embed Code Block**
| This code creates a framed window. We include a "Backup Button" in case the browser security blocks the window.
|
| *Syntax:*
| ```html
| [code]
| <div style="border: 1px solid #ccc; padding: 10px;">
|     <h3>Tool Window</h3>
|     <!-- The Iframe -->
|     <iframe src="https://renpra3119.github.io/service-now-helpers/" width="100%" height="600" style="border:none;"></iframe>
|     
|     <!-- The Backup Button -->
|     <br><br>
|     <div style="text-align:center;">
|         <span style="font-size:10px; color:red;">Window blank? Click below:</span><br>
|         <a href="https://renpra3119.github.io/service-now-helpers/" target="_blank" style="background-color: #333; color: white; padding: 5px 10px; text-decoration: none; border-radius: 3px;">Open Tool in New Tab</a>
|     </div>
| </div>
| [/code]
| ```

| **Verified Working Sources**
| *   **GitHub Pages:** Excellent for hosting custom HTML tools or guides.
| *   **Microsoft Bookings:** Public scheduling pages (`outlook.office.com/book/...`).
| *   **Google Drive (Preview Mode):** Use `.../preview` at the end of the URL for PDFs.