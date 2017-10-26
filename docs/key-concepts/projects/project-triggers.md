---
title: Project Triggers
description: Project Triggers allow you to define unattended behavior for your project such as automatically deploying a release to an environment.
position: 3
version: 3.4
---

Project Triggers allow you to define an unattended behavior for your [Projects](/docs/key-concepts/projects/index.md).

:::success
We have written a [comprehensive guide](/docs/guides/elastic-and-transient-environments/index.md) about using Project Triggers (specifically [Automatic Deployment Triggers](/docs/deploying-applications/automatic-deployment-triggers.md)) with a focus on deploying to elastic and transient environments.
:::

Project Triggers allow you to choose from a subset of **events** that can occur in Octopus Deploy, apply a **filter** to those events, and decide on an **action** you want performed once the trigger fires. The example below shows an [Automatic Deployment Trigger](/docs/deploying-applications/automatic-deployment-triggers.md) configured to fire when a [Deployment Target](/docs/deployment-targets/index.md) with the [Machine Role](/docs/key-concepts/machine-roles.md) **web-server** belonging to the **Production** [Environment](/docs/key-concepts/environments/index.md) becomes available.

![](/docs/images/5671189/5865830.png "width=500")

## What kinds of Project Triggers are available? {#ProjectTriggers-WhatkindsofProjectTriggersareavailable?}

[Automatic Deployment Triggers](/docs/deploying-applications/automatic-deployment-triggers.md) are the first kind of Project Trigger available in Octopus Deploy, and at the time of writing, the only kind. We think this concept could also extend to other automated actions like these:

- Automatically create a release when packages are pushed to a repository (think of a more intelligent version of [Automatic Release Creation](/docs/deploying-applications/automatic-release-creation.md))
- Automatically deploy a release to a particular [Environment](/docs/key-concepts/environments/index.md) when the Release is created
- Automatically deploy the current release to a [Tenant](/docs/key-concepts/tenants/index.md) when they are [connected to a Project and Environment](/docs/guides/multi-tenant-deployments/multi-tenant-deployment-guide/deploying-a-simple-multi-tenant-project.md)

Get in touch and let us know what you think of these ideas!
