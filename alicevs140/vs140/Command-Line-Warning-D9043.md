---
title: "Command-Line Warning D9043"
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
ms.assetid: 9263e28d-217b-414c-bfb6-86efd3c27a77
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command-Line Warning D9043
invalid value 'warning_level' for 'compiler_option'; assuming '4999'; Code Analysis warnings are not associated with warning levels  
  
## Example  
 The following sample generates C9043.  
  
```  
// D9043.cpp  
// compile with: /analyze /w16001  
// D9043 warning expected  
int main() {}  
```