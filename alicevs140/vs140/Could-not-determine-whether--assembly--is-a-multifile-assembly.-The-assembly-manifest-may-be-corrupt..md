---
title: "Could not determine whether &#39;assembly&#39; is a multifile assembly. The assembly manifest may be corrupt."
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d4af6ef-c2f8-4764-af8b-580d433bfbc9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Could not determine whether &#39;assembly&#39; is a multifile assembly. The assembly manifest may be corrupt.
The project system was unable to read an assembly referenced by your project such that the project system is unable to determine which files were referenced by the assembly.  
  
 **To correct this error**  
  
-   Reinstall Visual Studio (if the assembly came with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] or the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]).  
  
     \- or -  
  
-   Reinstall the appropriate third-party control.  
  
     This error will not prevent the project from building. However, a run-time error is possible.  
  
## See Also  
 [Troubleshooting Broken References](../vs140/Troubleshooting-Broken-References.md)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Assemblies in the Common Language Runtime](assetId:///33a0bc6a-6bb3-44c7-ada7-4a046e8c0945)