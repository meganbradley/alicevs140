---
title: "Compiler Error CS1537"
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
ms.assetid: fdc17f3e-05b3-4d04-8825-4563aec816f5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1537
The using alias 'alias' appeared previously in this namespace  
  
 You defined a symbol twice as an alias for a namespace. A symbol can only be defined once.  
  
 The following sample generates CS1537:  
  
```  
// CS1537.cs  
namespace x  
{  
   using System;  
   using Object = System.Object;  
   using Object = System.Object;   // CS1537, delete this line to resolve  
   using System = System;  
}  
```