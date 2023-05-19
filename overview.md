# SEED Primer - Quick start guide

This document gives you a high level introduction of SEED and on the following areas:

 
## SEED Overview

<summary style="font-size:20px;font-weight:bold">SEED Overview</summary>
<img align="right" width="390" height="270" src="images/seed-functionalities.png">

SEED is the Singapore Government's implementation of Identity and Access Management (IAM) and zero trust framework to protect against unauthorised access to the Government's engineering resources, such as Government on Commercial Cloud (GCC) and the Singapore Tech Stack(SGTS).

Zero Trust replaces traditional Virtual Private Network (VPN) connections and network-based security policies with a standardised central identity provider. It offers enforcement of access policies allowing only authorised users to use devices compliant with device postures.

## Why do we need SEED?

![why-do-we-need-seed](images/why-do-we-need-seed.png)

- Detects and provides remediation steps for known malware.
- Detects if the endpoint meets the required security hardening baseline according to the corresponding Center of Internet Security (CIS) benchmark for the installed endpoint operating system.
- Detects if the endpoint’s operating system version and security patches are up-to-date.
- Prevents accessing the resources of GCC and the SGTS services if the above requirements are not satisfied.

## How does SEED work?

SEED comprises of three components:

- TechPass
- Cloudflare
- Development Environment Endpoint Posture(DEEP)

![how-does-seed-work](images/how-does-seed-work.png)

<!-- tabs:start -->

### **TechPass**

- This is the Identity Access Management(IAM) and Single Sign-On(SSO) solution for accessing SGTS and GCC services.

- TechPass is an IAM solution that is equipped with Single Sign-On(SSO). It leverages on [Azure Active Directory](https://azure.microsoft.com/en-us/services/active-directory/), which is an enterprise identity service from Microsoft.

- It complies with Government Instruction Manual ICT&SS Management (also known as [IM8](https://www.developer.tech.gov.sg/guidelines/standards-and-best-practices/instruction-manual-for-ict-ss-management.html)). It utilises popular open standards [OAuth 2.0](https://oauth.net/2/), [OpenID Connect](https://openid.net/connect/), and [Security Assertion Markup Language 2.0](http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0.html) for authentication and authorisation processes.

### **Cloudflare**

This is the security platform that enforces Zero Trust network access allowing faster and safer connections to the Internet and applications. This comprises of the following:

- **Cloudflare WARP**: Replaces the traditional VPN clients.

- **Cloudflare Gateway**: Blocks and protects from malicious content.

- **Cloudflare Access**: Evaluates every request for user identity and device context.

### **DEEP**

This is the Device management layer of SEED. It establishes a robust security baseline automatically​ and prevents insecure or compromised devices from accessing engineering resources.​ DEEP manages the following:

- **Microsoft Intune**: Provides device and application management including remote application deployment and selective device wipe.

- **Microsoft Defender Advanced Threat Prevention**: Enterprise class vulnerability management, threat detection and response security solution.

- **Tanium**: Works with Cloudflare to ensure posture-based conditional access to the endpoint assets.

<!-- tabs:end -->

## What can SEED do on my device?

|SEED can do the following on your device|SEED cannot do the following on your device|
|---|---|
|- View the model number, serial number and operating system of the device.<br>- View the names of the applications you have installed.<br>- Identify your device by name.<br>- Reset lost or stolen device to factory setting upon required consent and approval from device owner and manager-in-charge, respectively.|- Access your emails, contacts and calendar.<br>- Access your documents.|








