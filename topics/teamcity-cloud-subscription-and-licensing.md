[//]: # (title: TeamCity Cloud Subscription and Licensing)
[//]: # (auxiliary-id: TeamCity Cloud Subscription and Licensing)

TeamCity Cloud services are provided by a monthly subscription which includes a predefined set of resources. If you reach any of the subscription limits, you can get additional resources on demand.

This document details the terms of a subscription and licensing in TeamCity Cloud. For more information, see our [F.A.Q]() or contact us via our [issue tracker](https://youtrack.jetbrains.com/issues/TCC).

Refer to the [licensing glossary](#Cloud+Licensing+Terminology) to learn about the terms used in this document.

## TeamCity Cloud Subscription

### Committers by Subscription

TeamCity Cloud subscription plans are predominantly based on the number of _[committers](#cloud-committers)_, that are users who make changes in the project code. All users who author VCS changes require an active _committer slot_ in TeamCity Cloud. Before acquiring the subscription, we suggest that you estimate the number of potential committers in all projects you are about to run in TeamCity. If you need help choosing the subscription plan, [contact us for a demo](https://www.jetbrains.com/teamcity/request-a-demo/).

>If you have utilized all the committer slots provided in terms of the subscription and a new user makes a commit to your source project, TeamCity Cloud will not be able to start new builds with changes from that committer. Other builds will continue to start as usual. Read how you can [get extra resources](#On-demand+Cloud+Resources) in this case.

Note that only contributors to the source take the committer clots. An unlimited number of users (managers, QA, [and so on](#cloud-web-users)) can get access to the TeamCity web interface.

Each committer slot is provided with a predefined set of _resources_:
* [build credits](#cloud-build-credits) for exchanging on necessary build resources;
* [storage](#cloud-storage) for build results;
* [data transfer capacity](#cloud-data-transfer).

The more committers you have, the more build resources you are proportionally granted with. Please refer to [our website]() to see the exact rates.

### Build Credits

_[Build credits](#cloud-build-credits)_, granted per committer, are your currency in TeamCity Cloud and can be flexibly utilized according to your needs. At the end of each month, the remaining build credits expire from your subscription, and a new set of build credits is provided at the beginning of the next month.

TeamCity Cloud can run builds on two types of agents: hosted by JetBrains and hosted by a customer. Each minute of build time on [JetBrains-hosted agents](#cloud-jb-hosted-agents) will expend some number of build credits. The exact rate depends on the type of your build agent [instance tier](). We also offer prepurchased build agents for customers who can more accurately predict their build agent utilization.

By default, when providing a JetBrains-Hosted Build Agent, we draw Build Credits at the per-minute rate of its instance type. If you anticipate a high utilization rate of our JetBrains-Hosted Agents, you can alternatively [pay for these agents upfront]() to help reduce costs. Once connected, builds running on Self-Hosted and [prepaid build agents](#cloud-prepaid-agents) do not draw on any additional Build Credits.

If you purchase [additional build credits](#On-demand+Cloud+Resources), they do not expire.

### Free Trial Subscription

You can [try TeamCity Cloud for free]() for 14 days. The free trial subscription plan includes 12,000 build credits (good for up to 20 build hours on our Linux small instance type), unlimited parallel builds, 120 GB of storage, and up to 3 self-hosted build agents.

## On-demand Cloud Resources

There are two ways to get more Build Credits for your TeamCity instance. You can add extra Committer slots or, if you don't require additional Committers, you can purchase Build Credits on demand. More information is available on our [pricing] page. Build credits purchased this way do not expire. Build credits can be redeemed for additional Storage, Data Transfer, build time, self-hosted agents, and Committers as needed. Additional Committer slots can also be purchased in the [JetBrains e-store]().

Customers can utilize their Build Credits to add Self-Hosted Build Agents to their instance at a flat monthly rate. Self-Hosted Build Agents do not draw on any additional Build Credits. You can run an unlimited number of builds on Self-Hosted Build Agents.

When a Self-Hosted Build Agent is redeemed in your TeamCity Cloud instance, it increases the number of concurrent builds you can perform on Self-Hosted Agents by 1. You will be able to connect as many Self-Hosted Agents as you wish. This allows you to connect a pool of Self-Hosted Agents to your TeamCity instance that can suit a wide variety of build configurations and requirements.

### Cloud Licensing Terminology

<table>
<tr><td></td><td></td></tr>

<tr>
<td id="cloud-build-credits" auxiliary-id="cloud-build-credits">

__Build credits__

</td>

<td>

For each [committer](#cloud-committers) slot purchased, TeamCity Cloud customers are granted build credits. They act as your "currency" in TeamCity Cloud. Build credits can be redeemed in TeamCity Cloud for build minutes on our [JetBrains-hosted agents](#cloud-jb-hosted-agents) or exchanged at a flat rate for [self-hosted build agents](#cloud-self-hosted-agents). You can also exchange build credits for additional [storage](#cloud-storage), [data transfer](#cloud-data-transfer-capacity), and commiter slots.

</td>

</tr>

<tr>
<td id="cloud-build-time" auxiliary-id="cloud-build-time">

__Build time__

</td>

<td>

Build time is calculated based on the total number of minutes your builds spend from start to finish.

</td>

</tr>

<tr>
<td id="cloud-storage" auxiliary-id="cloud-storage">

__Cloud storage__

</td>

<td>


Storage is counted for the results of builds, primarily build artifacts and build logs.

You can assure you remain under your storage capacity limits by maintaining proper clean-up rules in your TeamCity Cloud instance.

</td>

</tr>

<tr>
<td id="cloud-committers" auxiliary-id="cloud-committers">

__Committer__

</td>

<td>

A user who authors VCS (version control system) changes for projects that are built by TeamCity. Once a user authors 10 changes in a VCS, they will occupy one committer slot. Committer slots are released after 30 days of inactivity.

Roughly, each developer for a project will require a committer slot in TeamCity Cloud. Regular [web users](#cloud-web-users) are unlimited in TeamCity Cloud.

</td>

</tr>

<tr>
<td id="cloud-data-transfer" auxiliary-id="cloud-data-transfer">

__Cloud data transfer__

</td>

<td>

Cloud data transfer is counted when you download artifacts and build logs from TeamCity Cloud to outside locations. For example, between self-hosted agents and TeamCity Cloud, artifacts downloaded from the browser, or through tools like wget or curl.

</td>

</tr>

<tr>
<td id="cloud-instance-tier" auxiliary-id="cloud-instance-tier">

__Instance tier__

</td>

<td>

A type of virtual machine with a preinstalled TeamCity agent instance. A tier is defined by a unique combination of an operating system and instance size. For example, the Linux Small instance tier. Depending on its expected load, each tier is provided with a predefined set of hardware resources.

</td>

</tr>

<tr>
<td id="cloud-jb-hosted-agents" auxiliary-id="cloud-jb-hosted-agents">

__JetBrains-hosted build agent__

</td>

<td>

In TeamCity Cloud, we provide [build agents](build-agent.md) (with various instance sizes and OS platforms) that can be used out of the box, without any additional configuration. These build agents are configured, maintained, and hosted by [JetBrains](https://www.jetbrains.com/). When a build is added to the [queue](build-queue.md), an agent matching the [build requirements](agent-requirements.md) will automatically spin up and start your build.

JetBrains-hosted build agents come with a preinstalled set of commonly used build software. You can view a complete list [here](supported-platforms-and-environments.md). Additionally, TeamCity build configurations allow you to run [build steps](configuring-build-steps.md) within a [Docker container](docker-wrapper.md). This provides the ability to execute build steps that require software that may not be on the build agents by default.

</td>

</tr>

<tr>
<td id="cloud-self-hosted-agents" auxiliary-id="cloud-self-hosted-agents">

__Self-hosted build agent__

</td>

<td>

Self-hosted [build agents](build-agent.md) are "bring-your-own" build agents that can be connected to TeamCity Cloud, but are hosted and managed by the customer. Self-hosted build agents are useful if you require your own specialized set of build software, specialized build environments, and so on.

</td>

</tr>

<tr>
<td id="cloud-prepaid-agents" auxiliary-id="cloud-prepaid-agents">

__Prepaid build agent__

</td>

<td>

Prepaid build agents can provide cost savings, however, one drawback is reduced parallelism: while per-minute pricing allows for an unlimited number of parallel builds, with per-month pricing you can only run one build at a time for each per-month build agent you’ve purchased.

</td>

</tr>

<tr>
<td id="cloud-web-users" auxiliary-id="cloud-web-users">

__Web users__

</td>

<td>

QA, managers, or other team members who do not author changes will not take up committer slots. They can view build results, modify build configurations, and take other actions in the TeamCity user interface with no licensing limits.

</td>

</tr>

</table>