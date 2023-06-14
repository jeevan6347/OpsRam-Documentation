---
title: Patch Compliance
linkTitle: Patch Compliance
weight: 180
type: documentation
showRelated: false
related:
- patch-management-2.0
---

## Overview
Compliance is a metric that provides the number of uninstalled patches on a device. This refers to the number of resources that have been effectively patched or remediated against security threats. The distribution and deployment of patches accomplish nothing if your devices are not compliant. 

Automated patch management makes the process of patch compliance more accessible for organizations of any size. Automated patching solutions make it possible for users to patch across all devices regardless of the operating system, location, or third-party application from a single interface.

OpsRamp Patch Management can help your organization to meet regulatory compliance requirements by detecting and remediating non-compliant endpoints using an automated patch management system, assisting with regular software upgrades, establishing system health detection policy, and recognizing patching regulatory standards, and providing visibility over all endpoints through robust reporting features.

Following are reasons why compliance with patch management is so important:
- Enhance Security
- Boost Efficiency
- Enable Remote Working
- Prevent Reputation loss

## Create New Patch Compliance at Client Level
To create new patch compliance at client level, follow the below steps:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then **Compliance**.
5. Click **+ ADD** to create a new patch configuration.

Let's get started on creating a new patch compliance. You must fill out the necessary information on the following three pages:
- Resource Selection
- Patch Selection
- Schedule

### Resource Selection
On this page, we will choose resources based on the requirements.
1. In the **Compliance Name** field, give a name to the patch compliance.
2. Select the Resource group from the drop-down list.
3. Select the Operating system: **Windows/Linux**
2. Choose resources from the list. There are two options for doing so.
   - **Dynamic**: Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the Compliance configurations automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing Compliance configurations.
   - **Select Resources**: This is a manual process for searching and selecting resources by defining Resource attributes in a simple search query. The selected resources list would not be updated with newly onboarded devices if the Compliance configuration is saved with this option. Users must manually update the list for any onboarding or decommission of the devices on the platform.
   {{< alert title="Note" >}}
If you select multiple devices from the option **Select Resources**, in this case you cannot select more than 100 records at once; if you do, it show an error message "**Resource Ids should not be greater than 100**".
{{< /alert >}}
3. To proceed to the patch selection page, click **Next**.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/compliance-resource3.png" 
width="1200"
alt="patch management" >}} 

### Patch Selection
1. In the **Patch Selection** page, select the patches to be configured by using any of the options.
   - **Dynamic Patches**: You can have the Patches selected for the installation Dynamically using the filter criteria. With the next Missing Patch Scan job execution, if there are new patches found as per the filter criteria, those patches would be automatically included for installation under the respective configuration.
   - **Select Patches**: You can select the patched manually from the list or using the Filter criteria and then click **Apply**.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config7.png" 
width="1200"
height="600"
alt="patch management" >}} 
2. Once the patch selection process is completed, click **Next** to proceed to the schedule page.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/compliance-filter3.png" 
width="600"
alt="patch management" >}} 

{{< alert title="Note" >}}
If you select multiple patches from the option **Select Patches**, in this case you cannot select more than 100 records at once; if you do, it shows an error message "**Selection should not exceed more than 100 patches**".
{{< /alert >}}

### Schedule
After selecting the resource and patches, you must now define a schedule to run the compliance at the desired time.
1. On the **Schedule** section, you could specify when this patch activity should be performed:
   - Run On Demand: Select this option, if you want to apply the patch updates right away.
   - One Time: Select this option, if you want to apply the patch updates once a time.
   - Daily: Select this option, if you want to apply the patch updates on daily. You can configure this option by choosing: Every Weekday (Mon-Friday) or Everydays.
   - Weekly: Select this option, if you want to apply the patch updates on weekly wise. Configure weekly schedule by selecting: Time preference, Starting date, and Days.
   - Monthly: Select this option if you only want to apply patch updates on a monthly basis. Configure this by selecting:  Time preference, Starting date, and number of days in a month.

2. **Resource Time Zone**: You can select a specific time zone to patch all the resources in the patch compliance. When you select a time zone, it ignores the different local time zones of resources and instead uses the time zone specified in the patch compliance.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/time-zone1.png" 
width="300"
alt="" >}} 

4. **Approval Type**: If you want automatic approval, enable the **Approval Type** option. If it is not enabled, it means you have chosen the manual type approval.
8. Click **Finish** after you configured the scheduled page.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/complienec-finished.png" 
width="600"
alt="patch management" >}} 

