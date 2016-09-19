---
title: "ML Fatal Error A1011"
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
ms.assetid: 7fbf092d-4189-4330-a884-dfa2268fc3dd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Fatal Error A1011
**directive must be in control block**  
  
 The assembler found a high-level directive where one was not expected. One of the following directives was found:  
  
-   [.ELSE](../vs140/.ELSE.md) without [.IF](../vs140/.IF.md)  
  
-   [.ENDIF](../vs140/.ENDIF.md) without [.IF](../vs140/.IF.md)  
  
-   [.ENDW](../vs140/.ENDW.md) without [.WHILE](../vs140/.WHILE.md)  
  
-   [.UNTILCXZ](../vs140/.UNTILCXZ.md) without [.REPEAT](../vs140/.REPEAT.md)  
  
-   [.CONTINUE](../vs140/.CONTINUE.md) without [.WHILE](../vs140/.WHILE.md) or [.REPEAT](../vs140/.REPEAT.md)  
  
-   [.BREAK](../vs140/.BREAK.md) without [.WHILE](../vs140/.WHILE.md) or [.REPEAT](../vs140/.REPEAT.md)  
  
-   [.ELSE](../vs140/.ELSE.md) following `.ELSE`  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)