# Overview of SEED

SEED is the Singapore Government's implementation of Identity and Access Management (IAM) and zero trust framework to protect against unauthorised access to the Government's engineering resources, such as Government on Commercial Cloud (GCC) and the Singapore Tech Stack (SGTS).

Zero Trust replaces traditional Virtual Private Network (VPN) connections and network-based security policies with a standardised central identity provider. It offers enforcement of access policies allowing only authorised users to use devices compliant with device postures.

## Audience

Vendor and public officer who needs to access SGTS resources and GCC resources from an Internet Device. 

**Vendors**: Users whose organisational email address(official email address) does not have a **.gov.sg** or belongs to following domains:

- dsta.gov.sg
- dsta-wog.gov.sg
- mindef.gov.sg
- defence.gov.sg
- gebiz.gov.sg
- sps.gov.sg

**Public officer**: Users whose organisational email address(official email address) has a **.gov.sg** and must not belong to following domains:

- dsta.gov.sg
- dsta-wog.gov.sg
- mindef.gov.sg
- defence.gov.sg
- gebiz.gov.sg
- sps.gov.sg


### Identify your user type (Eunice either this goes or the above explanation)

Refer to this table to know what type of user you are for the SEED platform.

|<div style="width:200px"> User</div>| <div style="width:290px">organisational email address</div>   | email domain |
| --- |------------- |:-------------:|
|Vendor| does not have a **gov.sg** in it.| belongs to<br>- dsta.gov.sg<br>- dsta-wog.gov.sg<br>- mindef.gov.sg<br>- defence.gov.sg<br>- gebiz.gov.sg<br>- sps.gov.sg |
|Public officer| has a **gov.sg** in it. | does not belong to the domains mentioned for vendors.    |

## Features of SEED

- Detects and provides remediation steps for known malware.
- Detects if the endpoint meets the required security hardening baseline according to the corresponding Center of Internet Security (CIS) benchmark for the installed endpoint operating system.
- Detects if the endpoint’s operating system version and security patches are up-to-date.
- Prevents accessing the resources of GCC and the SGTS services if the above requirements are not satisfied.

## How does SEED work?

SEED comprises of three components:

- **TechPass**: The Identity Access Management(IAM) and Single Sign-On(SSO) solution.

- **Cloudflare**: The security platform that enforces Zero Trust network access allowing faster and safer connections to the Internet and applications. This comprises of the following:
    - **Cloudflare WARP**: Replaces the traditional VPN clients.
    - **Cloudflare Gateway**: Blocks and protects from malicious content.
    - **Cloudflare Access**: Evaluates every request for user identity and device context.

 - **Development Environment Endpoint Posture (DEEP)**: Device management layer of SEED. It establishes a robust security baseline automatically​ and prevents insecure or compromised devices from accessing engineering resources.​ DEEP manages the following:
    - **Microsoft Intune**: Provides device and application management including remote application deployment and selective device wipe.
    - **Microsoft Defender Advanced Threat Prevention**: Enterprise class vulnerability management, threat detection and response security solution.
    - **Tanium**: Works with Cloudflare to ensure posture-based conditional access to the endpoint assets.

