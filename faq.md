---
title: FAQs
linkTitle: FAQs
weight: 210
type: documentation
showRelated: false
related:
- patch-management-2.0
---

## How can I find the missing patches for the devices?

Create and a run a missing patches request job to identify missing patches. After the completion Missing Patch Scan job, users can view the Missing patches under **Configuration Management → Patch Management 2.0 → Menu → Missing Patches**. 

You can view the Missing Patch list for each device under **Infrastructure→ Resources → Select Resource → Patches**.

## What are the different types of approvals?
   - Auto approval: Automatically approve patches. Auto approval is applicable to Windows only.
   - Manual approval: Manual approval is needed to install a patch.

## What happens when the device fails during the patch windows?

To perform any patch related tasks, the agent should be up and running on the device.  If the Patch installation fails, alerts will be generated. The failure details including patch and device information will be available under **Configuration Management → Patch Management 2.0 → Menu → Installed**.

## What happens when the device needs to be rebooted after patching?

If configured to reboot servers after patching, the following message is displayed:
`"Patching completed and need to reboot"`

You can ignore the reboot if automatic reboot is not enabled.

## What is the reason to create a Patch Scan Schedule?
Use a job to gather missing patch details from the servers configured at the device.

## What is the reason for the mismatch between local machine patches and server patches?
Confirm that the server settings are a Microsoft server or WSUS server, local.

## Are incidents created during patching?
No, Incidents are not created during patching. However, if there are requirements to create incidents, then users can deploy Alert Escalation Policies by defining the filter criteria to look for Patch related alerts for escalation.