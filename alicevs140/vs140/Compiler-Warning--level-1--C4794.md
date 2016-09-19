---
title: "Compiler Warning (level 1) C4794"
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
ms.assetid: badc9c36-fa1a-4fec-929b-7bfda7a7b79f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4794
segment of thread local storage variable 'variable' changed from 'section name' to '.tls$'  
  
 You used [#pragma data_seg](../vs140/data_seg.md) to put a tls variable in a section not starting with .tls$.  
  
 The .tls$*x* section will exist in the object file where [__declspec(thread)](../vs140/thread.md) variables are defined. A .tls section in the EXE or DLL will result from these sections.  
  
## Example  
 The following sample generates C4794:  
  
```  
// C4794.cpp  
// compile with: /W1 /c  
#pragma data_seg(".someseg")  
__declspec(thread) int i;   // C4794  
  
// OK  
#pragma data_seg(".tls$9")  
__declspec(thread) int j;  
```