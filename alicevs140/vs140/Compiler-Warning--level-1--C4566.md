---
title: "Compiler Warning (level 1) C4566"
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
ms.assetid: 65f40730-e86f-447c-b37b-16caadcfe311
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4566
character represented by universal-character-name 'char' cannot be represented in the current code page (page)  
  
 Not every Unicode character can be represented in your current ANSI code page.  
  
 Narrow strings (one-byte characters) are converted to multi-byte characters whereas wide strings (two-byte characters) are not.  
  
 The following sample generates C4566:  
  
```  
// C4566.cpp  
// compile with: /W1  
int main() {  
   char c1 = '\u03a0';   // C4566  
   char c2 = '\u0642';   // C4566  
  
   wchar_t c3 = L'\u03a0';   // OK  
   wchar_t c4 = L'\u0642';   // OK  
}  
```