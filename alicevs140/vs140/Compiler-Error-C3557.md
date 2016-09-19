---
title: "Compiler Error C3557"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94c579f4-17b5-443f-87a5-3fc7165f57da
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3557
a function cannot have both a return type and a late-specified return type  
  
 A function can have either a return type or a late-specified return type, but not both. For example, the following declaration yields error C3557.  
  
```  
int f()->int; // C3557  
```