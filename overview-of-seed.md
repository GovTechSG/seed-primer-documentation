# Overview of SEED

SEED is the Singapore Government's implementation of Identity and Access Management (IAM) and zero trust framework to protect against unauthorised access to the Government's engineering resources, such as Government on Commercial Cloud (GCC) and the Singapore Tech Stack (SGTS).

Zero Trust replaces traditional Virtual Private Network (VPN) connections and network-based security policies with a standardised central identity provider. It offers enforcement of access policies allowing only authorised users to use devices compliant with device postures.

## Audience

- Vendors
- Public officers

| User| Description | <div style="width:210px">Examples</div> |
|----| ------------- |:-------------:|
| **Vendor** | Users whose organisational email address belong to any of the following email domains:<br>- dsta.gov.sg<br>- dsta-wog.gov.sg<br>- mindef.gov.sg<br>- defence.gov.sg<br>- gebiz.gov.sg<br>- sps.gov.sg<br>**Note**: Email domain is the part of an email address that comes after the “@” symbol. For example, if your email address is john_doe@sps.gov.sg, then **sps.gov.sg** is your email domain.<br><br>Users who have a vendor email address as their organisational email address. | - john_doe@dsta.gov.sg<br>- john_doe@gebiz.gov.sgz<br><br><br><br><br><br><br><br>- john_doe@ncs.com.sg<br>- john_doe@accenture.com.sg  |
| **Public officer** | Users whose organisational email address has a **.gov.sg** in it.<br><br>**Note**: Users who have a **.gov.sg** but also has a ***_from*** in their email address are **NOT** public officers. | - john_doe@cpf.gov.sg<br>- john_doe@hdb.gov.sg |





[Vendor](#vendor) and [public officer](#public-officer) who needs to access SGTS resources and GCC resources from an Internet Device.

### Vendor

- Users whose organisational email address belongs to any of the following email domains:
    - dsta.gov.sg
    - dsta-wog.gov.sg
    - mindef.gov.sg
    - defence.gov.sg
    - gebiz.gov.sg
    - sps.gov.sg

- Users who have a vendor email address as their organisational email address. For example:
    - john_doe@ncs.com.sg 
    - john_doe@accenture.com.sg 

?> Email domain is the part of an email address that comes after the “@” symbol. For example, if your email address is john_doe@sps.gov.sg, then ```sps.gov.sg``` is your email domain.      

### Public officer    

Users whose organisational email address has a **.gov.sg** in it.
For example:

<li>john_doe
<span>@</span>

cpf.gov.sg

- john_doe

<span>@</span>

hdb.gov.sg


?> Users who have a .gov.sg but has a ```_from``` in their email address are NOT public officers.

<!--
## Identify your user type (Eunice either this goes or the above explanation)

Refer to this table to know what type of user you are for the SEED platform.

|<div style="width:100px"> User</div>| <div style="width:140px">organisational email address</div>   | email domain 
| --- |------------- |:-------------:| 
|Vendor| Does not have a **gov.sg** in it.| belongs to<br>- dsta.gov.sg<br>- dsta-wog.gov.sg<br>- mindef.gov.sg<br>- defence.gov.sg<br>- gebiz.gov.sg<br>- sps.gov.sg |
|Public officer| has a **gov.sg** in it. | does not belong to the domains mentioned for vendors. | -->

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

