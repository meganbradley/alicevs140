---
title: "Information for the type of &#39;&lt;typename&gt;&#39; has not been loaded into the runtime"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0f074f9-571d-48f8-b334-4fd34b61cd89
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Information for the type of &#39;&lt;typename&gt;&#39; has not been loaded into the runtime
A type was referenced that has not been loaded by the runtime.  
  
 **Error ID:** BC30750  
  
### To correct this error  
  
1.  Restructure your code so the type is defined within the current scope.  
  
2.  Verify that the member is defined and that you have spelled the member name correctly.  
  
3.  Try accessing one of the members declared in the module. In some cases, the debugging environment cannot locate members because the modules where they are declared are not loaded.  
  
## See Also  
 [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)