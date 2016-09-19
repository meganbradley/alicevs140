---
title: "Compiler Error CS0702"
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
ms.assetid: 55952b5b-66a6-4c53-ac53-2e90a363c335
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0702
Constraint cannot be special class 'identifier'  
  
 The following types may not be used as constraints:  `System.Object,``System.Array`, `System.Delegate`, `System.Enum`, or `System.ValueType`.  
  
## Example  
 The following sample generates CS0702:  
  
```  
// CS0702.cs  
class C<T> where T : System.Array  // CS0702  
{  
}  
```  
  
## See Also  
 [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)