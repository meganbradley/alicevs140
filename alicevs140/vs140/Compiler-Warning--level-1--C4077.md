---
title: "Compiler Warning (level 1) C4077"
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
ms.assetid: c2d28805-b33f-41ad-afba-33b3f788c649
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4077
unknown check_stack option  
  
 The old form of the **check_stack** pragma is used with an unknown argument. The argument must be `+`, `-`, `(on)`, `(off)`, or empty.  
  
 The compiler ignores the pragma and leaves the stack checking unchanged.  
  
## Example  
  
```  
// C4077.cpp  
// compile with: /W1 /LD  
#pragma check_stack yes // C4077  
#pragma check_stack +    // Correct old form  
#pragma check_stack (on) // Correct new form  
```