---
title: "How to: Convert an Object to Another Type in Visual Basic"
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
ms.assetid: 60cb5fc7-7ba4-4ab5-9c24-480fa12ddcdc
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert an Object to Another Type in Visual Basic
You convert an `Object` variable to another data type by using a conversion keyword such as [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md).  
  
## Example  
 The following example converts an `Object` variable to an `Integer` and a `String`.  
  
```  
Public Sub objectConversion(ByVal anObject As Object)  
    Dim anInteger As Integer  
    Dim aString As String  
    anInteger = CType(anObject, Integer)  
    aString = CType(anObject, String)  
End Sub  
```  
  
 If you know that the contents of an `Object` variable are of a particular data type, it is better to convert the variable to that data type. If you continue to use the `Object` variable, you incur either *boxing* and *unboxing* (for a value type) or *late binding* (for a reference type). These operations all take extra execution time and make your performance slower.  
  
## Compiling the Code  
 This example requires:  
  
-   A reference to the <xref:System?qualifyHint=True> namespace.  
  
## See Also  
 <xref:System.Object?qualifyHint=False>   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Conversions Between Strings and Other Types](../vs140/Conversions-Between-Strings-and-Other-Types--Visual-Basic-.md)   
 [Array Conversions](../Topic/Array%20Conversions%20\(Visual%20Basic\).md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)