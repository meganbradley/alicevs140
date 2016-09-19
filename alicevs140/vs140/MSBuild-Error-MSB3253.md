---
title: "MSBuild Error MSB3253"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4b5eb5b-703b-4b80-aa5d-6c70ff9fe84d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3253
**MSB3254: The assembly <name\> referenced in the project depends on <name2\> which is not contained in the .NET Framework Client Profile.**  
  
 One of the assemblies, or dependent assemblies, referenced in the project depends on another assembly that is not contained in the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)].  
  
 This message typically occurs when a project references a third-party control or DLL that itself references an external assembly. For example, a project uses a control that in turn uses functionality that is contained in the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. If the application is re-targeted to [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)] and is installed on a system that does not have [!INCLUDE[net_v35_long](../vs140/includes/net_v35_long_md.md)], the application may not work correctly if it tries to access functionality that is not contained in the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)] subset.  
  
 This "error" message is actually only a warning; the application will still compile. However, it may fail later if the control or DLL refers to functionality that is located in a missing assembly.  
  
 The [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)] is a subset of the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] 3.5 run-time library. For more information about the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)], see [.NET Framework Client Overview](assetId:///f0219919-1f02-4588-8704-327a62fd91f1).  
  
### To correct this error  
  
-   Either remove the specified assembly reference from the project, or target the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] instead of the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)] subset library. For information about how to target the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], see [How To: Target a Specific .NET Framework](../vs140/How-to--Target-a-Version-of-the-.NET-Framework.md).  
  
## See Also  
 [MSBuild Target Framework and Target Platform](../vs140/MSBuild-Target-Framework-and-Target-Platform.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)