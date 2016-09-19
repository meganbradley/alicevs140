---
title: "Compiler Warning (level 4) C4032"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 70dd0c85-0239-43f9-bb06-507f6a57d206
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4032
formal parameter 'number' has different type when promoted  
  
 The parameter type is not compatible, through default promotions, with the type in a previous declaration.  
  
 This is an error in ANSI C ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)) and a warning under Microsoft extensions (/Ze).  
  
## Example  
  
```  
// C4032.c  
// compile with: /W4  
void func();  
void func(char);   // C4032, char promotes to int  
  
int main()  
{  
}  
```