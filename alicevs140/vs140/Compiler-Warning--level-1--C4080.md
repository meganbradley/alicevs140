---
title: "Compiler Warning (level 1) C4080"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 964fb3f4-b9fd-450b-aa23-35cece126172
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4080
expected identifier for segment name; found 'symbol'  
  
 The name of the segment in [#pragma alloc_text](../vs140/alloc_text.md) must be a string or an identifier. The compiler ignores the pragma if a valid identifier is not found.  
  
 The following sample generates C4080:  
  
```  
// C4080.cpp  
// compile with: /W1  
extern "C" void func(void);  
  
#pragma alloc_text()   // C4080  
  
// try this line to resolve the warning  
// #pragma alloc_text("mysection", func)  
  
int main() {  
}  
  
void func(void) {  
}  
```