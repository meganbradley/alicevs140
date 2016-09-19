---
title: "MSBuild Error MSB3187"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5e93c14-b099-4176-bf1b-dbecc47fb3fd
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3187
**MSB3187: Referenced assembly '<assembly\>' targets a different processor than the application.**  
  
 This warning is generated when the application's target platform (processor architecture) is set to neutral (MSIL) and the referenced assembly is not neutral, or if the application's architecture is not neutral and the dependency is neutral. Also, if both are not platform-neutral, then their architecture must match. In addition, application architecture and entry point assembly architecture must always match.  
  
### To correct this error  
  
-   Make sure that the application's target platform (processor architecture) matches all referenced assemblies and the entry point assembly architecture.  
  
## See Also  
 [Advanced Compiler Settings Dialog Box (Visual Basic)](../Topic/Advanced%20Compiler%20Settings%20Dialog%20Box%20\(Visual%20Basic\).md)   
 [Build Page, Project Designer (C#)](../Topic/Build%20Page,%20Project%20Designer%20\(C%23\).md)