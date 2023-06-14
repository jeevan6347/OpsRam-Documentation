---
title: Patch Feed
linkTitle: Patch Feed
weight: 140
type: documentation
showRelated: false
related:
- patch-management-2.0
---

You can instantiate your Patch Feed, apply the custom ratings to Windows and Linux patches published by the OS vendor using APIs and patch devices against custom rated patches.

You can qualify the patches by providing the following attributes using API:
   - Patch rating (Whitelisted, Blacklisted)
   - CVE ID (Common Vulnerabilities and Exposures identifier)

## Available Patch Feed Channels for Windows and Linux
Agent deployed Windows servers can get the missing patches downloaded from

**Microsoft cloud through Windows Update Agent (WUA) API** or **Windows Update Service (WSUS) - Local Repository**

### Pre-Requisites: Windows
1. Microsoft Cloud through Windows Update Agent (WUA) API
   - Windows Server/Laptop/Desktop should have an OpsRamp Agent installed to perform the patch activities.
   - Windows Server should have outbound internet (Proxy or Direct) connectivity to download the patches from the vendor site.

2. Windows Update Service (WSUS) - Local Repository
   - Windows Server/Laptop/Desktop should have an OpsRamp Agent installed to perform patch activities.
   - WSUS Services should be enabled on the Windows Server/Laptop/Desktop to download the patches from the local repository.

Agent deployed Linux servers can get the missing patches downloaded from Linux Cloud Public Repository.

### Pre-Requisites: Linux
1. Linux Public Repos
   - Linux Server/Laptop/Desktop should have an OpsRamp Agent installed to perform the patch activities.
   - Linux Server should have outbound internet (Proxy or Direct) connectivity to download the patches from the vendor site.

## Installing and Managing the Cloud Patch Feed Integrations
**Windows patch feed** – Generated from Microsoft authoritative source to contain all the patch data released by Microsoft for different operating system versions.

**Linux patch feed** – Generated from Linux repositories to contain patch data from different distributions of Linux from all its authoritative sources.

You can install the patch feed for Windows from the Integrations page in the **Setup** tab.
1. Select a client from the **All Clients** list.
2. Go to **Setup > Integrations and Apps > + Add**.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/setup.png" 
width="600"
alt="Credential Mapping" >}} 

3. On the **Available Apps** section, click on All Categories and select **Patch** or click on the search option and type **Patch**.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/available-app2.png" 
width="600"
alt="Credential Mapping" >}} 

4. Click **ADD** and From PATCH FEED INTEGRATION, click **Install**.
5. From the Install Patch Feed Integration window, provide details for the following parameters:
   - Name: Unique name for the patch feed integration.
   - Upload Logo: You can browse to upload a logo of your organization.
   - Use Service Provider Feed: You can inherit Patch Qualifications and Available Patches details from your Service Provider.
6. Click **Install**.
7. From **PATCH FEED INTEGRATION**, the Authentication section in the API tab displays Authentication Type. The default Authentication Type is OAUTH2.
8. Click **Save**. The **Authentication** section displays Tenant Id, Key, and Secret. You can use the Key and Secret to generate the authentication token required for API.

Copy the patch feed UID. You can use the patch feed UID while rating the patches for the respective patch feed through API.
   - When the client user does not select the Use Partner Feed, the Qualifications section on the Patch Feed Integration page does not display the Patch Rating and corresponding count.
   - When the client user unselects the option Use Partner Feed, the ratings of the patches changes to Not Rated and auto-approval of patches reverts to the unapproved, and a new feed for the client is created.
   - Patch integration is displayed in My Integrations after installation.
   - The rated patches are listed as Whitelisted.

For more information on how to create a Patch Feed using API, click the {{< target_blank  href="https://develop.opsramp.com/docs/v2/patching" title="Patch Feed API" hover="Open the OpsRamp website in a new window.">}}.

## Enabling WSUS Settings on the Server
To have the Windows Servers enabled to download the Missing Patches through WSUS services and Group Policy assigned to the device, follow the below steps.

1. Select a **Client** from **All Clients** List.
2. Go to **Infrastructure > Resources > Servers**.
3. Search for the Resources \ Devices, Select and click on the gear symbol on the top right corner of the page. to disable or enable WSUS Settings.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/server.png" 
width="600"
alt="Credential Mapping" >}} 

Once WSUS settings is enabled on the OpsRamp cloud, the agent registry key value should be `1`, and these values should be created by the agent.<br> 
{{< code >}}
OpsRamp Internal Path: HKEY_LOCAL_MACHINE\\SOFTWARE\\OpsRamp\\Agent
Key: USE_WSUS
Value: 1
{{< /code >}}

Once the above settings are enabled, the agent will look for the following two registry keys, which should not be created by the agent. The customer-side administrator should take care of these registry key as part of the WSUS server configuration.<br>

1. The WSUS setting is enabled at the device level.<br>
{{< code toml >}}
Path: HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\Windows\\WindowsUpdate\\AU
key: UseWUServer
Value: 1
{{< /code >}}
   
2. If the WSUS setting is enabled at the device level, the agent will look for the following registry key to locate the WSUS server.<br>
{{< code toml >}}
Path: HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\Windows\\WindowsUpdate
Key: WUServer
Value: http://<your_wsus_server>:8530

Default port: 8530 or 8531
{{< /code >}}
   
## Patch Workflow Based on the Patch Feed

### Cloud Patch Feed
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cloud-feed1.png" 
width="600"
alt="Credential Mapping" >}} 

### Windows WSUS Patch Feed
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/wsus-feed1.png" 
width="600"
alt="Credential Mapping" >}} 

