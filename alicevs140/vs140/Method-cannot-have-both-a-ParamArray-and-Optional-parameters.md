---
title: "Method cannot have both a ParamArray and Optional parameters"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 41066df8-c9ee-4f67-9f6c-4f62e3abc7be
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method cannot have both a ParamArray and Optional parameters
A `ParamArray` argument is automatically optional, and it must be the only optional argument in the procedure declaration. All preceding arguments must be required.  
  
 **Error ID:** BC30046  
  
### To correct this error  
  
-   Remove the optional arguments in the declaration.  
  
## See Also  
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [ParamArray](../vs140/ParamArray--Visual-Basic-.md)