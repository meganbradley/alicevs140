---
title: "Creating and Using Code Analysis Check-In Policies"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3fa5a849-e05f-4e31-8ba3-b014c889d94d
caps.latest.revision: 41
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating and Using Code Analysis Check-In Policies
When you use Team Foundation Version Control (TFVC), you can create a code analysis check-in policy for the .NET Framework and native (C/C++) code projects in a team project. You can use the code analysis check-in policy to control and improve the quality of code that is checked into the code base.  
  
 The policy passes when the local build is up to date and code analysis has been run on the most recent source files. At a minimum, the code analysis rules that are enabled in the code project must contain the same rules as those that are defined in the team project check-in policy. Rules that have been specified as errors in the Team Project Settings must also be specified as errors in the code project  
  
> [!IMPORTANT]
>  Code analysis check-in policies cannot be applied to web site projects. They can be applied to web application projects.  
  
 You create code analysis check-in policies by using the Team Project Settings of [!INCLUDE[esprscc](../vs140/includes/esprscc_md.md)]. Check-in policies are specified and enforced for a team project, but code analysis runs are configured and run for individual code projects on local development computers. This section describes how to specify code analysis check-in policies for a team project and how to implement custom code analysis policies for managed code.  
  
## In This Section  
 [How to: Create or Update Standard Code Analysis Check-in Policies](../vs140/How-to--Create-or-Update-Standard-Code-Analysis-Check-in-Policies.md)  
 Explains the steps that you use to set and modify a code analysis policy for a team project.  
  
 [Implementing Custom Code Analysis Check-in Policies for Managed Code](../vs140/Implementing-Custom-Code-Analysis-Check-in-Policies-for-Managed-Code.md)  
 Explains the steps that you use to create a custom rule set for the check-in policy of a team project, and to synchronize the code projects of the team project with the check-in policy.  
  
 [Version Compatibility for Check-In Policies](../vs140/Version-Compatibility-for-Code-Analysis-Check-In-Policies.md)  
 Explains code analysis check-in compatibility issues between versions of [!INCLUDE[vstsLong](../vs140/includes/vstsLong_md.md)].  
  
 [How to: Customize the Code Analysis Dictionary](../vs140/How-to--Customize-the-Code-Analysis-Dictionary.md)  
 Explains how to add words and tokens to the dictionary that is referenced in code analysis naming rules.  
  
## Related Sections  
 [Set and Enforce Quality Gates](assetId:///bdc5666e-6cf0-45b2-a0a1-133c3f61e852)  
  
 [Analyzing Application Quality](../vs140/Enhancing-Code-Quality-with-Team-Project-Check-in-Policies.md)