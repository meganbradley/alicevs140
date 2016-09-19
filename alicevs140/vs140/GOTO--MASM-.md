---
title: "GOTO (MASM)"
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
ms.assetid: 6a5f73e7-6784-4eae-ac52-4fc77a7f369f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GOTO (MASM)
Transfers assembly to the line marked **:***macrolabel*.  
  
## Syntax  
  
```  
  
GOTO   
macrolabel  
  
```  
  
## Remarks  
 **GOTO** is permitted only inside [MACRO](../vs140/MACRO.md), [FOR](../vs140/FOR--MASM-.md), [FORC](../vs140/FORC.md), [REPEAT](../vs140/REPEAT.md), and **WHILE** blocks. The label must be the only directive on the line and must be preceded by a leading colon.  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)