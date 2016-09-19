---
title: "Compiler Error CS0754"
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
ms.assetid: c83e04b5-6ab5-45c2-805e-0ba4f041d506
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0754
A partial method may not explicitly implement an interface method.  
  
 A partial method cannot be declared as an explicit implementation of a method defined in an interface.  
  
### To correct this error  
  
1.  Remove the explicit interface qualification from the method declaration.  
  
## Example  
 The following code generates CS0754:  
  
```  
// cs0754.cs  
using System;  
  
    public interface IF  
    {  
        void Part();  
    }  
  
    public partial class C : IF  
    {  
        partial void IF.Part(); //CS0754  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```  
  
## See Also  
 [Explicit Interface Implementation (C# Programming Guide)](../vs140/Explicit-Interface-Implementation--C#-Programming-Guide-.md)   
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)