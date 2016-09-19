---
title: "Compiler Warning (level 1) C4550"
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
ms.assetid: f902b4ed-5f17-48ea-b693-92f4fb8c8054
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4550
expression evaluates to a function which is missing an argument list  
  
 A dereferenced pointer to a function is missing an argument list.  
  
## Example  
  
```  
// C4550.cpp  
// compile with: /W1  
bool f()  
{  
   return true;  
}  
  
typedef bool (*pf_t)();  
  
int main()  
{  
   pf_t pf = f;  
   if (*pf) {}  // C4550  
   return 0;  
}  
```