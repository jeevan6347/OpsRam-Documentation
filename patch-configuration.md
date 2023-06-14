---
title: Patch Configurations
linkTitle: Patch Configurations
weight: 170
type: documentation
showRelated: false
related:
- patch-management-2.0
---

This section will walk you through the process of Patch installation configurations with more controlled options to Schedule, Approve, Reboot and Enable Maintenance on the devices.  You can also have the entire Patch activity from Scan to Install, automated using the Out of the Box Automation feature called [Process Definition]({{< relref "/solutions/remediation-automation/process-automation/process-definitions/_index.md" >}}), which reduces the human intervention completely to perform any Patch related tasks. 

To know more about available automation utility for Patch related tasks, see [Patch Automation]({{< relref "/solutions/remediation-automation/patch-management-2.0/automation.md" >}}). To know more about remediation and automation capability, see [Remediation Automation]({{< relref "/solutions/remediation-automation/" >}}).


## Configure the Patch Management at Client Level
To deploy Patch Installation Configurations at Client level, follow the below steps:
1. Login to OpsRamp Portal.
2. Select a **client** from the **All Clients** list.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then **Configuration**.
5. Click **+ ADD** to create a new patch configuration.

The Configuration deployment involves the below 3 steps:
- Resource Selection
- Patch Selection
- Schedule

### Resource Selection 
On this page, we will choose resources at client level based on the requirements.
1. In the **Configuration Name** field, give the configuration a name.
2. Choose resources from the list. There are two options for doing so.
   - **Dynamic**: Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the configurations automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing installation configurations.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/confi-dynamic2.png" 
width="1200"
height="600"
alt="patch management" >}} 

   {{< alert title="Resource Selection Criteria" >}}
   1. This unique feature is only applicable to dynamic patch configuration.
   2. Every eligible resource can be only assigned to a single patch configuration.
   3. When a new resource is on-boarded based on the given criteria, resource will be assigned to patch configuration.
   4. The order of assigning the resource will depends on the created date. It means, patch configuration created on an older date will be given higher priority when the assigning resources.<br>
   <b>For an example</b>: If one patch configuration is created on `10-08-2022` and another is created on `02-07-2022`, we will give first priority to configuration created on date `02-07-2022` when allocating the resources. 
   5. Resources which are not part of any existing configuration will be re-computed every 4 hours and assigned to configuration based on the criteria configured and priority.
   {{< /alert >}}

   - **Select Resources**: This is a manual process for searching and selecting resources by defining Resource attributes in a simple search query. The selected resources list would not be updated with newly onboarded devices if the installation schedule is saved with this option. Users must manually update the list for any onboarding or decommission of the devices on the platform.
3. To proceed to the patch selection page, click **Next**.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config-resource2.png" 
width="1200"
height="600"
alt="patch management" >}} 

### Patch Selection
1. In the **Patch Selection** page, select the patches to be configured by using any of the options.
   - **Approved Patches**: Would show the list of Approved Patches 
   - **Dynamic Patches**: You can have the Patches selected for the installation Dynamically using the filter criteria. With the next Missing Patch Scan job execution, if there are new patches found as per the filter criteria, those patches would be automatically included for installation under the respective configuration.
   - **Select Patches**: You can select the patched manually from the list or using the Filter criteria and then click **Apply**.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config7.png" 
width="700"
height="400"
alt="patch management" >}} 

2. Once the patch selection process is finished, click **Next** to proceed to the schedule page.
{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/config-patch-selection.png" 
width="1200"
height="600"
alt="patch management" >}} 

{{< alert title="Note" >}}
If you select multiple patches from the option **Select Patches**, in this case you cannot select more than 100 records at once; if you do, the message shown in the figure below will appear.

{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/bulk-selection-config1.png" 
width="1200"
height="600"
alt="patch management" >}}
{{< /alert >}}

### Schedule
After selecting the resource and patches, you must now define a schedule to run the scan at the desired time.
1. On the **Schedule** section, you could specify when this patch activity should be performed:
   - Run On Demand: Select this option, if you want to apply the patch updates right away.
   - One Time: Select this option, if you want to apply the patch updates once a time.
   - Daily: Select this option, if you want to apply the patch updates on daily. You can configure this option by choosing: Every Weekday (Mon-Friday) or Everydays.
   - Weekly: Select this option, if you want to apply the patch updates on weekly wise. Configure weekly schedule by selecting: Time preference, Starting date, and Days.
   - Monthly: Select this option if you only want to apply patch updates on a monthly basis. Configure this by selecting:  Time preference, Starting date, and number of days in a month.
   - Yearly: Select this option, if you want apply the patch updates on yearly once. Choose the option which are the months this should be happened. 
   - Patch Tuesday: Select this option, if you want apply the patch updates only on Tuesday of every months.
2. **Resource Time Zone**: You can select a specific time zone to patch all the resources in the patch configuration. When you select a time zone, it ignores the different local time zones of resources and instead uses the time zone specified in the patch configuration.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/time-zone1.png" 
width="300"
alt="" >}} 

