---
title: "Compiler Warning (level 4) C4204"
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
ms.assetid: 298d2880-6737-448e-b711-15572d540200
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4204
nonstandard extension used : non-constant aggregate initializer  
  
 With Microsoft extensions (/Ze), you can initialize aggregate types (arrays, structures, unions, and classes) with values that are not constants.  
  
## Example  
  
```  
// C4204.c  
// compile with: /W4  
int func1()  
{  
   return 0;  
}  
struct S1  
{  
   int i;  
};  
  
int main()  
{  
   struct S1 s1 = { func1() };   // C4204  
   return s1.i;  
}  
```  
  
 Such initializations are invalid under ANSI compatibility ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)).