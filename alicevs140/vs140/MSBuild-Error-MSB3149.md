---
title: "MSBuild Error MSB3149"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 63857405-d420-457d-9ba7-80e1a2a9dcb7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3149
**MSB3149: No resources available for building a bootstrapper.**  
  
 This error occurs when no bootstrapper resource files (setup.xml) could be found which matched any culture.  
  
### To correct this error  
  
-   Go to **Control Panel**, select **Add or Remove Programs**, and repair the Visual Studio SDK, or copy the files to the appropriate directory (<SDK install path\>\bootstrapper\engine\\<culture\>\setup.xml).  
  
## See Also  
 [Product and Package Schema Reference](../vs140/Product-and-Package-Schema-Reference.md)