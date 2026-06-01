# Burp Suite Intruder Authentication Testing

## Overview

This project demonstrates the use of Burp Suite Professional's Intruder module to analyze authentication behavior within a controlled and authorized testing environment. The purpose of this assessment was to understand how web applications process authentication requests, handle multiple input values, and respond to varying login attempts.

The project involved intercepting a login request, configuring Intruder payload positions, executing automated requests, and analyzing the resulting server responses. By comparing response lengths, status codes, and server behavior, it is possible to identify patterns that may indicate different authentication outcomes.

---

## Objectives

* Understand Burp Suite Intruder functionality.
* Capture and modify HTTP authentication requests.
* Configure payload positions for automated testing.
* Analyze server responses based on different input values.
* Study authentication security mechanisms and response behavior.
* Gain practical experience with web application security testing.

---

## Tools Used

### Burp Suite Professional

Used for intercepting, modifying, and automating HTTP requests.

### Mozilla Firefox

Used as the testing browser configured with Burp Suite proxy settings.

### Test Environment

A controlled environment used solely for educational and authorized security testing.

---

## Project Workflow

### Step 1: Capturing the Authentication Request

The login request was intercepted using Burp Suite Proxy while attempting to authenticate through the target application's login page.

The captured request contained:

* HTTP Method
* Request Headers
* Authentication Parameters
* Session Information
* CSRF Protection Tokens

The request was then forwarded to Burp Suite Intruder for further analysis.

---

### Step 2: Configuring Intruder

After sending the request to Intruder, the relevant authentication parameter was selected as the payload position.

Burp Suite markers were placed around the parameter to indicate where payload values would be inserted during automated testing.

Attack Type Used:

**Sniper Attack**

The Sniper attack type was selected because it modifies one payload position at a time while keeping the remainder of the request unchanged.

---

### Step 3: Payload Configuration

A custom payload list was loaded into Intruder.

Each payload value was automatically inserted into the selected parameter position during request execution.

This allowed multiple authentication requests to be generated and analyzed efficiently.

---

### Step 4: Launching the Attack

After configuring payloads and attack settings, the Intruder attack was launched.

Burp Suite generated multiple requests using the supplied payload values and sent them sequentially to the application.

During execution, Burp Suite recorded:

* HTTP Status Codes
* Response Lengths
* Response Times
* Server Responses
* Error Messages

---

### Step 5: Analyzing Results

Once the attack completed, the Intruder results table was examined.

Several key metrics were compared:

#### Status Codes

Status codes were analyzed to determine whether the server handled requests consistently or produced different responses under specific conditions.

#### Response Length

Response lengths were compared to identify variations that might indicate different application behavior.

#### Response Timing

Response times were reviewed to determine whether certain payloads triggered additional processing.

#### Error Messages

Any unusual or unexpected responses were examined for potential indicators of authentication handling differences.

---

## Results

The testing process successfully demonstrated how Burp Suite Intruder can automate authentication-related request analysis.

Key observations included:

* Consistent request generation using Intruder.
* Automated payload insertion and execution.
* Measurable differences in response characteristics.
* Effective comparison of authentication responses.
* Improved understanding of web application request handling.

<img width="1903" height="1049" alt="1" src="https://github.com/user-attachments/assets/8b0d450f-f105-4bbc-8aba-7de3b5d874b2" />
<img width="702" height="872" alt="2" src="https://github.com/user-attachments/assets/0646c0d4-a3c1-4500-94fb-c75d23c1a5c6" />
<img width="1769" height="362" alt="3" src="https://github.com/user-attachments/assets/45598d6f-e1aa-4c0c-b002-f82bbfb10dbb" />
<img width="1888" height="968" alt="4" src="https://github.com/user-attachments/assets/eb084b42-d42a-4256-81d9-4544eb5835a4" />
<img width="1794" height="1026" alt="5" src="https://github.com/user-attachments/assets/27cdb463-97fc-421c-9a3a-7e64f931e6da" />
<img width="1538" height="460" alt="6" src="https://github.com/user-attachments/assets/1d1209ea-3005-4d75-b948-e8f4e6c5a368" />
<img width="1781" height="461" alt="7" src="https://github.com/user-attachments/assets/eb4412de-46d2-465a-8f6c-cbbf591288b9" />
<img width="1633" height="891" alt="8" src="https://github.com/user-attachments/assets/47514ca1-d6d3-413c-aa7a-11faba7d7525" />
<img width="1280" height="965" alt="IMG-20251013-WA0027" src="https://github.com/user-attachments/assets/e6831305-7bbf-4b6d-b497-44f48ad63876" />


---

## Skills Demonstrated

* Web Application Security Testing
* HTTP Request Analysis
* Burp Suite Professional
* Intruder Configuration
* Authentication Workflow Analysis
* Response Comparison Techniques
* Security Research Methodology

---

## Disclaimer

This project was conducted strictly within an authorized and controlled environment for educational and research purposes. All testing activities were performed responsibly and in accordance with ethical security testing practices.
