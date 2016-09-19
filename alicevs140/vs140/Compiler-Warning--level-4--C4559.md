---
title: "Compiler Warning (level 4) C4559"
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
ms.assetid: ed542f60-454d-45cb-85da-987ede61b1ab
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4559
'function' : redefinition; the function gains __declspec(modifier)  
  
 A function was redefined or redeclared and the second definition or declaration added a __**declspec** modifier (***modifier***). This warning is informational. To fix this warning, delete one of the definitions.  
  
 The following sample generates C4559:  
  
```  
// C4559.cpp  
// compile with: /W4 /LD  
void f();  
__declspec(noalias) void f();   // C4559  
```