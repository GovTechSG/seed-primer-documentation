# SEED Primer - Quick start guide

This document gives you a high level overview of how to
onboard your device to SEED. This document contains:

<details open>
<summary style="font-size:20px;font-weight:bold">Introduction to SEED</summary>

SEED is the Singapore Government's implementation of Identity and Access Management (IAM) and zero trust framework to protect against unauthorised access to the Government's engineering resources, such as Government on Commercial Cloud (GCC) and the Singapore Tech Stack (SGTS).

Zero Trust replaces traditional Virtual Private Network (VPN) connections and network-based security policies with a standardised central identity provider. It offers enforcement of access policies allowing only authorised users to use devices compliant with device postures.

</details>

<details open>
<summary style="font-size:20px;font-weight:bold">SEED features</summary>

- Detects and provides remediation steps for known malware.
- Detects if the endpoint meets the required security hardening baseline according to the corresponding Center of Internet Security (CIS) benchmark for the installed endpoint operating system.
- Detects if the endpoint’s operating system version and security patches are up-to-date.
- Prevents accessing the resources of GCC and the SGTS services if the above requirements are not satisfied.

</details>

<details open>
<summary style="font-size:20px;font-weight:bold">How does SEED work?</summary>

SEED comprises of three components:

- TechPass
- Cloudflare
- Development Environment Endpoint Posture(DEEP)

<!-- tabs:start -->

### **TechPass**

This is the Identity Access Management(IAM) and Single Sign-On(SSO) solution for accessing SGTS and GCC services.

### **Cloudflare**

The security platform that enforces Zero Trust network access allowing faster and safer connections to the Internet and applications. This comprises of the following:<br>- **Cloudflare WARP**: Replaces the traditional VPN clients.<br>- **Cloudflare Gateway**: Blocks and protects from malicious content.<br>- **Cloudflare Access**: Evaluates every request for user identity and device context.

### **DEEP**

Device management layer of SEED. It establishes a robust security baseline automatically​ and prevents insecure or compromised devices from accessing engineering resources.​ DEEP manages the following:<br>- **Microsoft Intune**: Provides device and application management including remote application deployment and selective device wipe.<br>- **Microsoft Defender Advanced Threat Prevention**: Enterprise class vulnerability management, threat detection and response security solution.<br>- **Tanium**: Works with Cloudflare to ensure posture-based conditional access to the endpoint assets.

<!-- tabs:end -->

</details>




