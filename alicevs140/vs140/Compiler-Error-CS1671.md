---
title: "Compiler Error CS1671"
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
ms.assetid: 34255d2b-6ff6-4ac1-b617-3199e16726cf
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1671
A namespace declaration cannot have modifiers or attributes  
  
 Modifiers are not meaningful when applied to a namespace, so they are not allowed.  
  
 The following sample generates CS1671:  
  
```  
// CS1671.cs  
public namespace NS // CS1671  
{  
  
}  
```