---
title: Creating an Azure Account
description: Creating an Azure Account in Octopus Deploy contains the details of your Azure subscription. 
---

An Azure Account in Octopus Deploy contains the details of your Azure subscription.  It is used to authenticate with Azure when deploying or executing scripts.

To create an Azure Account, navigate to {{Infrastructure,Accounts}} and click *Add Account* in the *Azure Subscriptions* section.

![](add-new-azure-account.png "width=500")

## Authentication Method {#CreatinganAzureAccount-AuthenticationMethod}

Octopus Deploy authenticates with Azure in one of two methods: using a *Management Certificate* or a *Service Principal*.

The divide in authentication-methods in Octopus reflects the divide within Azure itself: There are two distinct interfaces for interacting with Azure, Service Management (ASM) and Resource Manager (ARM).  [This document](https://azure.microsoft.com/en-us/documentation/articles/resource-manager-deployment-model/) explains the differences.

- If you wish to use Resource Manager mode, then you will need to [create a Service Principal account](/docs/guides/azure-deployments/creating-an-azure-account/creating-an-azure-service-principal-account.md).
- If you wish to Service Management mode, then you will need to create a [Management Certificate account](/docs/guides/azure-deployments/creating-an-azure-account/creating-an-azure-management-certificate-account.md).

![](add-new-azure-account-detail.png "width=500")
