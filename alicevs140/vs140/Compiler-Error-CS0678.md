---
title: "Compiler Error CS0678"
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
ms.assetid: ca389fc9-da78-4e16-b68c-782f90b17c83
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0678
'variable': a field can not be both volatile and readonly  
  
 Use of the [volatile](../Topic/volatile%20\(C%23%20Reference\).md) and [readonly](../vs140/readonly--C#-Reference-.md) keywords is mutually exclusive.  
  
 The following sample generates CS0678:  
  
```  
// CS0678.cs  
using System;  
  
class TestClass  
{  
   private readonly volatile int i;   // CS0678  
   // try the following line instead  
   // private volatile int i;  
  
   public static void Main()  
   {  
   }  
}  
```