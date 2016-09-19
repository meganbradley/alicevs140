---
title: "Compiler Error CS1113"
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
ms.assetid: ef2d828f-b5ee-4be9-ba2e-36df5502cc5a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1113
Extension methods 'name' defined on value type 'name' cannot be used to create delegates.  
  
 Extension methods that are defined for class types can be used to create delegates. Extension methods that are defined for value types cannot.  
  
### To correct this error  
  
1.  Associate the extension method with a class type.  
  
2.  Make the method a regular method on the struct.  
  
## Example  
 The following example generates CS1113:  
  
```  
// cs1113.cs  
using System;  
public static class Extensions  
{  
    public static S ExtMethod(this S s)  
    {  
        return s;  
    }  
}  
  
public struct S  
{  
}  
  
public class Test  
{  
    static int Main()  
    {  
        Func<S> f = new S().ExtMethod; // CS1113  
        return 1;  
    }  
}  
  
```  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)