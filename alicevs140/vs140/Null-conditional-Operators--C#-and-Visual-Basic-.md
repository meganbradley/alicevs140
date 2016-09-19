---
title: "Null-conditional Operators (C# and Visual Basic)"
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
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Null-conditional Operators (C# and Visual Basic)
Used to test for null before performing a member access (`?.`) or index (`?[`) operation.  These operators help you write less code to handle null checks, especially for descending into data structures.  
  
```c#  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
  
```  
  
```vb  
Dim length = customers?.Length  ‘’ null if customers is null  
Dim first as Customer = customers?(0);  ‘’ null if customers is null  
Dim count as Integer? = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
  
```  
  
 The last example demonstrates that the null-condition operators are short-circuiting.  If one operation in a chain of conditional member access and index operation returns null, then the rest of the chain’s execution stops.  Other operations with lower precedence in the expression continue.  For example, `E` in the following always executes, and the `??` and `==` operations execute.  
  
```vb-c#  
A?.B?.C?[0] ?? E  
A?.B?.C?[0] == E  
  
```  
  
 Another use for the null-condition member access is invoking delegates in a thread-safe way with much less code.  The old way requires code like the following:  
  
```c#  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…)  
  
```  
  
```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
  
```  
  
 The new way is much simpler:  
  
```vb-c#  
PropertyChanged?.Invoke(e)  
  
```  
  
 The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in temporary variable.  
  
 You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.  There were too many ambiguous parsing situations to allow it.  
  
## Language Specifications  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
 For more information, see the [Visual Basic Language Reference](../Topic/Visual%20Basic%20Language%20Reference.md).  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Visual Basic Language Reference](../Topic/Visual%20Basic%20Language%20Reference.md)   
 [Visual Basic Programming Guide](../vs140/Visual-Basic-Programming-Guide.md)