3. **Reboot After Install**: Select the option Yes/No if you want to reboot the system after patch installation. If you choose **Yes**, you will be given the option to Force Reboot.
   - **Force Reboot**: If users want to reboot each server that is part of the Patch Installation job after the patch is installed, select the Force Reboot option .
4. **Approval Type**: Select type of approval of patches whether it will be Manual or Automatic. If you select Automatic type approval; all whitelisted security and critical patches are approved automatically on the selected devices.
5. **Maintenance Period**: This setting creates a maintenance window for all of the selected devices, using the given schedule and duration. To know more about scheduling maintenance period on the resources for other related use cases, see [Scheduling Maintenance Period]({{< relref "/platform-features/feature-guides/alerts-templates/scheduling-maintenance-periods.md" >}}).
6. Choose the deployed and enabled Patch Automation Process Definition from the drop-down list (if any).
7. In the **Notifications** section, select the users who want to be notified about the Patch Installation status. All the platform Users would be listed under **"Notify Users"**. If the Installation status notifications required to be sent to any external email address without having an account on the platform, enter the external email address under "CC Users" and hit enter.
8. **Precedence**: Resources allocation will be done based on the precedence order for dynamic query based configurations.
Least value will get high precedence for resource allocation.

{{< alert title="Note" >}}
The system will automatically recompute the resources every 4 hours to assign the match criteria. Recompute jobs executed every 4 hours and it should recompute the newly added resources and removed resources information only.
{{< /alert >}}

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/force-reboot1.png" 
width="600"
alt="patch management" >}} 

9. Click **Save** after you configured the scheduled page.
## Configure the Patch Management at Partner Level
To deploy Patch Installation Configurations at Partner Level, follow the below steps:
1. Login to OpsRamp Portal.
2. Select **All Clients**.
3. Go to **Configuration Management > Patch Management 2.0**.
4. On the left side of this page, click the Menu bar icon and then **Configuration**.
5. Click **+ ADD** to create a new patch configuration.

The Configuration deployment involves the below 3 steps:
- Resource Selection
- Patch Selection
- Schedule

### Resource Selection 
On this page, we will choose resources at Partner level based on the requirements.
1. To select a client, choose from **All Clients** or **Select Clients**.
2. In the **Configuration Name** field, give the configuration a name.
2. Find the resources from the list using the **+ QUERY** button.<br>
   Choose resources by adding an OpsQL query; if any resources match the query, they will be included in the configurations automatically. This will automate the process and reduce the need for user intervention whenever there are new devices onboarded and required to add new devices to the existing installation configurations.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config-partner-level.png" 
width="1200"
height="600"
alt="patch management" >}} 
3. To proceed to the patch selection page, click **Next**.

{{< alert title="Note" >}}
The next two steps for Patch Configuration at the **Partner** level (**Patch Selection** and **Scheduling**) are the same as the described above for Patch Configuration at the Client level. Follow the same steps to complete the configuration at Partner level.
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
<td rowspan="4"><b>Patch Selection</b></td>
</tr>
<tr>
<td>Approved Patches</td>
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
<td rowspan="8"><b>Schedule</b></td>
</tr>
<tr>
<td>Schedule Type</td>
<td> &check; </td>
<td>&check;<br/>
</tr>
<tr>
<td>Reboot after Install</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
</tr>
<tr>
<td>Force Reboot</td>
<td>&check;
 <br/>
</td>
<td>&check;
 <br/>
</td>
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
<tr>
<td>Maintenance Period</td>
<td>&check;
 <br/>
</td>
<td>&cross;
 <br/>
</td>
</tr>
<tr>
<td>Assign Process</td>
<td>&check;
 <br/>
</td>
<td>&cross;
 <br/>
</td>
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

## View the Patch Configuration Page
View the list of configured jobs under **Patch Management 2.0 > Configuration**.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config-view-12.png" 
width="600"
alt="patch management" >}} 

The following table describes the various attributes and actions displayed on the Patch Scan Schedule page:

<table class="table table-striped">
 <thead class="thead-dark">
     <tr>
         <th width="20%">Attributes</th>
         <th width="45%">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
  <td>Name</td>
  <td>Name of the patch configuration.</td>
 </tr>
 <tr>
  <td>Schedule</td>
  <td>The start date, time, and the selected scheduled configurations.</td>
 </tr>
  <tr>
  <td>Resources</td>
  <td>The number of resources chosen when scheduling a scan job.</td>
 </tr>
 <tr>
  <td>Precedence</td>
  <td>The number of resources chosen to prioritize for scheduling a scan job.</td>
 </tr>
  <tr>
  <td>Search button</td>
  <td>Use the search field to find jobs.</td>
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
 </tr>
  <tr>
  <td>Recompute</td>
  <td>When a dynamic query patch configuration is removed or the query is no longer valid, or resources are qualified for another patch configuration with a higher precedence order, recompute will take place.<br>
  It is applicable for only Dynamic patch configurations.<br><br>
</td>
 </tr>
</tbody>
</table>

To see the configuration of the created schedule scan such as: Properties, Resources, Patches, logs, and Installation Status, click on the configured jobs listed here.

