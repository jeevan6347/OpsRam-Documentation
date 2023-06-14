---
title: Missing Patches
linkTitle: Missing Patches
weight: 160
type: documentation
showRelated: false
related:
- patch-management-2.0
---

After scanning the patches and identifying a list of missing patches, this section will guide you through the process of viewing and managing the found missing patches. You can also take necessary action against each or bulk of missing patches from the list.

View the list of patches using one of the following options:
   - BY PATCH
   - BY DEVICE

## View Missing Patches By Patch
The **BY PATCH** option enables you to view the list of all the missing patches.
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of the page, click the Menu bar icon and then **Missing Patches**.
5. Enable the option **BY PATCH** to see the list of all missing patches.
6. To perform an action on a single patch, click the three-dot icon as displayed below. 

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-by-patch1.png" 
width="1200"
height="1200"
alt="patch management" >}} 

7. To perform an action on multiple patches, select the patches from the list. The available action will be displayed on the page.

{{< alert title="Note" >}}
You cannot select more than 100 records at once; if you do, the message shown in the figure below will appear.

{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/bulk-selection-missing.png" 
width="1200"
height="600"
alt="patch management" >}}
{{< /alert >}}

8. Choose the action you want to perform on the patches as shown below.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/perform-action2.png" 
width="1200"
height="600"
alt="patch management" >}} 

## View Missing Patches By Device
The **BY DEVICE** option enables you to view the list of missing patches for the devices.
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of the page, click the Menu bar icon and then **Missing Patches**.
5. Enable the option **BY DEVICE** to see the list of missing patches for the devices.
6. To perform an action on a single patch, click the three-dot icon as displayed below.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-by-device1.png" 
width="1200"
height="1200"
alt="patch management" >}} 

7. To perform an action on multiple patches, select the patches from the list. The available action will be displayed on the page.
8. Choose the action you want to perform on the patches as shown below.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/perform-action3.png" 
width="1200"
height="600"
alt="patch management" >}} 

## Additional Options and Attributes on Missing Patch Page.
Below are the additional options on the **Missing Patches** page:
   - **Search field**: To find any specific missing patches from the list. You need to add the dollar symbol ($) and then add the required data into the search field.
   - **Refresh**: Click the Refresh button to refresh this page if some of the patches are not showing up.
   - **Scan Now**: Click Scan Now to quickly scan the patches.
   - **Patch Scan Schedule**: Click Patch Scan Schedule to schedule the scan at a certain period of time. Refer to [Patch Scan Schedule]({{< relref "/solutions/remediation-automation/patch-management-2.0/patch-scan-schedule.md" >}}) for how to schedule the patch scan.

On the **Missing Patches** page, you will have various options for the listed patches. You can also choose one or more patches from the list to perform an action.

The following table describes the various action buttons displayed for the patches. 

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Action</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Approve</td>
  <td>If you click Approve, your selected missing patches will be approved for installation.</td>
 </tr>
 <tr>
  <td>Unapprove</td>
  <td>Click Unapprove to reject the selected ID/missing patches.</td>
 </tr>
  <tr>
  <td>Copy ID</td>
  <td>Use this option to copy the external ID and paste.</td>
 </tr>
  <tr>
  <td>Install</td>
  <td>Click Install to install the approved patches.</td>
 </tr>
  <tr>
  <td>Whitelist</td>
  <td>Click Whitelist to add the missing patches to your whitelist and to be approved automatically.</td>
 </tr>
  <tr>
  <td>Blacklist</td>
  <td>Click Blacklist to blacklist  the selected patches. The blacklisted patches will not be approved or installed further.</td>
 </tr>
 <tr>
  <td>Unrate</td>
  <td>If you selected the ratings (Whitelist or Blacklist), delete these ratings by clicking on the unrate button.</td>
 </tr>
</tbody>
</table>

### Use Parent Level Rating
If `USE PARENT LEVEL` is enabled, then parent organization ratings will be applicable for the organization and you will not have options to rate at the client level.<br>
To enable the parent level rating, click the **Menu bar** and enable the `USE PARENT LEVEL` button.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-rating1.png" 
width="300"
alt="patch management" >}} 


If `USE PARENT LEVEL` is disabled, then you will have options to rate at the client level.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/disabled1.png" 
width="1200"
height="1200"
alt="patch management" >}} 

The following table describes the various attributes displayed on the **Missing Patches** page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Attributes</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>External id</td>
  <td>A unique id is used to identify the patches.</td>
 </tr>
 <tr>
  <td>Patch Name</td>
  <td>Name of the patch.</td>
 </tr>
  <tr>
  <td>Category</td>
  <td>Define the type of patch, whether it is an update or a new one.</td>
 </tr>
  <tr>
  <td>Release Date</td>
  <td>Date and time of patch release.</td>
 </tr>
  <tr>
  <td>Severity</td>
  <td>Severity of the Released patch.</td>
 </tr>
  <tr>
  <td>Dependency</td>
  <td>Number of dependent Patches.</td>
 </tr>
  <tr>
  <td>Rating</td>
  <td>Assigned Patch Ratings as per the requirements.</td>
 </tr>
</tbody>
</table>

To view the Resources list related to the Patch Status, click on the Patch Name and a right side pane would pop up , click on each status to see the list of Resources:
   - Missing: Shows the number of resources where this patch was not applied.
   - Approved: Shows the number of resources where this patch was applied and approved.
   - Installed: The number of resources where this patch has been installed.
   - Failed: You can see the number of resources that have failed to install this patch.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/missing-status2.png" 
width="1200"
height="1200"
alt="patch management" >}} 