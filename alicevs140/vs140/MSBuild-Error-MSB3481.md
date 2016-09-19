---
title: "MSBuild Error MSB3481"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55f99775-3bd5-4e1b-b184-c6405d75e8ff
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3481
**MSB3481: The signing certificate could not be located. Ensure that it is in the current user's personal store.**  
  
 This error is generated when the signing certificate was not found in your personal certificate store. This error is similar to [MSBuild Error MSB3486](../vs140/MSBuild-Error-MSB3486.md), which means that the certificate was found, but does not match.  
  
### To correct this error  
  
-   Make sure that a valid certificate that matches your project's .pfx file is in your personal certificate store.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)