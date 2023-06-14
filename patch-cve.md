---
title: Patch CVE
linkTitle: Patch CVE
weight: 194
type: documentation
showRelated: false
related:
- patch-management-2.0
---

CVE stands for “**Common Vulnerabilities and Exposures**”. The CVE number is a unique identifier used by vendors. By using a common identifier, cybersecurity professionals can more easily communicate about vulnerabilities and exposures, which makes it easier to coordinate efforts to fix or mitigate them. Each CVE entry contains a description of the vulnerability or exposure, as well as information about how to mitigate or fix it.

OpsRamp uses CVE in the Patch Management process to identify which vulnerabilities and exposures require patching.

How to get the CVE information and uses of these information into OpsRamp patch management process:
   - Each time we run an “**asset info scan**” on a device to collect information about the installed software. This software's information includes the CVEs number, which is published by the vendors. <br>
   OpsRamp uses the latest installed software information from Agent to detect if there are any CVEs published by the vendors. 
   - OpsRamp obtains CVE information from the **OVAL advisory** and the **NVD database**. 
   - Now, we only support detecting the CVEs information from **Ubuntu** and **RedHat** operating systems.

In the OpsRamp Patch Management 2.0, we have added **CVE Insights** page and **CVE Details** page.<br>
To view the CVE information, navigate to **Configuration Management > Patch Management 2.0** and then click the Menu bar icon.


{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-overview.png" 
alt="patch management" >}} 

## Prerequisite
- A "**asset info scan**" must be run on the resource on a regular basis.
- It will work starting with Agent version 16.0.0.


## View the CVE Insights Page
Follow the steps below to see the CVE Insights page:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon.
5. Click the **Insights** under the **CVE** tab.
6. Here you will see CVE Insights landing page.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-insight1.png" 
width="600"
alt="patch management" >}} 

By clicking on any of the displayed numbers above, it will provide you with detailed information. Here is an example of what you can expect when click on "Impacted Resources":

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/impacted-resources.png" 
width="300"
alt="patch management" >}} 

The following table describes the various widgets displayed on the Insights page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Widgets</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Resources</td>
  <td>See the total number of resources for the selected client.</td>
 </tr>
 <tr>
  <td>Impacted Resources</td>
  <td>Number of resources impacted for CVE out of of total resources.</td>
 </tr>
  <tr>
  <td>Severity By CVE</td>
  <td>Type of Severity impacted for each resources:<br>
  - Critical<br>
  - High<br>
  - Medium<br>
  - Low<br>
  - None</td>
 </tr>
  <tr>
  <td>By Operating System</td>
  <td>See the list of operating system impacted by CVE with Severity categories.</td>
 </tr>
</tbody>
</table>

## View the CVE Details Page
Follow the steps below to see the CVE Details page:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon.
5. Click the **Details** under the **CVE** tab.
6. Here you will see CVE Details listing page. You can view the CVE details by selecting the **CVE** or **RESOURCES** option.

**By using CVE option:**

The CVE option enables you to view the list of CVE id for the impacted devices.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-details-cve1.png" 
width="600"
alt="patch management" >}} 

By clicking on any of the displayed CVE IDs mentioned above, you will be provided with detailed information about the impacted resources. Here is an example of what you can expect:

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-details-info.png" 
width="300"
alt="patch management" >}} 

**By using RESOURCES option:**

The RESOURCES option enables you to view the list of devices with the number of CVE.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-details-resources1.png" 
width="600"
alt="patch management" >}} 

By clicking on any of the displayed Device Name above, you will be provided detailed information about the CVEs number for that specific device. Here is an example of what you can expect:

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/cve-details-resource-info.png" 
width="300"
alt="patch management" >}} 

The following table describes the various information displayed on the Details page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%"></th>
         <th width="45%">Name</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>BY CVE</td>
  <td>CVE ID</td>
  <td>It is a unique, alphanumeric identifier assigned by the CVE Program. Each identifier references a specific vulnerability.</td>
 </tr>
 <tr>
  <td> </td>
  <td>Severity</td>
  <td>It shows the effect of severity on the operating system.</td>
 </tr>
  <tr>
  <td> </td>
  <td>Description</td>
  <td>Detailed description mentioned for the CVE ID.</td>
 </tr>
  <tr>
  <td> </td>
  <td>Impacted OS</td>
  <td>Listed of impacted OS.</td>
 </tr>
 <tr>
 <td> </td>
  <td>Impacted Resources</td>
  <td>Show the number of resources impacted against each CVE.</td>
 </tr>
 <tr>
 <td>BY RESOURCES</td>
  <td>Device Name</td>
  <td>Name of the device.</td>
 </tr>
 <tr>
 <td> </td>
  <td>IP Address</td>
  <td>Show the IP Address of the devices.</td>
 </tr>
 <tr>
 <td> </td>
  <td>Operating System</td>
  <td>Show the operating System for the devices.</td>
 </tr>
 <tr>
 <td> </td>
  <td>CVE</td>
  <td>Show the number of Common Vulnerabilities and Exposures (CVE) against each device.</td>
 </tr>
</tbody>
</table>