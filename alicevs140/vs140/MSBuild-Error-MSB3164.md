---
title: "MSBuild Error MSB3164"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5a1e31fc-0322-4d4e-8c26-013b1efb82c9
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3164
**MSB3164: No 'HomeSite' attribute has been provided for '<package\>', so the package will be published to the same location as the bootstrapper.**  
  
 This warning is generated when the user wants to use HomeSite, but the appropriate HomeSite info for the specified package is not available.  
  
### To correct this error  
  
-   Update the manifest files to include HomeSite info.  
  
-   Alternatively, do not use HomeSite.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)