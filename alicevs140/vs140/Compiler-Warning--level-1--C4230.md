---
title: "Compiler Warning (level 1) C4230"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: a4be8729-74b6-44df-a5ea-e3f45aad0f8f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4230
anachronism used : modifiers/qualifiers interspersed; qualifier ignored  
  
 Using a qualifier before a Microsoft modifier such as `__cdecl` is an outdated practice.  
  
## Example  
  
```  
// C4230.cpp  
// compile with: /W1 /LD  
int __cdecl const function1();   // C4230 const ignored  
```