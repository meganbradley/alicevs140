---
title: "Default Values Table (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4af2c1df-9e3a-48c1-83ac-b192986fc5bc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Default Values Table (C# Reference)
The following table shows the default values of value types returned by the default constructors. Default constructors are invoked by using the `new` operator, as follows:  
  
```  
int myInt = new int();  
```  
  
 The preceding statement has the same effect as the following statement:  
  
```  
int myInt = 0;  
```  
  
 Remember that using uninitialized variables in C# is not allowed.  
  
|Value type|Default value|  
|----------------|-------------------|  
|[bool](../Topic/bool%20\(C%23%20Reference\).md)|`false`|  
|[byte](../Topic/byte%20\(C%23%20Reference\).md)|0|  
|[char](../vs140/char--C#-Reference-.md)|'\0'|  
|[decimal](../Topic/decimal%20\(C%23%20Reference\).md)|0.0M|  
|[double](../vs140/double--C#-Reference-.md)|0.0D|  
|[enum](../Topic/enum%20\(C%23%20Reference\).md)|The value produced by the expression (E)0, where E is the enum identifier.|  
|[float](../vs140/float--C#-Reference-.md)|0.0F|  
|[int](../Topic/int%20\(C%23%20Reference\).md)|0|  
|[long](../vs140/long--C#-Reference-.md)|0L|  
|[sbyte](../Topic/sbyte%20\(C%23%20Reference\).md)|0|  
|[short](../Topic/short%20\(C%23%20Reference\).md)|0|  
|[struct](../vs140/struct--C#-Reference-.md)|The value produced by setting all value-type fields to their default values and all reference-type fields to `null`.|  
|[uint](../Topic/uint%20\(C%23%20Reference\).md)|0|  
|[ulong](../Topic/ulong%20\(C%23%20Reference\).md)|0|  
|[ushort](../Topic/ushort%20\(C%23%20Reference\).md)|0|  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Value Types Table (C# Reference)](../vs140/Value-Types-Table--C#-Reference-.md)   
 [Value Types](../Topic/Value%20Types%20\(C%23%20Reference\).md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Reference Tables for Types](../vs140/Reference-Tables-for-Types--C#-Reference-.md)