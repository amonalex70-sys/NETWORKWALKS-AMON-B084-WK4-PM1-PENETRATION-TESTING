
<div align="center">

# Web Application Penetration Testing
Conducting a black-box penetration test and vulnerability assessment to identify and evaluate security weaknesses in a web application.

<p align="center">
  <img src="https://img.shields.io/badge/Project-Penetration%20Testing-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Assessment-Black--Box-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Focus-Web%20Security-C00000?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Platform-Kali%20Linux-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Tool-PenTools-404040?style=flat-square&labelColor=C00000" />  
  <img src="https://img.shields.io/badge/Testing-Web%20Application-404040?style=flat-square&labelColor=0070C0" />
  <img src="https://img.shields.io/badge/Platform-GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Program-NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Week-04-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Practice-Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Mentor-Waqas%20Karim%20(CCIE)-C00000?style=flat-square" />
</p>

</div>

## 🛡️ Penetration Testing Project Overview

This project documents a **black-box penetration test and vulnerability assessment** of a web application to identify, analyse, and evaluate potential security weaknesses within an authorized testing environment.

The assessment follows a structured five-phase penetration-testing methodology, covering reconnaissance and footprinting, vulnerability assessment and scanning, gaining and maintaining access, covering tracks, and documentation. Each phase involves practical security testing, evidence collection, and analysis to evaluate the target's security posture.

The project aims to demonstrate the practical application of penetration-testing techniques, identify potential security risks, assess their impact, and provide appropriate remediation recommendations to improve the overall security of the target environment.

## 🎯 Penetration Testing Objectives

The primary objectives of this project are to:

- Perform reconnaissance and identify potential attack surfaces.
- Identify and assess security vulnerabilities within the target environment.
- Evaluate the effectiveness of existing security controls.
- Validate identified vulnerabilities through authorized security testing.
- Assess potential security risks and their impact.
- Document findings and provide appropriate remediation recommendations.

  
## 🛡️ Penetration Testing Purpose and Security Scope

This project provides a structured approach to conducting a **black-box penetration test and vulnerability assessment** in an authorized environment.

It supports hands-on security testing in the following areas:

- Reconnaissance and information gathering
- Network scanning and service enumeration
- Vulnerability identification and assessment
- Web application security testing
- Authorized exploitation and access validation
- Security analysis, evidence collection, and reporting

**⚠️ Security Notice:** All testing must be conducted within the explicitly authorized scope. Unauthorized access, denial-of-service attacks, social engineering, and testing outside the agreed scope are prohibited.

## ⚙️ Penetration Testing Environment Specifications

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Kali Linux 2026.3 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Testing Platform | Kali Linux |
| 🐉 Security Distribution | Kali Linux 2026.3 |
| 🔍 Assessment Type | Black-box Penetration Testing |
| 🌐 Target Domain | medirozahospital.com |
| 🛠️ Primary Toolset | PenTools |
| 🎯 Assessment Focus | Web Application Security |


## Step 1: Information Gathering (Reconnaissance and Footprinting)

**Domain Information Lookup**

Identify the target domain's IP address and retrieve basic DNS information to understand how the domain resolves across the internet.

```bash
nslookup medirozahospital.com
```
| Information | Finding |
|---|---|
| DNS Server | 8.8.8.8 |
| Target Domain | medirozahospital.com |
| Resolved IP | `199.188.201.16` |
| Local DNS (10.0.0.1) | Request timed out |

**Domain Registration Information**

Retrieve publicly available domain registration details, including registrar information, registration dates, and nameserver records.

```bash
whois medirozahospital.com
```

**Web Technology Fingerprinting**

Identify publicly detectable technologies and application components, including web server details, frameworks, scripts, and HTTP headers.

```bash
whatweb medirozahospital.com
```

<img width="1366" height="657" alt="Whateweb" src="https://github.com/user-attachments/assets/7a2f8d97-fdc3-4d55-afc1-9cc0d4d0e953" />

**HTTP Response and Header Analysis**

Examine the HTTP response, status code, and response headers to understand how the web server handles incoming requests and communicates with clients.

```bash
curl -i https://medirozahospital.com
```


**Web Application Firewall Detection**

Determine whether the target is protected by a detectable Web Application Firewall (WAF) and identify its provider, if possible.

```bash
wafw00f https://medirozahospital.com
```
<img width="628" height="394" alt="WAF_Pic" src="https://github.com/user-attachments/assets/6af76ee3-1ae0-417f-87cf-0c5060b9d28e" />

**DNS Reconnaissance**

Gather publicly available DNS records and identify associated domain infrastructure, including discovered subdomains and DNS configurations.

```bash
dnsrecon -d medirozahospital.com
```

## Step 2: Scanning 

Scanning involves examining the target environment to identify reachable hosts, exposed network ports, running services, and potential security weaknesses. This phase helps map the target's externally visible attack surface and provides information for further security assessment.

### Host Discovery

Determine whether the authorized target host is reachable over the network.

```bash
ping 199.188.201.16
```

### Port Scanning

Identify open, closed, and filtered ports to understand which network services may be exposed.

### Service and Version Detection

Identify services running on discovered open ports and determine their reported software versions.

### Vulnerability Assessment

Assess identified services for potential known security weaknesses using non-intrusive checks within the authorized testing scope.

