---
title: "Compiler Error CS1663"
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
ms.assetid: 013f36ac-8925-4cee-9008-54fa7ad1324b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1663
Fixed size buffer type must be one of the following: bool, byte, short, int, long, char, sbyte, ushort, uint, ulong, float or double  
  
 A fixed sized buffer may not be any type other than those listed. To avoid this error, use another type or do not use a fixed array.  
  
## Example  
 The following sample generates CS1663.  
  
```  
// CS1663.cs  
// compile with: /unsafe /target:library  
  
unsafe struct C  
{  
   fixed string ab[10];   // CS1663  
}  
```