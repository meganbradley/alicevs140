---
title: "XML literals and XML axis properties are not available during this debugging session because they are not used in this assembly"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36be5c92-dd6b-41d4-894a-2bd71d772092
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XML literals and XML axis properties are not available during this debugging session because they are not used in this assembly
An XML literal or XML axis property has been referenced in the **Watch** or **Immediate** window during a debugging session in which XML in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] features are not available. This is the case for an assembly that either does not use the XML in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] features or is a release build.  
  
 **Error ID:** BC31196  
  
### To correct this error  
  
-   Start a new debugging session using the debug build of the assembly.  
  
## See Also  
 [Debugging Your Visual Basic Application](../vs140/Debugging-Your-Visual-Basic-Application.md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML in Visual Basic](../Topic/XML%20in%20Visual%20Basic.md)