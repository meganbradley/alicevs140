---
title: "Compiler Error C2628"
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
ms.assetid: 19a25e77-d5be-4107-88d5-0745b6281f98
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2628
'type1' followed by 'type2' is illegal (did you forget a ';'?)  
  
 A semicolon may be missing.  
  
 The following sample generates C2628:  
  
```  
// C2628.cpp  
class CMyClass {}  
int main(){}   // C2628 error  
```  
  
 Possible resolution:  
  
```  
// C2628b.cpp  
class CMyClass {};  
int main(){}  
```