---
title: "Compiler Error CS1928"
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
ms.assetid: bcc9dbef-ded5-4ddd-8c03-a9837cb6d165
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1928
'Type' does not contain a definition for 'method' and the best extension method overload 'method' has some invalid arguments.  
  
 This error is produced when the compiler cannot find a class member with the name of the method you have called. It can find an extension method with that name, but not with a signature that matches the types you passed in with your method call.  
  
### To correct this error  
  
1.  Pass in types that match an existing extension method or class method.  
  
## Example  
 The following code generates CS1928:  
  
```  
// cs1928.cs  
class Test  
{  
    static void Main()  
    {  
        Test t = new Test();  
        t.M("hi"); // CS1928  
    }  
}  
static class Ext  
{  
    public static void M(this Test t, int i)  
    {  
    }  
}  
```  
  
 This error is often accompanied by CS1503: Argument 'n': cannot convert from 'typeA' to 'typeB'.  
  
## See Also  
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)