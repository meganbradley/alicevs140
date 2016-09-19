---
title: "Floating-Point Support for Older Code (Visual C++)"
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
ms.assetid: a2a26b96-7bc2-418a-981a-51aa1a0294a2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Floating-Point Support for Older Code (Visual C++)
The MMX and floating-point stack registers (MM0-MM7/ST0-ST7) are preserved across context switches.  There is no explicit calling convention for these registers.  The use of these registers is strictly prohibited in kernel mode code.  
  
## See Also  
 [Calling Convention](../vs140/Calling-Convention.md)