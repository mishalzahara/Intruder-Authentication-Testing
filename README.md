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

*(Insert attack results screenshot here)*
https://photos.google.com/documents/ChhTY3JlZW5zaG90cyAmIHJlY29yZGluZ3MiCRIHCgWyAQIYDijR5rWh6DM%3D/photo/AF1QipNtLhNL21dtYFXggTSW4B-cUhxaSmHhDpMlkouu
https://photos.google.com/documents/ChhTY3JlZW5zaG90cyAmIHJlY29yZGluZ3MiCRIHCgWyAQIYDijR5rWh6DM%3D/photo/AF1QipNbyFrG2jUlPtGgRVy2eEHE4qBv_nCFZC_Iuuo-


---

## Screenshots

### Intruder Configuration

Insert Screenshot:
`intruder-configuration.png`

Description:
Shows the request loaded into Intruder, payload position selection, attack type configuration, and payload list setup.

---

### Attack Results

Insert Screenshot:
`intruder-results.png`

Description:
Displays generated requests, status codes, response lengths, and response metrics collected during testing.

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
