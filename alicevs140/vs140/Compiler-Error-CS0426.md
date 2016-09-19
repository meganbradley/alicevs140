---
title: "Compiler Error CS0426"
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
ms.assetid: 62df0deb-3624-436e-9691-ebe3ee1fc31f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0426
The type name 'identifier' does not exist in the type 'type'  
  
 This error occurs when you reference a type nested within another type, but no such nested type exists. This can occur if you mistype the name of the nested type. Check the spelling of the names used, and verify that the enclosing type has the expected member.  
  
 The following sample generates CS0426 because class C has no nested type A:  
  
```  
// CS0426.cs  
  
class C  
{  
    // No nested types are declared.     
}  
  
class D  
{  
   public static void Main()  
   {  
       C c = new C();  
       // Attempt to reference a nested type A:  
       C.A a; // CS0426 because no such type C.A  
   }  
}  
```  
  
## See Also  
 [Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)