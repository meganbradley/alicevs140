---
title: "Compiler Error CS0757"
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
ms.assetid: ba093570-306d-4b7b-aad5-1a3855ad6776
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0757
A partial method may not have multiple implementing declarations.  
  
 A partial method consists of exactly one defining declaration (signature) and one or zero implementing declarations (body). Multiple implementing declarations for the same identical defining declarations are not allowed. Partial methods may be overloaded, and each overloaded version may have one or zero implementing declarations.  
  
### To correct this error  
  
1.  Remove all except one of the implementing declarations for the partial method.  
  
## Example  
 The following example generates CS0757:  
  
```  
// cs0757.cs  
using System;  
  
    public partial class C  
    {  
        // Defining declaration.  
        partial void Part();  
  
        // Implementing declaration.  
        partial void Part()  
        {  
            //...Do something.  
        }  
  
        // Second implementing declaration.  
        partial void Part() // CS0757  
        {  
            //...Do something.  
        }  
  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```  
  
## See Also  
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)