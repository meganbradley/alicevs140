---
title: "MSBuild Error MSB3252"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4e6982b8-84b3-4d21-94e1-05cc10bf1393
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3252
**MSB3252: The project has a reference to assembly <name\>. This assembly is not part of the .NET Framework Client Profile.  By not having this reference there may be compile or runtime errors.**  
  
 A call was made to a member in an assembly, or dependent assembly, that is not part of the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)]. Therefore, the call cannot be resolved and the application cannot be compiled.  
  
 For more information about the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)], see [.NET Framework Client Overview](assetId:///f0219919-1f02-4588-8704-327a62fd91f1).  
  
### To correct this error  
  
-   Either remove the specified assembly reference from your project, or target the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] instead of the [!INCLUDE[net_client_v35_long](../vs140/includes/net_client_v35_long_md.md)] subset library. For information about how to target the full [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], see [How To: Target a Specific .NET Framework](../vs140/How-to--Target-a-Version-of-the-.NET-Framework.md).  
  
## See Also  
 [MSBuild Target Framework and Target Platform](../vs140/MSBuild-Target-Framework-and-Target-Platform.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)