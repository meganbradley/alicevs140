---
title: "ML Warning A4012"
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
ms.assetid: 842b1259-9679-4eeb-a02d-672a583a94e5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ML Warning A4012
**line number information for segment without class 'CODE'**  
  
 There were instructions in a segment that did not have a class name that ends with "CODE." The assembler did not generate CodeView information for these instructions.  
  
 CodeView cannot process modules with code in segments with class names that do not end with "CODE."  
  
## See Also  
 [ML Error Messages](../vs140/ML-Error-Messages.md)