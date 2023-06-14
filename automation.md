---
title: Patch Automation
linkTitle: Patch Automation
weight: 200
type: documentation
showRelated: false
related:
- patch-management-2.0
---

This section provides the details about automating the entire patch activities using the platform strong Automation and Remediation capability.

## Patch Process Automation using Process Definition
OpsRamp provides a very strong Out of the Box Automation and Remediation layer with the features like [Process Definition]({{< relref "/solutions/remediation-automation/process-automation/process-definitions/" >}}), [Scripts and Jobs]({{< relref "/solutions/remediation-automation/jobs-and-scripts/" >}}). Using the patch services under Processes Definition feature, users can define multiple patch workflow actions sequentially, starting from the missing patch Scan → approving the missing patches → installing the missing patches. 

Users can also use the scripts feature to deploy and manage any pre and post check activity scripts used by any operation teams that must be executed on the end devices before and after patch installation as needed. Process definitions for patch activates would only need to be deployed once, and then selected as "Process" from the [Patch Configuration]({{< relref "/solutions/remediation-automation/patch-management-2.0/patch-configuration.md" >}}) page to trigger the execution of these designed patch workflows.

The following is an example of a generic Patch Process Workflow designed using the Process Definition feature which reduces any Human intervention required to perform any patch related tasks.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-process1.png" 
width="900"
alt="patch management" >}} 

{{< alert title="Note" >}}
Users can design any custom patch workflow as per the requirements and defined operation procedures. Above shown is just a recommended flow and not a mandatory flow.
{{< /alert >}}

Below are the Patch Services available under Process Definition feature and PATCH MANAGEMENT Category.

{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-management2.png" 
width="900"
alt="patch management" >}} 
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/patch-management3.png" 
width="400"
alt="patch management" >}} 

To learn more about process definition features, see [Process Definition]({{< relref "/solutions/remediation-automation/process-automation/process-definitions/" >}}) article.

## Recommendations
We recommend to use at least one Process Definition in the Patch Configurations to automate the complete patch process which provides the below mentioned value additions.

**Without Patch Automation**
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/without-automation1.png" 
width="700"
alt="patch management" >}} 

Major challenges with manual process:
1. Time consuming.
2. Required dedicated Windows and Linux teams to perform each step manually including pre and post patching tasks.
3. Manual efforts to send notifications about patching status.

**Using Patch Automation**
{{< figure 
src="https://docsmedia.opsramp.com/screenshots/Patch/with-automation1.png" 
width="700"
alt="patch management" >}} 

Advantages of Automated Patch Process:
1. Higher efficiency and productivity.
2. Reduction in time and dedicated required manual efforts from operations teams.
3. Improving compliance and increasing ability to scale.