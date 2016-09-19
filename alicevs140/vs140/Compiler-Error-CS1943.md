---
title: "Compiler Error CS1943"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: eb3e36b7-1372-471c-8cfb-a955a86c379e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1943
An expression of type 'type' is not allowed in a subsequent from clause in a query expression with source type 'type'. Type inference failed in the call to 'method'.  
  
 All range variables must represent queryable types.  
  
### To correct this error  
  
1.  Make sure that the type is a queryable type that implements `IEnumerable`, `IEnumerable<T>` or a derived interface, or any other type which has a query pattern defined for it.  
  
2.  If the type is a non-generic `IEnumerable`, provide an explicit type on the range variable.  
  
## Example  
 The following code generates CS1943:  
  
```  
// cs1943.cs  
using System.Linq;  
class Test  
{  
    class TestClass  
    { }  
    static void Main()  
    {  
        int[] nums = { 0, 1, 2, 3, 4, 5 };  
        TestClass tc = new TestClass();  
  
        var x = from n in nums  
                from s in tc // CS1943  
                select n + s;  
    }  
}  
```