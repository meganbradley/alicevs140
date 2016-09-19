---
title: "How to: Specify Verbose Log Files for ClickOnce Deployments"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0807a28d-2e40-4a51-ab10-308d808ded6b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Specify Verbose Log Files for ClickOnce Deployments
[!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] maintains activity log files for all deployments. These logs document details pertaining to installing, initializing, updating, and uninstalling a [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] deployment. To increase the detail that [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] writes to these log files, use Registry Editor (**regedit.exe**) to specify the verbosity level.  
  
> [!CAUTION]
>  If you use Registry Editor incorrectly, you may cause serious problems that may require you to reinstall the operating system. Use Registry Editor at your own risk.  
  
 The following procedure describes how to specify the verbosity level for [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] log files for the current user. To reduce the level of verbosity, remove this registry value.  
  
### To specify verbose log files  
  
1.  Open **Regedit.exe**.  
  
2.  Navigate to the node `HKEY_CURRENT_USER\Software\Classes\Software\Microsoft\Windows\CurrentVersion\Deployment`.  
  
3.  If necessary, create a new string value named `LogVerbosityLevel`.  
  
4.  Set the `LogVerbosityLevel` value to `1`.  
  
## See Also  
 [Troubleshooting ClickOnce Deployments](../vs140/Troubleshooting-ClickOnce-Deployments.md)