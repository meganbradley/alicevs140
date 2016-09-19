---
title: "ML Fatal Error A1008"
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
ms.assetid: fe592f9d-c37b-4cd8-a51d-e3c15ddcab83
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Fatal Error A1008
**unmatched macro nesting**  
  
 Either a macro was not terminated before the end of the file or the terminating directive [ENDM](../vs140/ENDM.md) was found outside of a macro block.  
  
 One cause of this error is omission of the dot before [.REPEAT](../vs140/.REPEAT.md) or [.WHILE](../vs140/.WHILE.md).  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)