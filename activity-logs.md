---
title: Activity Logs
linkTitle: Activity Logs
weight: 191
type: documentation
showRelated: false
related:
- patch-management-2.0
---

This page displays a list of all the logs for Patch Configuration, Patch Scan, Compliance, and Bulk Patch (missing patches). This will help users to check the all logs activity in one page. 

## View List of Logs
Follow the steps below to see the list of logs:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then **Logs**.
5. Here you will have a list of all activity logs.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-activity-logs.png" 
width="600"
alt="patch management" >}} 

The following table describes the various widgets displayed on the logs page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Widgets</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Name</td>
  <td>Name of the logs.</td>
 </tr>
 <tr>
  <td>Object Type</td>
  <td>Types of logs created for scan, configuration, compliance etc.</td>
 </tr>
  <tr>
  <td>Log Message</td>
  <td>Display if any message is added during log creation.</td>
 </tr>
  <tr>
  <td>Activity Time</td>
  <td>Show date and time for log creation.</td>
 </tr>
  <tr>
  <td>Performed By</td>
  <td>Display who performed the logs.</td>
 </tr>
  <tr>
  <td>Action</td>
  <td>This will show if any log actions have been selected.</td>
 </tr>
</tbody>
</table>

## Apply Filter to View the Logs
You can use the filter option to narrow down the list of logs and view them individually for Scan, Configuration, Compliance, and Bulk Actions.

Follow the steps below to apply the filter to the activity logs:
1. On the right side of this page, click on the **filter** icon.
2. Choose a date and time for which you want to view the logs.
3. Select a **Object Type** from the list below:
   - **Scan**: If you select Scan, you will be able to view the patch scan logs.
   - **Configuration**: If you select Configuration, you will be able to view the patch configuration logs.
   - **Compliance**: If you select Compliance, you will be able to view the compliance logs.
   - **Bulk Actions**: If you select Bulk Actions, you will be able to view all the missing patch logs.
4. You can also select the name of the object type.
5. Choose **Action Types** from the list for the object.
6. After you have entered all of your filter criteria, click **Apply**. 
7. If you want to reset the filter criteria, click the **Reset** button.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-activity-logs-filter.png" 
width="600"
alt="patch management" >}} 