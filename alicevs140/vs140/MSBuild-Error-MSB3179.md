---
title: "MSBuild Error MSB3179"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa744f6c-e398-4e60-b4f7-455ace7e3bd2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3179
**MSB3179: Problem isolating COM reference '<assembly\>': '<error\>'**  
  
 This is a generic error message indicating a problem with the generation of RegFree COM entries in application manifest (as specified by the `IsolatedComReferences` task parameter). The latter part of the error message contains more information about the nature of the problem. A possible cause of this error is that RegFree COM components are not properly registered on the build computer.  
  
### To correct this error  
  
-   Make sure that all COM components are registered on the build computer.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)