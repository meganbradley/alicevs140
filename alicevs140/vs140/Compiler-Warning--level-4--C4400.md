---
title: "Compiler Warning (level 4) C4400"
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
ms.assetid: f135fe98-4f92-4e07-9d71-2621b36ee755
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4400
'type' : const/volatile qualifiers on this type are not supported  
  
 The [const (C++)](../vs140/const--C---.md)and [volatile (C++)](../vs140/volatile--C---.md)qualifiers will not work with variables of common language runtime types.  
  
## Example  
 The following sample generates C4400.  
  
```  
// C4400.cpp  
// compile with: /clr /W4  
// C4401 expected  
using namespace System;  
#pragma warning (disable : 4101)  
int main() {  
   const String^ str;   // C4400  
   volatile String^ str2;   // C4400  
}  
```