---
title: "C Assignment Operators"
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
ms.assetid: 11688dcb-c941-44e7-a636-3fc98e7dac40
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Assignment Operators
An assignment operation assigns the value of the right-hand operand to the storage location named by the left-hand operand. Therefore, the left-hand operand of an assignment operation must be a modifiable l-value. After the assignment, an assignment expression has the value of the left operand but is not an l-value.  
  
 **Syntax**  
  
 *assignment-expression*:  
 *conditional-expression*  
  
 *unary-expression assignment-operator assignment-expression*  
  
 *assignment-operator*: one of  
 **= \*=** `/=` `%=` `+=` **–= <<= >>= &=** `^=` `|=`  
  
 The assignment operators in C can both transform and assign values in a single operation. C provides the following assignment operators:  
  
|Operator|Operation Performed|  
|--------------|-------------------------|  
|**=**|Simple assignment|  
|**\*=**|Multiplication assignment|  
|`/=`|Division assignment|  
|`%=`|Remainder assignment|  
|`+=`|Addition assignment|  
|**–=**|Subtraction assignment|  
|**<<=**|Left-shift assignment|  
|**>>=**|Right-shift assignment|  
|**&=**|Bitwise-AND assignment|  
|`^=`|Bitwise-exclusive-OR assignment|  
|`&#124;=`|Bitwise-inclusive-OR assignment|  
  
 In assignment, the type of the right-hand value is converted to the type of the left-hand value, and the value is stored in the left operand after the assignment has taken place. The left operand must not be an array, a function, or a constant. The specific conversion path, which depends on the two types, is outlined in detail in [Type Conversions](../vs140/Type-Conversions--C-.md).  
  
## See Also  
 [Assignment Operators](../vs140/Assignment-Operators.md)