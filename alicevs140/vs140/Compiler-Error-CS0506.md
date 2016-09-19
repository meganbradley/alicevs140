---
title: "Compiler Error CS0506"
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
ms.assetid: 1286957c-2505-4b5f-ade0-154ad5f09dc1
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0506
'function1' : cannot override inherited member 'function2' because it is not marked "virtual", "abstract", or "override"  
  
 A method was overridden that was not explicitly marked as **virtual**, **abstract**, or `override`.  
  
 The following sample generates CS0506:  
  
```  
// CS0506.cs  
namespace MyNameSpace  
{  
   abstract public class ClassX  
   {  
      public int i = 0;  
  
      public int f()  
      {  
         return 0;  
      }  
      // Try the following definition for f() instead:  
      // abstract public int f();  
   }  
  
   public class ClassY : ClassX  
   {  
      public override int f()   // CS0506  
      {  
         return 0;  
      }  
  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```