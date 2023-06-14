---
title: Patch Overview Page
linkTitle: Patch Overview Page
weight: 130
type: documentation
showRelated: false
related:
- patch-management-2.0
---

The Overview Page of patch management provides a snapshot of the current overall Patch status in your Windows and Linux devices for the selected clients. Follow the below steps to access the Patch Overview page.

1. Login to OpsRamp Portal.
2. To see a client level overview, select a **client** from the **All Clients** list. To see a partner level overview, select **All Clients**.
3. Navigate to **Configuration Management > Patch Management 2.0**.

The Overview page contains few pre-built widgets to provide a status info about the configured Patching parameters of the agent installed devices. 

{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-overview6.png"
width="1200"
height="600"
alt="By Patch" >}}

You can get individual widget data through drill down links:
- Click on the **Resource** tile to view the data for unscanned resources.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-unscanned.png"
alt="By Patch" >}}
- Click on the **Scanned** tile to view the data for scanned resources.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-scanned.png"
alt="By Patch" >}}
- Click on the **Installed** tile to view the data for installed resources.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-installed-report.png"
alt="By Patch" >}}
- Click on the **Failed** tile to view the data for failed resources.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-failed-report.png"
alt="By Patch" >}}
- Click on the **Rebooted** tile to view the data for rebooted resources.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-rebooted-report.png"
alt="By Patch" >}}

{{< alert title="Note" >}}
We've added a new widget as <b>Client Overview</b> under the partner level overview page.
{{< /alert >}}

{{< alert title="Note" >}}
These are hard coded widgets under Patch Management 2.0 and Users would not have an option of re-arranging or editing the widgets on the overview page for now. Keep referring to the Patch Management 2.0 release notes for any enhancements developed on the Patch Overview Page.
{{< /alert >}}

### Widgets

Below is the list of pre-built widgets and description:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="35%">Widget</th>
         <th width="65%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Failed</td>
  <td>Number of patches failed to install on the Resources/Devices</td>
 </tr>
<tr>
  <td>Installed</td>
  <td>Number of Patches installed Successfully</td>
 </tr>
<tr>
  <td>Missing Critical & Security</td>
  <td>Number of Missing Critical and Security category patches across all devices as per the last Missing Scan Schedule for the selected Client</td>
 </tr>
<tr>
  <td>Non-Compliance</td>
  <td>Number of Non-Compliant Resources/Devices as per the defined compliance configuration<br>
 </tr>
<tr>
  <td>Patch Compliance Resource</td>
  <td>List of defined Compliance configuration under the selected client<br>
 </tr>
 <tr>
  <td>Patch Configurations</td>
  <td>Last and Next 24 Hrs. Patch installation configuration list under the selected client</td>
 </tr>
 <tr>
  <td>Patch Scan Schedule</td>
  <td>Last and Next 24 Hrs. Patch Scan Schedule Jobs list under the selected client</td>
 </tr>
 <tr>
  <td>Reboot Required</td>
  <td>Number of patches installed successfully and Resource/Device reboot is required</td>
  <td></td>
 </tr>
  <tr>
  <td>Scanned</td>
  <td>Number of Resources/Devices scanned as per the last missing patch scan schedule</td>
 </tr>
  <tr>
  <td>UnScanned</td>
  <td>Number of Resources\Devices which were not scanned for any missing patches by the agent</td>
 </tr>
</tbody>
</table>

Users can access the Patch Management Configurations by clicking on the Menu bar on the top left corner of the page as shown below. This Menu provides the list of Patch Capabilities of the platform.

Below are the list of Configurations available to setup under the Menu. You can find more details on each of these configurations in the following documentation of Patch Management.

{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/menu-bar4.png"
width="300"
alt="By Patch" >}}

### FAQs
1. **Can Users rename or re-order the widgets on the Overview Page?**

   No. Users would not be able to make any changes to the pre-built widgets for now, look for the future enhancements of the page.

2. **Can Users export the widget data from the Overview page?**

   No. Users would not be able to export any data generated in the pre-built widgets for now, look for the future enhancements of the page.

3. **Why Users are getting the message as "No Rows To Show"?**

   There are no related Patch Configuration created under the client, hence "No Rows To Show". Check the each configuration list by accessing through the Menu.