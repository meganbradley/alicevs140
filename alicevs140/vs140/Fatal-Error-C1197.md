---
title: "Fatal Error C1197"
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
ms.assetid: 22b801b7-e792-41f6-a461-973c03c69f25
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1197
cannot reference 'mscorlib.dll_1' as the program has already referenced 'mscorlib.dll_2'  
  
 The compiler is matched to a version of the common language runtime.  However, an attempt was made to reference a version of a common language runtime file from a previous version.  
  
 To resolve this error, only reference files from the version of the common language runtime that shipped with the version of Visual C++ you are compiling with.  
  
## Example  
 The following sample generates C1197:  
  
```  
// C1197.cpp  
// compile with: /clr /c  
// processor: x86  
#using "C:\Windows\Microsoft.NET\Framework\v1.1.4322\mscorlib.dll"   // C1197  
// try the following line instead  
// #using "mscorlib.dll"  
```