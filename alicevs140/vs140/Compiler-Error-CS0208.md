---
title: "Compiler Error CS0208"
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
ms.assetid: 03534893-1522-4dab-9822-8b9ed97b3bd0
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0208
Cannot take the address of, get the size of, or declare a pointer to a managed type ('type')  
  
 Even when used with the [unsafe](../vs140/unsafe--C#-Reference-.md) keyword, taking the address of a managed object, getting the size of a managed object, or declaring a pointer to a managed type is not allowed. A managed type is:  
  
-   any reference type  
  
-   any struct that contains a reference type as a field or property  
  
 For more information, see [Unsafe Code and Pointers (C# Programmers Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md) and [sizeof](../vs140/sizeof--C#-Reference-.md).  
  
## Example  
 The following sample generates CS0208:  
  
```  
// CS0208.cs  
// compile with: /unsafe  
  
class myClass  
{  
    public int a = 98;  
}  
  
struct myProblemStruct  
{  
    string s;  
    float f;  
}  
  
struct myGoodStruct  
{  
    int i;  
    float f;  
}  
  
public class MyClass  
{  
    unsafe public static void Main()  
    {  
        // myClass is a class, a managed type.  
        myClass s = new myClass();    
        myClass* s2 = &s;    // CS0208  
  
        // The struct contains a string, a managed type.  
        int i = sizeof(myProblemStruct); //CS0208  
  
        // The struct contains only value types.  
        i = sizeof(myGoodStruct); //OK  
  
    }  
}  
  
```  
  
## See Also  
 [sizeof (C# Reference)](../vs140/sizeof--C#-Reference-.md)