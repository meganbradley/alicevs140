---
title: "ML Fatal Error A1010"
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
ms.assetid: 9e0b5241-67f4-4740-8701-3b2d2d1ad9e4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Fatal Error A1010
**unmatched block nesting :**  
  
 A block beginning did not have a matching end, or a block end did not have a matching beginning. One of the following may be involved:  
  
-   A high-level directive such as [.IF](../vs140/.IF.md), [.REPEAT](../vs140/.REPEAT.md), or [.WHILE](../vs140/.WHILE.md).  
  
-   A conditional-assembly directive such as [IF](../vs140/IF--MASM-.md), [REPEAT](../vs140/REPEAT.md), or **WHILE**.  
  
-   A structure or union definition.  
  
-   A procedure definition.  
  
-   A segment definition.  
  
-   A [POPCONTEXT](../vs140/POPCONTEXT.md) directive.  
  
-   A conditional-assembly directive, such as an [ELSE](../vs140/ELSE--MASM-.md), [ELSEIF](../vs140/ELSEIF--MASM-.md), or **ENDIF** without a matching [IF](../vs140/IF--MASM-.md).  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)