---
title: "Compiler Warning (level 1) C4085"
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
ms.assetid: 2bc6eb25-058f-4597-b351-fd69587b5170
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4085
expected pragma parameter to be 'on' or 'off'  
  
 The pragma requires an **on** or **off** parameter. The pragma is ignored.  
  
 The following sample generates C4085:  
  
```  
// C4085.cpp  
// compile with: /W1 /LD  
#pragma optimize( "t", maybe )  // C4085  
```