**Properties:** Find the basic user information and the date the patch was configured.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/config12.png" 
width="400"
alt="patch management" >}} 

**Logs:** See the logs details of each run.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/logs-details.png" 
width="400"
alt="patch management" >}} 

**Installation Progress:** Check the installation status of each resource.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-progress1.png" 
width="400"
alt="patch management" >}} 

**Next Run:** Users will be able to easily check the Time Zone, Next Scheduled Run Time, and Last Run Time for a particular scheduled job.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/next-run-config.png" 
width="400"
alt="patch management" >}} 

<table class="table">
 <thead class="thead-dark">
     <tr>
         <th width="15%" style="border:none !important; ">Widget</th>
         <th width="20%" style="border:none !important; "></th>
         <th width="45%" style="border:none !important; ">Description</th>
     </tr>
 </thead>
 <tbody>
<tr>
<td rowspan="1"><b>Properties</b></td>
<td> Created By</td>
<td>User who created this patch configuration
</td>
</tr>
<tr>
<td></td>
<td>Updated By</td>
<td>User who updated this patch configuration at last
</td>
</tr>
<tr>
<td></td>
<td>Created Time</td>
<td>Time when this Configuration was created
</td>
</tr>
<tr>
<td></td>
<td>Last Updated Time</td>
<td>Time when this Configuration was Last Updated
</td>
</tr>
<tr>
<td></td>
<td>Operating System</td>
<td>Operating system of the selected Resources
</td>
</tr>
<tr>
<td></td>
<td>Reboot After Install</td>
<td>Device Reboot options selected after the Patch installation</td>
</tr>
<tr>
<td></td>
<td>Approval Type</td>
<td>Type of Approval defined for the Patch Installation</td>
</tr>
<tr>
<td></td>
<td>Maintenance Period</td>
<td>The Scheduled Maintenance period defined to ignore the Monitoring alerts generated  during Patch Installation</td>
</tr>
<tr>
<td></td>
<td>UUID</td>
<td>The unique ID generated for each Patch Configuration. These UUIDs can be used with OpsQL for any required use cases</td>
</tr>
</tbody>
<tbody>
<tr>
<td rowspan="1"><b>Resources</b></td>
<td></td>
<td>Selected Resources for the Patch Installation Configuration</td>
</tr>
<tr>
</tbody>
<tbody>
<tr>
<td rowspan="1"><b>Patches</b></td>
<td></td>
<td>Selected Patches for the Installation on the selected Devices</td>
</tr>
<tr>
</tbody>
<tbody>
<tr>
<td rowspan="1"><b>Logs</b></td>
<td></td>
<td>Activity Logs of the Patch Configurations
</td>
</tr>
<tr>
</tbody>
<tbody>
<tr>
<td rowspan="1"><b>Installation Status</b></td>
<td></td>
<td>See live status of a resource patch installation, including whether it has started, completed, failed, etc.</td>
</tr>
<tr>
</tbody>
</table>

## Recompute

### What is Recompute?
Recompute all the patch configurations based on priority, which means that all policies that will be matched with other policies must be assigned to the highest priority policy. It will perform the following tasks:
- Recompute will take care of schedule maintenance.
- Auto Approval
- Auto Trigger 
- It will identify new resources (addition/removal) and assign new changes to policies that have a high prior approval rating.

### When Recomputation is triggered?
- In rule-based configurations, resources should be re-allocated based on the precedence value.
- A lower precedence value indicates a higher priority.
- Triggers should be recreated in each of the rule-based configurations based on the allocated resources.
- Maintenance windows should be recreated/updated in each rule-based configuration based on the allocated resources.
- Auto-approval should be performed in accordance with the allocated resources in each rule-based configuration.
- Client-level configurations should be prioritized over partner-level configurations.
- Recomputation should have no effect on configurations that use static resources.

### When new resources are onboarded?
- When the Recomputation is triggered, the newly onboarded resources should be assigned to configurations with higher priority.
- Triggers and maintenance should be created for the new resources in accordance with the configurations to which they are assigned.
- Auto Approval and Reboot should function as expected.

### When resources are deleted?
- The triggers and maintenance windows associated with the deleted resources should be deleted/unassigned.

### How to Recompute?
1. Go to **Patch Management 2.0 > Configuration**.
2. Click **Recompute** on the right side of the configuration page.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/recompute.png" 
width="600"
alt="patch management" >}} 
3. When you click the Recompute button, a warning message should appear. <br>
If you want to Recompute, click **Yes**.
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/recompute-warning.png" 
alt="patch management" >}} 
4. Once Recompute is complete, you should see the following recomputation details in the **Logs** page:
   - Triggered by
   - Resources assigned/unassigned to Config_Names
   - Timestamps

## Notifications
Users added in the configuration job will get the following email notifications:
   - **Patch Install Details Notification**: Users who have been added to the configuration job will receive this email notification, after 2 hrs of job triggered.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-install-notifi.png" 
width="400"
alt="patch management" >}} 
   - **Patch Configuration Created**: Only Partner users will get this email notification.
   {{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-scan-create-notifi.png" 
width="400"
alt="patch management" >}} 