---
title: "Compiler Warning (level 1) C4829"
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
ms.assetid: 4ffabe2b-2ddc-4c52-8564-d1355c93cfa6
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4829
Possibly incorrect parameters to function main. Consider 'intmain(Platform::Array\<Platform::String^>^ argv)'  
  
 Certain functions, such as main, cannot take reference type parameters. While compilation will succeed, the resulting image will probably not run.  
  
 The following sample generates C4829:  
  
```  
// C4829.cpp  
// compile by using: cl /EHsc /ZW /W4 /c C4829.cpp  
int main(Platform::String ^ s) {}   // C4829  
  
```