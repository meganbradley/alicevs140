---
title: "Compiler Error C2963"
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
ms.assetid: 5f606f7d-7941-4b20-af77-d682d3464be7
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2963
string literals are not permitted as parameter to a template specialization  
  
 One or more of the template parameter expressions is a string literal.  
  
 This error may be fixed if you use a pointer to a string variable.