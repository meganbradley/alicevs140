---
title: "Compiler Error CS1681"
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
ms.assetid: 99934e15-1db8-4b71-9da8-a681a1d47407
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1681
You cannot redefine the global extern alias  
  
 The global alias is already defined to include all unaliased references and therefore cannot be redefined.  
  
## Example  
 The following sample generates CS1681.  
  
```  
// CS1681.cs  
// compile with: /reference:global=System.dll  
// CS1681 expected  
  
// try this instead: /reference:System.dll  
class A  
{  
   static void Main() {}  
}  
```