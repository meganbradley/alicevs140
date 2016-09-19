---
title: "MSBuild Error MSB3113"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81e73738-e6ee-4651-9f48-acb1feef3ff5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3113
**MSB3113: Could not find file '<file\>'.**  
  
 This error is generated when an irresolvable reference is encountered when creating a new manifest. It might have originated from the project file or as a task parameter.  
  
### To correct this error  
  
-   Check your project file (and build parameters, if you are custom building) for conflicts in file references.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)