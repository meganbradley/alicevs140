---
title: "Compiler Error CS0447"
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
ms.assetid: a25486c5-e9bf-4528-8533-c1aaab22ace0
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0447
Attributes cannot be used on type arguments, only on type parameters  
  
 This error occurs when you apply an attribute to a type argument that occurs in an invocation statement. It is acceptable to apply an attribute to a type parameter in a class or method declaration statement such as the following:  
  
```  
class C<[some attribute] T> {…}  
```  
  
 The following line of code will generate this error. It is assumed that the class `C`, defined in the previous line of code, has a static method called `MyStaticMethod`.  
  
```  
C<[some attribute] T>.MyStaticMethod();  
```  
  
## Example  
 The following code generates error CS0447.  
  
```  
// CS0447.cs  
using System;  
namespace Test41  
{  
    public interface I<A>   
    {  
        void Meth<B>();  
    }  
    public class B : I<int>   
    {  
        void I<[Test] int>.Meth<X>() { }  // CS0447  
    }  
}  
```