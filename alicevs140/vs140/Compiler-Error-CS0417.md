---
title: "Compiler Error CS0417"
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
ms.topic: error-reference
ms.assetid: e2a617da-f0b2-4bad-aefa-3dd3bc1fb24b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0417
'identifier': cannot provide arguments when creating an instance of a variable type  
  
 This error occurs if a call to the `new` operator on a type parameter has arguments. The only constructor that can be called by using the `new` operator on an unknown parameter type is a constructor that has no arguments. If you need to call another constructor, consider using a class type constraint or interface constraint.  
  
## Example  
 The following example generates CS0417:  
  
```c#  
// CS0417  
class ExampleClass<T> where T : new()  
{  
    // The following line causes CS0417.  
    T instance1 = new T(1);     
  
    // The following line doesn't cause the error.  
    T instance2 = new T();  
}  
  
```  
  
## See Also  
 [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)