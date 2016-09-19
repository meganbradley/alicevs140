---
title: "Option Strict On disallows late binding"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9da4b826-2e12-4a5d-9e17-762b0b68fc9b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On disallows late binding
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] allows implicit conversions of any data type to any other data type. However, data loss can occur if the value of one data type is converted to a data type with less precision or a smaller capacity. `Option Strict On` ensures compile-time notification of these types of conversions so they may be avoided. You cannot use `Option Strict On` with late binding.  
  
 The following code example uses late binding and causes this error when `Option Strict` is set to `On`.  
  
 [!CODE [VbVbalrOptionStrictError#1](VbVbalrOptionStrictError#1)]  
  
 **Error ID:** BC30574  
  
### To correct this error  
  
-   Modify the object declaration to use an explicit type, as shown in the following example:  
  
     [!CODE [VbVbalrOptionStrictError#2](VbVbalrOptionStrictError#2)]  
  
 \- or -  
  
-   Modify the late-bound expression to specify an explicit type, as shown in the following example:  
  
     [!CODE [VbVbalrOptionStrictError#3](VbVbalrOptionStrictError#3)]  
  
 \- or -  
  
-   Let the compiler infer a specific type, as shown in the following example:  
  
     [!CODE [VbVbalrOptionStrictError#4](VbVbalrOptionStrictError#4)]  
  
 \- or -  
  
-   Turn `Option Strict` off by removing the word `On` after it or by explicitly specifying `Off`.  
  
## See Also  
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Option Strict Statement](../vs140/Option-Strict-Statement.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)