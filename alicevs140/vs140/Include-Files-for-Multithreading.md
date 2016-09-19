---
title: "Include Files for Multithreading"
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
ms.assetid: 98d764f9-71f4-4da5-8f3a-8d2d26e96799
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Include Files for Multithreading
Standard include files declare C run-time library functions as they are implemented in the libraries. If you use the [Full Optimization](../vs140/-Ox--Full-Optimization-.md) (/Ox) or [fastcall Calling Convention](../Topic/-Gd,%20-Gr,%20-Gv,%20-Gz%20\(Calling%20Convention\).md) (/Gr) option, the compiler assumes that all functions should be called using the register calling convention. The run-time library functions were compiled using the C calling convention, and the declarations in the standard include files tell the compiler to generate correct external references to these functions.  
  
## See Also  
 [Multithreading with C and Win32](../vs140/Multithreading-with-C-and-Win32.md)