## Create New Patch Compliance at Partner Level
OpsRamp categorizes any device as Compliant, if there are zero missing patches to be installed for a given Compliance configuration. If the missing patches in the Compliance criteria is greater than zero, the Device would be displayed as Non-Compliant.

To create new patch compliance at partner level, follow the below steps:
1. Login to OpsRamp Portal.
2. Select **All Clients**.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then **Compliance**.
5. Click **+ ADD** to create a new patch configuration.

Let's get started on creating a new patch compliance. You must fill out the necessary information on the following three pages:
- Resource Selection
- Patch Selection
- Schedule

### Resource Selection
On this page, we will choose resources based on the requirements.
1. To select a client, choose from **All Clients** or **Select Clients**.
2. In the **Compliance Name** field, give a name to the patch compliance.
3. Select the Operating system: **Windows/Linux**
4. Find the resources from the list using the **+ QUERY** button.<br>
   Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the configurations automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing installation configurations.
5. To proceed to the patch selection page, click **Next**.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/complience-partner-level1.png" 
width="1200"
alt="patch management" >}} 

{{< alert title="Note" >}}
The next two steps for Patch Compliance at the Partner level (**Patch Selection** and **Scheduling**) are the same as the described above for Patch Compliance at the Client level. Follow the same steps to complete the configuration at Partner level.
{{< /alert >}}

The following table summarizes the difference between Client Level and Partner Level functionality.

<table class="table">
 <thead class="thead-dark">
     <tr>
         <th width="30%" style="border:none !important; "></th>
         <th width="30%" style="border:none !important; ">Functionality</th>
         <th width="20%" style="border:none !important; ">Client Level</th>
         <th width="20%" style="border:none !important; ">Partner Level</th>
     </tr>
 </thead>
 <tbody>
<tr>
<td rowspan="6"><b>Resource Selection</b></td>
</tr>
<tr>
<td>Client Selection</td>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td>Windows OS Selection</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td>Linux OS Selection</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td>Dynamic Resources</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td>Static Resources</td>
<td>&check;
 <br/>
</td>
<td>&cross;
 <br/>
</td>
</tr>
<tr>
<td rowspan="5"><b>Patch Selection</b></td>
</tr>
<tr>
<td>Manual Approval Type</td>
<td>&check;</td>
<td>&check;<br/>
</tr>
<tr>
<td>Automatic Approval Type</td>
<td>&check;</td>
<td>&check;<br/>
</tr>
<tr>
<td>Dynamic Patches</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td>Select Patches</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td rowspan="3"><b>Schedule</b></td>
</tr>
<tr>
<td>Schedule Type</td>
<td> &check; </td>
<td>&check;<br/>
</tr>
<tr>
<td>Approval Type</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
</tbody>
</table>

### View List of Patch Compliance
View the list of configured patch compliance under **Patch Management 2.0 > Compliance**. You can choose one or more patches and take action against them.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/compliance-view2.png" 
width="1200"
alt="patch management" >}} 

The following table describes the various attributes and actions displayed on the **Compliance** page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Attributes</th>
         <th width="50%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Name</td>
  <td>The name of the patch compliance.</td>
 </tr>
 <tr>
  <td>OS Type</td>
  <td>Type operating system selected during the configuration; Windows/Linux.</td>
 </tr>
  <tr>
  <td>Resources</td>
  <td>The number of resources chosen when scheduling a compliance job.</td>
 </tr>
   <tr>
  <td>Patches</td>
  <td>Number patches selected for the particular compliance.</td>
 </tr>
   <tr>
  <td>Resource Group</td>
  <td>Selected resource group for the specific patch compliance. </td>
 </tr>
  <tr>
  <td>Search button</td>
  <td>Use the search field to find jobs.</td>
 </tr>
  <tr>
  <td>Approve</td>
  <td>Use this option to approve the patches.</td>
 </tr>
  <tr>
  <td>Edit</td>
  <td>Use the edit option to change the current job setup.</td>
 </tr>
  <tr>
  <td>Run Now</td>
  <td>Run the patch job on selected devices and resource groups.</td>
 </tr>
  <tr>
  <td>Remove</td>
  <td>Use this option to remove tasks from the list if they are not relevant.</td>
 </tr>
</tbody>
</table>

To see the configuration of the created compliance such as: Properties, Resources, Patches, and logs, click on the compliance jobs listed here.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/compliance-config1.png" 
width="400"
alt="patch management" >}} 