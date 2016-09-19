---
title: "Compiler Error CS1666"
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
ms.assetid: 4d62aa9c-71b9-4c6e-8141-2426d20ac243
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1666
You cannot use fixed size buffers contained in unfixed expressions. Try using the fixed statement.  
  
 This error occurs if you use the fixed sized buffer in an expression involving a class that is not itself fixed. The runtime is free to move the unfixed class around to optimize memory access, which could lead to errors when using the fixed sized buffer. To avoid this error, use the `fixed` keyword on the statement.  
  
## Example  
 The following sample generates CS1666.  
  
```  
// CS1666.cs  
// compile with: /unsafe /target:library  
unsafe struct S  
{  
   public fixed int buffer[1];  
}  
  
unsafe class Test  
{  
   S field = new S();  
  
   private bool example1()  
   {  
      return (field.buffer[0] == 0);   // CS1666 error  
   }  
  
   private bool example2()  
   {  
      // OK  
      fixed (S* p = &field)  
      {  
         return (p->buffer[0] == 0);  
      }  
   }  
  
   private bool example3()  
   {  
      S local = new S();  
      return (local.buffer[0] == 0);   
   }   
}  
```