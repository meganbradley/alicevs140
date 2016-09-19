---
title: "ML Fatal Error A1007"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcf9c826-beb3-4e93-91fe-1ffd34995fbf
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Fatal Error A1007
**nesting level too deep**  
  
 The assembler reached its nesting limit. The limit is 20 levels except where noted otherwise.  
  
 One of the following was nested too deeply:  
  
-   A high-level directive such as [.IF](../vs140/.IF.md), [.REPEAT](../vs140/.REPEAT.md), or [.WHILE](../vs140/.WHILE.md).  
  
-   A structure definition.  
  
-   A conditional-assembly directive.  
  
-   A procedure definition.  
  
-   A [PUSHCONTEXT](../vs140/PUSHCONTEXT.md) directive (the limit is 10).  
  
-   A segment definition.  
  
-   An include file.  
  
-   A macro.  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)