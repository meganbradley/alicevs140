---
title: "SetEnv Task"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fd9e4225-68cb-4608-8b27-468b0218c936
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SetEnv Task
Sets or deletes the value of a specified environment variable.  
  
## Parameters  
 The following table describes the parameters of the **SetEnv** task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|**Name**|Required **String** parameter.<br /><br /> The name of an environment variable.|  
|**OutputEnvironmentVariable**|Optional **String** output parameter.<br /><br /> Contains the value that is assigned to the environment variable that is specified by the **Name** parameter.|  
|**Prefix**|Mandatory `Boolean` parameter.<br /><br /> If `true`, concatenates the value of the **Value** parameter before the value of the environment variable that is specified by the **Name** parameter, and then assigns the result to the environment variable. If `false`, assigns only the value of the **Value** parameter to the environment variable.|  
|**Target**|Optional **String** parameter.<br /><br /> Specifies the location where an environment variable is stored. Specify "`User`" or "`Machine`".<br /><br /> For more information, see "EnvironmentVariableTarget Enumeration" on the [MSDN](http://go.microsoft.com/fwlink/?LinkId=737) Web site.|  
|**Value**|Optional **String** parameter.<br /><br /> The value assigned to the environment variable that is specified by the **Name** parameter. If **Value** is empty and the variable exists, the variable is deleted. If the variable does not exist, no error occurs even though the operation cannot be performed.<br /><br /> For more information, see "Environment::SetEnvironmentVariable Method" on the [MSDN](http://go.microsoft.com/fwlink/?LinkId=737) Web site.|  
  
## Remarks  
  
## See Also  
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)