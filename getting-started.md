# Getting started

This section provides general guidelines on how to get started with SEED onboarding. It offers essential steps and information to help you complete the onboarding process smoothly. 


```mermaid
%%{init: {'theme': 'default','themeVariables': { 'fontSize': '20px' }}}%%
graph LR
    A["<a href='https://docs.developer.tech.gov.sg/docs/seed-primer/getting-started?id=step-0-ensure-you-meet-the-required-prerequisites'>Step 0: Complete prerequisites</a>"]
    B["<a href='https://docs.developer.tech.gov.sg/docs/seed-primer/getting-started?id=step-1-identify-your-onboarding-persona'>Step 1: Identify onboarding persona</a>"]
    C["<a href='https://docs.developer.tech.gov.sg/docs/seed-primer/getting-started?id=step-2-onboard-device-to-seed'>Step 2: Onboard to SEED</a>"]
    D["<a href='https://docs.developer.tech.gov.sg/docs/seed-primer/post-onboarding-steps'>Step 3: Complete post onboarding steps</a>"]
    E["<a href='https://docs.developer.tech.gov.sg/docs/seed-primer/dashboard'>Step 4: Access SEED Dashboard</a>"]

    style A  stroke:#333, max-width: 1000px
    style B  stroke:#333, max-width: 1000px
    style C  stroke:#333, max-width: 1000px
    style D  stroke:#333, max-width: 1000px
    style E  stroke:#333, max-width: 1000px
    
    A --> B
    B --> C
    C --> D
    D --> E

```

## Guidelines for onboarding

![guidelines-to-onboard-your-device-to-seed](images/guidelines-to-onboard-your-device-to-seed.png)


## Step 0: Ensure you meet the required prerequisites

- You need an active <a href="https://docs.developer.tech.gov.sg/docs/techpass-user-guide/onboard-to-techpass">TechPass account</a>.
- Request SEED provisioning.
Internet Device running on one of the following operating systems:
    - Windows 10 and 11 Pro or Enterprise versions.
    - macOS 11 (macOS Big Sur), macOS 12 (macOS Monterey) and macOS 13 (Ventura) versions.
- Have administrator permissions on the device.
- Remove any existing software on your device such as MDM software, Tanium client or any other unified endpoint management and security platform.
- Ensure that System Integrity Protection(SIP) is enabled if you are onboarding a macOS device.
- Encrypt hard disk drive to protect the data at rest.
- If your organisation uses a firewall or other policies to restrict Internet traffic, you may need to make few changes to allow WARP to connect.

?> Refer to the [SEED user documentation](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/prerequisites-for-onboarding) to know how to ensure you meet the prerequisites.

## Step 1: Identify your onboarding persona

To determine if your onboarding persona is that of a **vendor** or a **public officer**, refer to your TechPass login ID. The onboarding persona is determined based on your login ID associated with TechPass.

| Onboarding Persona 	| Description 	| Example 	|
|---	|---	|---	|
| Vendor 	| If your TechPass login ID belongs to the domain ```techpass.gov.sg```, you need to onboard your Internet Device to SEED as a vendor. 	| john_doe@techpass.gov.sg 	|
| Public officer 	| If your TechPass login ID is the same as your organisational email address (WOG account), you need to onboard your Internet Device to SEED as a public officer. 	| john_doe@moe.gov.sg<br>john_doe_from.cognizant@tech.gov.sg 	|

## Step 2: Onboard device to SEED

The onboarding process consists of the following steps. 

?> For step-by-step instructions tailored to your specific onboarding persona, please refer to the [SEED Documentation](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/onboard-device/onboard-device-to-seed). It provides comprehensive guidance to assist you throughout the onboarding process.

1. Set up Microsoft Intune on the device. 

2. Ensure that your device is connected to the Internet so that Intune is able to install the required SEED components and configurations. 

    If you are onboarding as a vendor, all the necessary applications and device configurations will be provided when you set up Intune, provided your device is connected to the internet. 

3. If you are onboarding as a public officer, you need to register your Intune Device ID on the [TechPass portal](https://portal.techpass.gov.sg/secure/account/profile) from your non-SE GSIB device. This step ensures that the required applications and device configurations are installed on your device. 

?> **Note**<br>- If you are a SE GSIB device user, please submit a [support request](https://go.gov.sg/seed-techpass-support) to register your Intune Device ID. <br>- Ensure that the device you are onboarding remains connected to the internet until you receive the confirmation email indicating successful onboarding.<br>- Public officers who are undergoing the onboarding process can check their onboarding status on the TechPass portal.<br>- Please be aware that onboarding may fail due to various reasons. In such cases, we will provide the specific onboarding status and the necessary action required from you to resolve the issue. 

3. When your onboarding is successfully completed, a confirmation email will be sent to the email address associated to your TechPass account.

4. Verify that the required profiles have been installed on your device.



  







