---
title: "Expected one of &#39;Dim&#39;, &#39;Const&#39;, &#39;Public&#39;, &#39;Private&#39;, &#39;Protected&#39;, &#39;Friend&#39;, &#39;Shadows&#39;, &#39;ReadOnly&#39; or &#39;Shared&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95684eaa-5aa2-4ae4-9a73-5f97c491e02c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expected one of &#39;Dim&#39;, &#39;Const&#39;, &#39;Public&#39;, &#39;Private&#39;, &#39;Protected&#39;, &#39;Friend&#39;, &#39;Shadows&#39;, &#39;ReadOnly&#39; or &#39;Shared&#39;
A declaration statement is missing a declaration keyword. One possible cause is that an attribute declaration calls a method.  
  
 **Error ID:** BC30195  
  
### To correct this error  
  
1.  Check to see if a method is declared inside an attribute declaration.  
  
2.  Start the statement with the appropriate declaration keyword.  
  
## See Also  
 [Declared Elements](../vs140/Declared-Elements-in-Visual-Basic.md)   
 [Arrays cannot be declared with 'New'](../vs140/Arrays-cannot-be-declared-with--New-.md)