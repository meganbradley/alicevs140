---
title: "Compiler Warning (level 3) C4159"
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
ms.assetid: e2cf964e-f4b8-4b2c-9569-1abb94307232
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4159
\#pragma pragma(pop,...) : has popped previously pushed identifier 'identifier'  
  
 Your source code contains a **push** instruction with an identifier for a pragma followed by a **pop** instruction without an identifier. As a result, ***identifier*** is popped, and subsequent uses of ***identifier*** may cause unexpected behavior.  
  
 To avoid this warning, give an identifier in the **pop** instruction. For example:  
  
```  
// C4159.cpp  
// compile with: /W3  
#pragma pack(push, f)  
#pragma pack(pop)   // C4159  
  
// using the identifier resolves the warning  
// #pragma pack(pop, f)  
  
int main()  
{  
}  
```