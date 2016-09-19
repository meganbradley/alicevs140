---
title: "Compiler Error CS1628"
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
ms.assetid: 520f864c-afe3-4db2-b44e-cfaac28ff49d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1628
Cannot use ref or out parameter 'parameter' inside an anonymous method, lambda expression, or query expression  
  
 This error occurs if you use a ref or out parameter inside an anonymous method block. To avoid this error, use a local variable or some other construct.  
  
 The following sample generates CS1628:  
  
```  
// CS1628.cs  
  
delegate int MyDelegate();  
  
class C  
{  
  public static void F(ref int i)  
  {  
      MyDelegate d = delegate { return i; };  // CS1628  
      // Try this instead:  
      // int tmp = i;  
      // MyDelegate d = delegate { return tmp; };  
  }  
  
  public static void Main()  
  {  
  
  }  
}  
```