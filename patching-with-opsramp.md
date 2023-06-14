---
title: Patching With OpsRamp
linkTitle: Patching With OpsRamp
weight: 100
type: documentation
showRelated: false
related:
- patch-management-2.0
---

## Why Patching with OpsRamp?
With the aid of the OpsRamp patch management solution, you can automate the entire patch management process without no cost, from the identification of missing patches to the process of patch deployment to endpoints.

This helps in the reduction of system failures, allowing you to increase production while reducing the costs associated with improper patch management. Instead of manually maintaining patches and upgrades on your network's numerous devices, you can focus on key business tasks that enhance revenue with automated patch management.

## Advantages of Patching with OpsRamp
There are numerous benefits to OpsRamp Patch management, some of which are highlighted below:

- Out of box platform feature with no extra cost.
- There is no need for a separate agent to perform Patching activity including Patch Automation.
- Easy to setup the entire patch activity flow from scan to installation.
- Agent deployed devices also configured for monitoring on the same platform which helps in tracking the device status during pre and post patching.
- Visibility at the partner and customer levels, particularly for MSPs where managing patches is quite simple.
- Easy steps for patch approval, installation, monitoring, and notification configurations.
- Custom jobs can be scheduled to completely automate the execution of external patch automation scripts.
- Custom setup that reduces the need for manual intervention both during and after the patching activity
- Custom scripts for Windows and Linux that make use of the Run Book Automation (RBA) capability and make RBA scripts accessible to partners and customers for maximum control.
- Patch Dashboards that come pre-configured with easy customizable widgets, readily available reports, and analyses of device status are available.
- Controlled patch activity related alerts and easily customizable notifications.
- All Patch Management capabilities are supported at both client and partner levels.

## Standard Patch Workflow 

{{< figure
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-flow.png"
width="900"
alt="By Patch" >}}

Key steps to the patch management process include:

1. **Patch Feed Setup**: Patch feed is a source of published patch information including all the available patch attributes. You can setup patch feed through:
   - Platform integration with vendor sites.
   - WSUS (Windows Update Service)
2. **Missing Patch Scan**:
   - You can create jobs to automate the process for missing patches for one time or scheduled for the specified time and date.
   - You can view scanned missing patches.
3. **Patch Configurations**: You can schedule patch configurations on a periodic or on-demand basis. Once missing patches are identified: 
   - Approve the missing patches - Manually or Automatically
   - Agent initiates the downloading of the approved missing patches
   - Enable maintenance windows during the Patch installation to suppress the alerts
   - Install the downloaded missing patches
4. **Patch Compliance**: Compliance is a metric that provides the number of uninstalled patches in the baseline on a device. You can view the patch compliance status.
5. **Reports and Dashboards**: Use the readily available Reports and Dashboard widgets to view the patch and device status against the user defined compliance criteria.

## Supported Patch Categories
- **Security and Critical**: Security patch updates can fix vulnerabilities to new attacks that have cropped up and Critical Patch Updates are collections of security fixes for Oracle products. 
- **Definition Updates**: Definition updates is regularly downloading updates to the definition files that are used to identify spyware and other potentially unwanted software.
- **Feature Packs**: Feature Pack is a pack of updates that contains fixes, enhancements, performance improvements, and so on.
- **Service Packs**: A service pack is a collection of updates and fixes, called patches, for an operating system or a software program.
- **Updates**: An update is new, improved, or fixed software, which replaces older versions of the same software. For example, updating your operating system brings it up-to-date with the latest drivers, system utilities, and security software.
- **Update Rollups**: Rollup updates is a cumulative setup of hotfixes that contains security updates, and critical updates that need to be deployed immediately.

## Classic Patch Management Vs Patch Management 2.0
The following table summarizes the feature differences between OpsRamp Classic Patch Management Vs Patch Management 2.0.

<table class="table">
 <thead class="thead-dark">
     <tr>
         <th width="40%" style="border:none !important; ">Feature</th>
         <th width="20%" style="border:none !important; ">Classic Patch Management</th>
         <th width="20%" style="border:none !important; ">Patch Management 2.0</th>
     </tr>
 </thead>
 <tbody>
<tr>
<td rowspan="2"><b>Overview</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>OpsQL for Patches & Resources</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Schedule for Scan & Install
</b></td>
</tr>
<tr>
<td>&check;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Notifications for out of Platform users</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Single Page Navigation</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Patch feed integration required
</b></td>
</tr>
<tr>
<td> &check;</td>
<td>&cross;<br/>
</tr>
<tr>
<td rowspan="2"><b>Auto Patch Scan</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Parent Level Rating </b></td>
</tr>
<tr>
<td>&check;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Patch Progress</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Audit logs for all the actions</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Partner level Patch Configuration</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Patch Compliance</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Patch Configurations & Scan</b></td>
</tr>
<tr>
<td>&check;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Quick Actions on Patch
</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Bulk Operations</b></td>
</tr>
<tr>
<td>&cross;</td>
<td>&check;<br/>
</tr>
<tr>
<td rowspan="2"><b>Snapshots and Metric Graph</b></td>
</tr>
<tr>
<td> &check; </td>
<td>&cross;<br/>
</tr>
<tr>
<td rowspan="3"><b>Schedule for Scan & Install</b></td>
<td>&check;</td>
<td>&check; (Advanced)<br/>
</td>
</tr>
</tbody>
</table>