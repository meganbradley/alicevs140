---
title: "Compiler Error CS0752"
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
ms.assetid: f9a373d6-31ed-42db-8206-80cbe9b8c546
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0752
A partial method cannot have out parameters  
  
 A partial method cannot have an [out](../vs140/out--C#-Reference-.md) parameter. Out parameters are not allowed because if the partial method is removed by the compiler then there is no guarantee that the out parameter is ever assigned.  
  
### To correct this error  
  
1.  Remove the out modifier from the parameter and use the return value of the method instead, or else remove the partial modifier from the method declaration.  
  
## Example  
 The following code generates CS0752:  
  
```  
// cs0752.cs  
public partial class C  
{  
    partial void Part(out int num); // CS0752  
    // try the following line instead  
    // partial void Part(int num);  
  
    public static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)