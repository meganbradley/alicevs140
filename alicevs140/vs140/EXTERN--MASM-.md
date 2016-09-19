---
title: "EXTERN (MASM)"
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
ms.assetid: 667d703d-3aaf-4139-a586-29bc5dab1aff
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EXTERN (MASM)
Defines one or more external variables, labels, or symbols called *name* whose type is `type`.  
  
## Syntax  
  
```  
  
   EXTERN [[langtype]] name [[(altid)]] :  
type [[, [[langtype]] name [[(altid)]] :type]]...  
```  
  
## Remarks  
 The `type` can be [ABS](../vs140/operator-ABS.md), which imports *name* as a constant. Same as [EXTRN](../vs140/EXTRN.md).  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)