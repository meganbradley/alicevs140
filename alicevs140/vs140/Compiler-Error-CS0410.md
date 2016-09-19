---
title: "Compiler Error CS0410"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8b11042-9119-465e-abf6-235cbc7b8db5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0410
No overload for 'method' has the correct parameter and return types  
  
 This error occurs if you try to instantiate a delegate with a function that has the wrong parameter types. The parameter types of the delegate must match the function that you are assigning to the delegate.  
  
## Example  
 The following example generates CS0410:  
  
```  
// CS0410.cs  
// compile with: /langversion:ISO-1  
  
class Test  
{  
    delegate void D(double d );  
    static void F(int i) { }  
  
    static void Main()  
    {  
        D d = new D(F);  // CS0410  
    }  
}  
```