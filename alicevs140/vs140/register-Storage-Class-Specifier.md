---
title: "register Storage-Class Specifier"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7577bf48-88ec-4191-873c-ef4217a4034e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# register Storage-Class Specifier
**Microsoft Specific**  
  
 The Microsoft C/C++ compiler does not honor user requests for register variables. However, for portability all other semantics associated with the **register** keyword are honored by the compiler. For example, you cannot apply the unary address-of operator (**&**) to a register object nor can the **register** keyword be used on arrays.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Storage-Class Specifiers for Internal-Level Declarations](../vs140/Storage-Class-Specifiers-for-Internal-Level-Declarations.md)