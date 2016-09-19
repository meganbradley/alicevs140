---
title: "ResolveKeySource Task"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 449f06c2-e9aa-4236-ab1e-c45c25452b2e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ResolveKeySource Task
Determines the strong name key source.  
  
## Task Parameters  
 The following table describes the parameters of the `ResolveKeySource` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`AutoClosePasswordPromptShow`|Optional `Int32` parameter.<br /><br /> Gets or sets the amount of time, in seconds, to display the count down message.|  
|`AutoClosePasswordPromptTimeout`|Optional `Int32` parameter.<br /><br /> Gets or sets the amount of time, in seconds, to wait before closing the password prompt dialog.|  
|`CertificateFile`|Optional `String` parameter.<br /><br /> Gets or sets the path of the certificate file.|  
|`CertificateThumbprint`|Optional `String` parameter.<br /><br /> Gets or sets the certificate thumbprint.|  
|`KeyFile`|Optional `String` parameter.<br /><br /> Gets or sets the path of the key file.|  
|`ResolvedKeyContainer`|Optional `String` output parameter.<br /><br /> Gets or sets the resolved key container.|  
|`ResolvedKeyFile`|Optional `String` output parameter.<br /><br /> Gets or sets the resolved key file.|  
|`ResolvedThumbprint`|Optional `String` output parameter.<br /><br /> Gets or sets the resolved certificate thumbprint.|  
|`ShowImportDialogDespitePreviousFailures`|Optional `Boolean` parameter.<br /><br /> If `true`, show the import dialog despite previous failures.|  
|`SuppressAutoClosePasswordPrompt`|Optional `Boolean` parameter.<br /><br /> Gets or sets a Boolean value that specifies whether the password prompt dialog should not auto-close.|  
  
## Remarks  
 In addition to the parameters listed above, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension?qualifyHint=False> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../Topic/TaskExtension%20Base%20Class.md).  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)