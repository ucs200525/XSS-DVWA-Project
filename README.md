XSS-DVWA-Project Project Title Cross-Site Scripting (XSS) Attacks on DVWA

Description

This project showcases three types of XSS attacks—Reflected, Stored, and DOM-Based—using the Damn Vulnerable Web Application (DVWA) within a Dockerized environment. It also provides detailed notes on mitigation techniques for preventing XSS vulnerabilities in real-world applications.

---

  Setup Instructions

 1. Install Docker

If Docker is not already installed, download and install it from:
[https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

 2. Run DVWA Container

Use the command below to launch DVWA locally:

```bash
docker run -d -p 80:80 vulnerables/web-dvwa
```

 3. Access DVWA in Browser

Navigate to:
[http://localhost/setup.php](http://localhost/setup.php)

Steps:

* Click on "Create / Reset Database"
* Log in with the following credentials:

  * Username: `admin`
  * Password: `password`

 4. Set DVWA Security Level to "Low"

Navigate to:
DVWA Security → Security Level → Low → Submit

-

  Attack Overviews

 🔹 Reflected XSS

* The malicious script is reflected off a web server and executed immediately.
* Commonly delivered via a URL or form submission.
* Files: `Reflected-XSS/`

 🔹 Stored XSS

* The script is stored in the web application's database and executed when another user views the stored content.
* Most dangerous type of XSS.
* Files: `Stored-XSS/`

 🔹 DOM-Based XSS

* The vulnerability is in the client-side code (JavaScript), where the input is read from the DOM and executed.
* No request is sent to the server.
* Files: `DOM-Based-XSS/`

Each of the above folders contains:

* The XSS payload or attack script
* Screenshot proof of successful execution
* README with steps to replicate

---

  Mitigation Techniques

Folder: `Mitigation-Techniques/`
The documentation includes modern prevention strategies such as:

* Input validation and sanitization
* Output encoding (especially for HTML, JS, and URL contexts)
* Setting appropriate Content Security Policy (CSP) headers
* Enabling HttpOnly, Secure, and SameSite flags on cookies
* Using secure web frameworks like React, Angular, or Vue
* Avoiding `innerHTML`, `document.write`, and other unsafe APIs



