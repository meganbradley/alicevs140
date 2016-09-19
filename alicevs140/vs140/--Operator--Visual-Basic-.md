---
title: "* Operator (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b210382-99da-4195-89ba-b1d06f5e89ad
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# * Operator (Visual Basic)
Multiplies two numbers.  
  
## Syntax  
  
```  
  
number1 * number2  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`number1`|Required. Any numeric expression.|  
|`number2`|Required. Any numeric expression.|  
  
## Result  
 The result is the product of `number1` and `number2`.  
  
## Supported Types  
 All numeric types, including the unsigned and floating-point types and `Decimal`.  
  
## Remarks  
 The data type of the result depends on the types of the operands. The following table shows how the data type of the result is determined.  
  
|||  
|-|-|  
|Operand data types|Result data type|  
|Both expressions are integral data types ([SByte](../Topic/SByte%20Data%20Type%20\(Visual%20Basic\).md), [Byte](../vs140/Byte-Data-Type--Visual-Basic-.md), [Short](../Topic/Short%20Data%20Type%20\(Visual%20Basic\).md), [UShort](../Topic/UShort%20Data%20Type%20\(Visual%20Basic\).md), [Integer](../vs140/Integer-Data-Type--Visual-Basic-.md), [UInteger](../vs140/UInteger-Data-Type.md), [Long](../Topic/Long%20Data%20Type%20\(Visual%20Basic\).md), [ULong](../vs140/ULong-Data-Type--Visual-Basic-.md))|A numeric data type appropriate for the data types of `number1` and `number2`. See the "Integer Arithmetic" tables in [Data Types of Operator Results](../Topic/Data%20Types%20of%20Operator%20Results%20\(Visual%20Basic\).md).|  
|Both expressions are [Decimal](../vs140/Decimal-Data-Type--Visual-Basic-.md)|`Decimal`|  
|Both expressions are [Single](../Topic/Single%20Data%20Type%20\(Visual%20Basic\).md)|`Single`|  
|Either expression is a floating-point data type (`Single` or [Double](../Topic/Double%20Data%20Type%20\(Visual%20Basic\).md)) but not both `Single` (note `Decimal` is not a floating-point data type)|`Double`|  
  
 If an expression evaluates to [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md), it is treated as zero.  
  
## Overloading  
 The `*` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. If your code uses this operator on such a class or structure, be sure you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 This example uses the `*` operator to multiply two numbers. The result is the product of the two operands.  
  
 [!CODE [VbVbalrOperators#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#4)]  
  
## See Also  
 [*= Operator](../vs140/-=-Operator--Visual-Basic-.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Arithmetic Operators in Visual Basic](../Topic/Arithmetic%20Operators%20in%20Visual%20Basic.md)