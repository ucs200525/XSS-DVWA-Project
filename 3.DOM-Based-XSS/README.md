DOM-Based-XSS

🔹 Description:
This folder demonstrates a DOM-Based Cross-Site Scripting (XSS) attack using DVWA.

Steps followed

1. Launch DVWA in Docker and log in.
2. Set the DVWA Security Level to "Low".
3. Navigate to: "Vulnerabilities → XSS (DOM)"
4. Use a crafted URL in the browser to inject the script.

Attack Script:

```
http://localhost:8080/vulnerabilities/xss_d/?default=<script>alert('DOM XSS! ' + document.cookie)</script>
```

Screenshot:

* `screenshot-2.png` shows successful execution of the script in the browser.

Notes:

* DOM XSS occurs entirely in the browser and does not involve server response.
* The attack script is executed via URL manipulation and processed by client-side JavaScript.

Files:

* `test_url.txt`: Contains the attack URL used.
* `screenshot-2.png`: Proof of successful execution.

