---
title: "Compiler Error CS2007"
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
ms.assetid: 9be20e8e-2424-4435-9371-778fb12823c0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2007
Unrecognized command-line option: 'option'  
  
 The compiler was passed a string that was not a [compiler option](../vs140/C#-Compiler-Options.md), even though it began with a forward slash (/).  
  
 The following sample generates CS2007:  
  
```  
// CS2007.cs  
// compile with: /recur  
// CS2007 expected  
class x  
{  
   public static void Main() {}  
}  
```