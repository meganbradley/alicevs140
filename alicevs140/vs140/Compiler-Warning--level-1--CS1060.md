---
title: "Compiler Warning (level 1) CS1060"
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
ms.assetid: af389239-672b-449e-84b5-edb52e320013
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1060
Use of possibly unassigned field 'name'. Struct instance variables are initially unassigned if struct is unassigned.  
  
 Struct members are initialized to their default value if you do not explicitly initialize them. The default value for class types (and other reference types) is null. If the class is not initialized before any attempt to access it, a `NullReferenceException` will be thrown at runtime. The compiler cannot determine definitively whether the class member will be initialized or not, and so CS1060 is a warning and not an error.  
  
### To correct this error  
  
1.  Provide a constructor for the `struct` that initializes all its members.  
  
## Example  
 The following code generates CS1060 because the class type `U` is a member of the `struct S` but is never initialized.  
  
```  
// cs1060.cs  
namespace CS1060  
{      
    public class U  
    {  
        public int i;  
    }  
  
    public struct S  
    {  
        public U u;  
        // Add constructor to correct the error.  
        //public S(int val)  
        //{  
        //    u = new U() { i = val };  
        //}  
    }  
    public class Test  
    {  
        static void Main()  
        {  
            S s;  
            s.u.i = 5;  // CS1060  
  
            //Try these lines instead, and uncomment the constructor in S  
            // S s = new S(0);  
            // s.u.i = 5;  
  
        }  
    }    
}  
```  
  
## See Also  
 [Structs (C# Programming Guide)](../vs140/Structs--C#-Programming-Guide-.md)