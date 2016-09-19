---
title: "MSBuild Error MSB4143"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 25019aa4-f0da-4bcd-862e-9b5a57913bb4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB4143
**MSB4143: The expression "<expression\>" cannot be evaluated.**  
  
 A property expression that reads its value from the registry cannot be evaluated.  
  
### To correct this error  
  
-   Make sure that the property follows the correct syntax to read a value from the registry. For example: `$(Registry:HKEY_LOCAL_MACHINE\Software\Microsoft\VisualStudio\8.0\MSBuild@MSBuildBinPath)`.  
  
## See Also  
 [MSBuild Properties](../Topic/MSBuild%20Properties.md)   
 [Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)   
 [Resources for Troubleshooting MSBuild Errors](../vs140/Additional-MSBuild-Resources.md)