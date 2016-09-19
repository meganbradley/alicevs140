---
title: "Named argument cannot match a ParamArray parameter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aff179af-96f2-4157-971e-881d8e08f5f2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Named argument cannot match a ParamArray parameter
You have supplied a named argument (specified with the argument's declared name followed by a colon and an equal sign, followed by the argument value); however you cannot pass a parameter array by name. When you call the procedure, you supply an indefinite number of comma-separated arguments for the parameter array, and the compiler cannot associate more than one argument with a single name.  
  
 **Error ID:** BC30587  
  
### To correct this error  
  
-   Pass the argument by position, rather than by name.  
  
## See Also  
 [ParamArray](../vs140/ParamArray--Visual-Basic-.md)   
 [Passing Arguments by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)