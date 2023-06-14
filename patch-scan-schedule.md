---
title: Patch Scan Schedule
linkTitle: Patch Scan Schedule
weight: 150
type: documentation
showRelated: false
related:
- patch-management-2.0
---

This document will walk you through the process of scheduling a scan of your device to identify missing patches. You can "Run Now" or schedule the Missing Patch Scan Job which would be executed on each device by the Agent at the specified time and date to automate the missing patch process.

## Create Patch Scan Schedule at Client Level
Follow the steps below to schedule the patch scan at client level:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then Patch Scan Schedule.
5. Click **+ ADD** to schedule a patch scan.

Let's get started on creating a patch scan schedule. You must fill out the necessary information on the following two pages:
   - Resource selection
   - Schedule

### Resource Selection
On this page, we will choose resources based on the requirements.

1. In the Job Name field, give the job scheduling a name.
2. Choose resources from the list. There are two options for doing so.
   - **Dynamic**: Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the job automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing scan job.
   - **Select Resources**: This is a manual process for searching and selecting resources by defining Resource attributes in a simple search query. The selected resources list would not be updated with newly onboarded devices if the scan schedule is saved with this option. Users have to manually update the list for any onboarding or decommission of the devices on the platform.
3. To proceed to the schedule page, click **Next**. 
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/selected-resource2.png" 
width="1200"
height="600"
alt="Credential Mapping" >}} 

### Schedule
After selecting the resource, you must now define a schedule to run the scan at the desired time.

1. On the **Schedule** section, you could specify when this patch activity should be performed:
   - Run On Demand: Select this option, If you want to apply the patch updates right away.
   - One Time: Select this option, If you want to apply the patch updates once a time.
   - Daily: Select this option, If you want to apply the patch updates on daily. You can configure this option by choosing: Every Weekday (Mon-Friday) or Everydays.
   - Weekly: Select this option, If you want to apply the patch updates on weekly wise. Configure weekly schedule by selecting: Time preference, Starting date, and Days.
   - Monthly: Select this option if you only want to apply patch updates on a monthly basis. Configure this by selecting:  Time preference, Starting date, and number of days in a month.
2. **Resource Time Zone**: You can select a specific time zone to patch all the resources in the patch configuration. When you select a time zone, it ignores the different local time zones of resources and instead uses the time zone specified in the patch configuration.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/time-zone1.png" 
width="400"
alt="Credential Mapping" >}} 

3. In the **Notifications** section, select the users you want to be notified about the scans. 
4. Click **Finish** after you configured the scheduled page.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/schedule-scan1.png" 
width="1200"
alt="Credential Mapping" >}} 

## Create Patch Scan Schedule at Partner Level
Follow the steps below to schedule the patch scan at partner level:
1. Login to OpsRamp Portal.
2. Select **All Clients**.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then Patch Scan Schedule.
5. Click **+ ADD** to schedule a patch scan.

Let's get started on creating a patch scan schedule. You must fill out the necessary information on the following two pages:
   - Resource selection
   - Schedule

### Resource Selection 
On this page, we will choose resources at Partner level based on the requirements.
1. To select a client, choose from **All Clients** or **Select Clients**.
2. In the **Job Name** field, give the configuration a name.
2. Find the resources from the list using the **+ QUERY** button.<br>
   Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the configurations automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing installation configurations.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/schedule-partner-level.png" 
width="1200"
height="600"
alt="patch management" >}} 
3. To proceed to the schedule page, click **Next**.

{{< alert title="Note" >}}
The next step (**Scheduling**) for Patch Scan Schedule at the **Partner** level is the same as described above for Client level. Follow the same steps to complete the scheduling at Partner level.
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
<td rowspan="4"><b>Resource Selection</b></td>
</tr>
<tr>
<td>Client Selection</td>
<td>&cross;</td>
<td>&check;<br/>
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
<td rowspan="7"><b>Schedule</b></td>
</tr>
<tr>
<td>Schedule Type</td>
<td> &check; </td>
<td>&check;<br/>
</tr>
<tr>
<td>Notifications</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
</tbody>
</table>

## View Scheduled Jobs
View the list of scheduled scan jobs under **Patch Management 2.0 > Patch Scan Schedule**.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/schedule-job1.png" 
width="1200"
alt="Patch Management 2.0" >}} 

The following table describes the various attributes and actions displayed on the **Patch Scan Schedule** page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Attributes</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Job Name</td>
  <td>The scheduled scan job's name.</td>
 </tr>
 <tr>
  <td>Job Schedule</td>
  <td>The start date, time, and the selected scheduled configurations.</td>
 </tr>
  <tr>
  <td>Resources</td>
  <td>The number of resources chosen when scheduling a scan job.</td>
 </tr>
  <tr>
  <td>UUID</td>
  <td>The universally unique ID used for API communication.
</td>
 </tr>
  <tr>
  <td>Search Field</td>
  <td>Use the search field to find jobs.
</td>
 </tr>
  <tr>
  <td>Edit</td>
  <td>Use the edit option to change the current job setup.</td>
 </tr>
  <tr>
  <td>Run Now</td>
  <td>This option allows you to run the job.</td>
 </tr>
  <tr>
  <td>Remove</td>
  <td>Use this option to remove tasks from the list if they are not relevant.</td>
 </tr>
</tbody>
</table>

Click on the scheduled scan job to see the configuration details of a particular scan:
   - Properties: Basic information about the user and the date the patch was created.                                               
   - Resources: See the list of resources impacted by this patch.                                              
   - Logs: View the actual event that happened while these patches were applied.
   - Next Run- Users will be able to easily check the Time Zone, Next Scheduled Run Time, and Last Run Time for a particular scheduled job.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/schedule-test5.png" 
width="1200"
alt="Credential Mapping" >}} 

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/schedule-test5-1.png" 
width="1200"
alt="Credential Mapping" >}} 

## Auto Patch Scan
If the `Auto Patch Scan` option is enabled, any resources that are not part of the existing patch scan jobs, the missing resources will be automatically scanned at 00:00 UTC.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/auto-scan.png" 
width="300"
alt="Credential Mapping" >}} 

## Notifications
Users added in the scan job will get the below email notification, after 2 hrs of scan job triggered.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-scan-notifi.png" 
width="400"
alt="patch management" >}} 