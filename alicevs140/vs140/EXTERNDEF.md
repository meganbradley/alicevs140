---
title: "EXTERNDEF"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95a10de6-c345-4428-a2f2-90f7d411dc86
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EXTERNDEF
Defines one or more external variables, labels, or symbols called *name* whose type is `type`.  
  
## Syntax  
  
```  
  
EXTERNDEF [[langtype]] name:type [[, [[langtype]] name:type]]...  
```  
  
## Remarks  
 If *name* is defined in the module, it is treated as [PUBLIC](../vs140/PUBLIC--MASM-.md). If *name* is referenced in the module, it is treated as [EXTERN](../vs140/EXTERN--MASM-.md). If *name* is not referenced, it is ignored. The `type` can be [ABS](../vs140/operator-ABS.md), which imports *name* as a constant. Normally used in include files.  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)