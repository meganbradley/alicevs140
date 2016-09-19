---
title: "Compiler Error CS1520"
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
ms.assetid: 1aeeee83-52a6-45dc-b197-a9a6de3a220c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1520
Method must have a return type  
  
 A method that is declared in a class, struct, or interface must have an explicit return type. In the following example, the Square method has a return value of [string](../Topic/string%20\(C%23%20Reference\).md):  
  
```  
class Test  
{  
    string IntToString(int i)  
    {  
        return i.ToString();  
    }  
}  
```  
  
 The following sample generates CS1520:  
  
```  
// CS1520a.cs  
public class x  
{  
   // Method declaration missing a return type  
   MyMethod()   // CS1520     
   {}  
   // Add the desired return type:  
   // void MyMethod2()  
  // { }  
  
   public static void Main()  
   {  
   }  
}  
```  
  
 Alternatively, this error might be encountered when the case of a constructor's name differs from that of the class or struct declaration, as in the following sample. Because the name is not exactly the same as the class name, the compiler interprets it as a regular method, not a constructor, and produces the error:  
  
```  
// CS1520b.cs  
public class Class1  
{  
   // Should be Class1, not class1  
   public class1()   // CS1520  
   {  
   }  
   static void Main()  
   {  
   }  
}  
```  
  
## See Also  
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)   
 [Constructors (C# Programming Guide)](../vs140/Constructors--C#-Programming-Guide-.md)