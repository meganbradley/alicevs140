---
title: "Compiler Error CS0704"
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
ms.assetid: a16ae7f3-11e0-45f3-ac40-91a853eea4e5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0704
Cannot do member lookup in 'type' because it is a type parameter  
  
 An inner type cannot be specified through a type parameter. Try using the desired type explicitly.  
  
## Example  
 The following sample generates CS0704:  
  
```  
// CS0704.cs  
class B  
{  
    public class I { }  
}  
  
class C<T> where T : B  
{  
    T.I f;  // CS0704 – member lookup on type parameter  
    // Try this instead:  
    // B.I f;  
}  
  
class CMain  
{  
    public static void Main() {}  
}  
```