Reflected-XSS

🔹 Description:
This folder demonstrates a Reflected Cross-Site Scripting (XSS) attack using DVWA.

Steps followed
1. Launch DVWA in Docker and log in.
2. Set the DVWA Security Level to "Low".
3. Navigate to: "Vulnerabilities → XSS (Reflected)"
4. Copy and paste the attack script into the input field.

```html
Attack Script:
<script>alert('Reflected XSS: Session Cookies => ' + document.cookie)</script>
```
Screenshot:
- `screenshot-2.png` shows successful execution of the script in the browser.

Notes:
- Reflected XSS occurs when user input is immediately reflected in the response.
- The attack executes as soon as the crafted URL or form is submitted.

Files:
- `attack_script.txt`: Contains the payload used.
- `screenshot-2.png`: Proof of successful execution.
