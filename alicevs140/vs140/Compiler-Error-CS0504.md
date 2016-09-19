---
title: "Compiler Error CS0504"
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
ms.topic: error-reference
ms.assetid: f2486ffd-aa85-4b40-a89c-a32530b85d1f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0504
The constant 'variable' cannot be marked static  
  
 If a variable is [const](../vs140/const--C#-Reference-.md), it is also [static](../vs140/static--C#-Reference-.md). If you want a **const** and **static** variable, just declare that variable as **const**; if all you want is a **static** variable, just mark it **static**.  
  
 The following sample generates CS0504:  
  
```  
// CS0504.cs  
namespace x  
{  
   abstract public class clx  
   {  
      static const int i = 0;   // CS0504, cannot be both static and const  
      abstract public void f();  
   }  
}  
```