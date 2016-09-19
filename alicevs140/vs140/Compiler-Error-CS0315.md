---
title: "Compiler Error CS0315"
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
ms.assetid: 9bb1cab3-1dca-4467-978b-1ab310901a70
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0315
The type 'valueType' cannot be used as type parameter 'T' in the generic type or method 'TypeorMethod<T\>'. There is no boxing conversion from 'valueType' to 'referenceType'.  
  
 This error occurs when you constrain a generic type to a particular class, and try to construct an instance of that class by using a value type that cannot be implicitly boxed to it.  
  
### To correct this error  
  
1.  One solution is to redefine the struct as a class.  
  
## Example  
 The following example generates CS0315:  
  
```  
// cs0315.cs  
public class ClassConstraint { }  
public struct ViolateClassConstraint { }  
  
public class Gen<T> where T : ClassConstraint  
{         
}  
public class Test  
{  
    public static int Main()  
    {  
        Gen<ViolateClassConstraint> g = new Gen<ViolateClassConstraint>(); //CS0315  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)   
 [Boxing and Unboxing (C# Programming Guide)](../Topic/Boxing%20and%20Unboxing%20\(C%23%20Programming%20Guide\).md)