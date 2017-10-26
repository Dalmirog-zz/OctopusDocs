---
title: Environments
description: Environments allow you to define a group of machines that you will deploy to at the same time; common examples of environments are **Dev**, **Test** or **Production**.
position: 0
---

In Octopus, an *environment* is a group of machines that you will deploy to at the same time; common examples of environments are **Test**, **Acceptance**, **Staging** or **Production**.

## Managing environments {#Environments-Managingenvironments}

!partial <location>

![](environments.png "width=500")

Environments can be added using the **Add environment** button.

![](add-environment.png "width=500")

:::success
**Tip: don&#39;t forget project groups**
[Project groups](/docs/key-concepts/project-groups.md) can be used to limit which environments a project can be deployed to. When adding an environment, don't forget to modify any project groups to add the new environment!
:::

## Adding machines to environments {#Environments-Addingmachinestoenvironments}

Machines can be added to environments in different ways, [depending on how they will communicate](/docs/installation/installing-tentacles/index.md) with the Octopus Deploy Server.

- Adding [listening machines](/docs/installation/installing-tentacles/listening-tentacles.md)
- Adding [polling machines](/docs/installation/installing-tentacles/polling-tentacles.md)

## Environment ordering {#Environments-Environmentordering}

!partial <reorder-link>

![](environment-reordering-button.png "width=500")

![](environment-reordering.png "width=500")

The order that environments are shown on the Environments tab also affects:

- The order that they are shown in the Dashboard
- The order that they are listed in when choosing which environment to deploy a release to

It's a good idea to put your least production-like environments first, and the most production-like environments last.

## Guided failures {#Environments-Guidedfailures}

[Guided failure mode](/docs/deploying-applications/guided-failures.md) can be enabled on an environment by default. This is useful for critical environments that are usually deployed to manually (for example, staging and production-like environments), though you may want to disable this feature for environments which are deployed to automatically such as smoke testing environments.

Guided failure mode is an option when editing an environment:

![](guided-failure.png "width=500")

(Note that this option only sets it *by* *default*: for individual deployments it can be overridden)

!partial <guided-failure-indicator>

## Associating projects with environments {#Environments-Associatingprojectswithenvironments}

By default, a project can be deployed to any environment. You can limit which projects can be deployed to which environment using [Lifecycles](/docs/key-concepts/lifecycles.md). This is useful if you have one set of environments for projects developed by one team, and another set of environments for projects developed by another team.

## Environment permissions {#Environments-Environmentpermissions}

You can control who has access to view or edit environments, as well as who has access to deploy to environments, by assigning users to Teams and assigning roles to those teams. For more information, see the section on [managing users and teams](/docs/administration/managing-users-and-teams/index.md).
