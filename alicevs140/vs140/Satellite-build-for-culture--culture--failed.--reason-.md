---
title: "Satellite build for culture &#39;culture&#39; failed. &lt;reason&gt;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c97c589f-cf4d-4f6b-941a-7526a1091fce
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Satellite build for culture &#39;culture&#39; failed. &lt;reason&gt;
A satellite assembly for a particular culture could not be built. This error will cause the build process to fail.  
  
 This error can appear for two reasons:  
  
1.  ALINK.EXE is not installed on the system.  
  
2.  ALINK.EXE failed but did not return any extended error information.  
  
 **To correct this error**  
  
-   Reinstall [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] or just the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)].  
  
-   When <reason\> is reported as "The assembly linker could not be launched. The file exists," empty the Temp folder in which the files are generated (for example, C:\Documents and Settings\\<user\>\Local Settings\Temp).  
  
## See Also  
 [Assembly Linker (Al.exe)](assetId:///b5382965-0053-47cf-b92f-862860275a01)