---
title: "Compiler Error CS0534"
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
ms.assetid: 39fde9d1-3041-41fc-9dc2-43394c13c6c9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0534
'function1' does not implement inherited abstract member 'function2'  
  
 A class is required to implement all the [abstract](../vs140/abstract--C#-Reference-.md) members in the base class, unless the class is also abstract.  
  
 The following sample generates CS0534:  
  
```  
// CS0534.cs  
namespace x  
{  
   abstract public class clx  
   {  
      public abstract void f();  
   }  
  
   public class cly : clx   // CS0534, no override for clx::f  
   {  
      // uncomment the following sample override to resolve CS0534  
      // override public void f()  
      // {  
      // }  
  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```