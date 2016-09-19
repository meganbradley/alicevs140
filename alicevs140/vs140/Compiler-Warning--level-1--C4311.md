---
title: "Compiler Warning (level 1) C4311"
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
ms.assetid: ddc579d0-d051-47bc-915d-71ffb32323c9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4311
'variable' : pointer truncation from 'type' to 'type'  
  
 This warning detects 64-bit pointer truncation issues. For example, if code is compiled for a 64-bit architecture, the value of a pointer (64 bits) will be truncated if it is assigned to an `int` (32 bits). For more information, see [Rules for Using Pointers](http://msdn.microsoft.com/library/windows/desktop/aa384242).  
  
 For additional information about common causes of warning C4311, see [Common Compiler Errors](http://msdn.microsoft.com/library/windows/desktop/aa384160).  
  
 The following code example generates C4311 when compiled for a 64-bit target, and then demonstrates how to fix it:  
  
```  
// C4311.cpp  
// compile by using: cl /W1 C4311.cpp  
int main() {  
   void* p = &p;  
   unsigned int i = (unsigned int) p;   // C4311 for 64-bit targets  
   unsigned long long j = (unsigned long long) p;   // OK  
}  
  
```